## Practica 4: Desfacer cambios

### Comandos empregados

``` bash 
git clean -f
```
> Sirve para eliminar un arquivo que ainda non esta para commitear.

``` bash 
git reset --soft HEAD~1
```
> Sirve para eliminar solo o commit pero non os cambios no stage.

``` bash 
git reset --hard HEAD~1
```
> Sirve para volver o repo o estado anterior.

```bash 
git reset "archivo"
```
> Git mixed. Restablece o indice pero non o arbol de traballo e indica o que non se actualizou.

``` bash 
git restore "arquivo"
```
> Sirve para desfacer os cambios que se acaban de facer nun arquivo.

``` bash
git restore --stage
```
> Sirve para desfacer os cambios que se acaban de facer no stage.


### Pasos a seguir na práctica.

1. Eliminamos a ultima linea de indice.txt e executamos o comando git status para comprobar o estado do repo.
2. Executamos o comando git restore para desfacer os cambios que acabamos de realizar. 
3. Volvemos a eliminar a ultima linea de indice.txt e executamos o comando "git add ." para añdilo o stage.
4. Desfacemos o ultimo git add . executando o comando "git restore --stage" e comprobamos o estado do repo.
5. Volvemos eliminar a ultima linea de indice.txt, eliminamos capitulo3.txt e engadimos o arquivo capitulo4.txt.
6. Facemos un git add . para engadir os cambios e revisamos o estado do repo.
7. Facemos un git restore --stage * para desfacer todos os cambios no stage e revisamos o estado do repo.
8. Facemos un git restore * para desfacer todos os cambios e revisamos o estado do repo.
9. Facemos git clean -f para eliminar o arquivo novo "capitulo4.txt" 
10. Eliminamos a ultima linea de indice.txt e o capitulo3.txt
11. Facemos git add * para engadir todos os cambios e despois git commit -m "borrado accidental" e revisamos o estado do repo.
12. Facemos un git reset --soft para desfacer o commit pero non o git add . nin os cambios e revisamos o estado do repo vendo que o git add ainda se conserva.
13. Facemos de novo git commit -m "borrado accidental" e un git log para ver o estado do repo.
14. Volvemos a ultima version anterior do repo utilizando o comando git reset --hard e vemos que o repo volveu o estado anterior.
