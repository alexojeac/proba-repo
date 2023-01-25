# Practicas Git


## Practica 1: creación e conexión de repositorios git


### Comandos empregados

```bash
git init
```
> Sirve para inicializar un repo local

```bash
git config --global user.name "Nome de usuario"
```
> Sirve para engadir o nome do usuario ao repositorio.

```bash
git config --global user.email correo
```
> Sirve para engadir o correo do usuario ao repositorio.

```bash
git add .
```
> Sirve para engadir todos os arquivos dun directorio ao repositorio local.

```bash
git commit -m "Mensaxe"
```
> Sirve para facer un commit dos arquivos ao repositorio local.

```bash
git branch -M main
```
> Sirve para cambiar a rama do repositorio a main.

```bash
git remote add origin https://github.com/fersp95/proba-repo
```
> Sirve para conectar o repositorio local e o repositorio en liña.

```bash
git push -u origin main
```
> Sirve para subir o contido do repositorio local ao repositorio en liña.

```bash
git pull --all
```
> Sirve para baixar o contido do repositorio en liña ao repositorio local.

### Pasos a seguir na práctica

1. Inicializar repo local co comando `git init`.
2. Establecemos o nome de usuario co comando `git config --global user.name "Nome de usuario"`
3. Establecemos o correo do usuario co comando `git config --global user.email correo`
4. Crear arquivos index.html e index2.html e engadilos ao repositorio local co comando `git add .`
5. Facemos o primero commit co comando `git commit -m "Creación do proxecto"`
6. Modificamos a rama á rama main do repositorio co comando `git branch -M main`
7. Unimos o repositorio local co repositorio en liña co comando `git remote add origin https://github.com/fersp95/proba-repo`
8. Subimos o contido do repositorio local ao repositorio en liña co comando `git push -u origin main`
9. Creamos o arquivo README.md
10. Baixamos os arquivos do repositorio en liña ao local co comando `git pull --all`

## Practica 2: creación e conexión de repositorios git

### Comandos empregados

```bash 
git config --global color.ui auto
```
> Sirve para modificar o color da interfaz de usuario.

```bash 
git diff
```
> Sirve para mostrar as modificacions entre distintos commits.

``` bash 
git show
```
> Sirve para mostrar visualmente as diferencias de contido entre os commits.

``` bash 
git commit --amend -m"
```
> Modifica a mensaxe de descripción do commit.

### Pasos a seguir na práctica.
1. Creamos o repositorio Libro.
2. Creamos o archivo INDICE.txt.
3. Añadimos o archivo o repositorio Libro.
4. Comprobamos o estado do respositorio.
5. Realizamos un commit.
6. Revisamos de novo o estado do repositorio.
7. Modificamos o archivo INDICE.txt.
8. Mostramos os cambios respecto a última versión.
9. Facemos un commit dos cambios.
10. Cambiamos a mensaxe do último commit.
11. Volvemos mostrar os cambios no repositorio.

## Practica 3: manexo de historial de cambios de repositorios git

### Comandos empregados

```bash 
git clone
```
> Sirve para clonar un repositorio.

```bash 
git reset --hard codigo
```
> Sirve para devolver o repositorio ó estado dun commit determinado.

``` bash 
git add .
```
> Sirve para añadir todos os archivos do directorio actual.

``` bash 
git commit -m "texto"
```
> Sirve para subir os cambios ó repositorio remoto.

``` bash 
git log
```
> Sirve para ver todos os cambios feitos nos commits do repositorio.

``` bash 
git diff HEAD~2..HEAD
```
> Sirve para mostrar as diferencias e modificacions entre dous commits.

``` bash 
git annotate "archivo"
```
> Sirve para mostrar as lineas de comandos e o autor que as modificou.

### Pasos a seguir na práctica.

1. Clonamos o repositorio Libro do enlace https://github.com/asalber/libro-git e configurámolo.
2. Creamos a carpeta capitulos e dentro o ficheiro capitulo1.txt co contido indicado.
3. Engadimolo ao repositorio e facemos un commit.
4. Mostramos os cambios.
5. Creamos o ficheiro capitulo2.txt co contido indicado, engadimolo ao repositorio e facemos un commit
6. Mostramos as diferencias entre a versión actual e dúas versións antes.
7. Creamos o ficheiro capitulo3.txt co contido indicado, engadímolo ao repositorio e facemos un commit
8. Mostramos as diferencias entre a primeira e a última versión do repositorio.
9. Engadimos ao final do ficheiro indice.txt a liña "Capítulo 5: Conceptos avanzados"
10. Engadímolo ao repositorio e facemos un commit.
11. Mostramos quen fixo os cambios no ficheiro indice.txt

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
> Sirve para desfacer os cambios que se acaban de facer pero solo no stage.

### Pasos a seguir na práctica.

1. Eliminamos a última linea de indice.txt e executamos o comando git status para comprobar o estado do repo.
2. Executamos o comando git restore para desfacer os cambios que acabamos de realizar. 
3. Volvemos a eliminar a última linea de indice.txt e executamos o comando "git add ." para añadilo o stage.
4. Desfacemos o ultimo git add . executando o comando "git restore --stage" e comprobamos o estado do repo.
5. Volvemos eliminar a última linea de indice.txt, eliminamos capitulo3.txt e engadimos o arquivo capitulo4.txt.
6. Facemos un git add . para engadir os cambios e revisamos o estado do repo.
7. Facemos un git restore --stage * para desfacer todos os cambios no stage e revisamos o estado do repo.
8. Facemos un git restore * para desfacer todos os cambios e revisamos o estado do repo.
9. Facemos git clean -f para eliminar o arquivo novo "capitulo4.txt" 
10. Eliminamos a última linea de indice.txt e o capitulo3.txt
11. Facemos git add * para engadir todos os cambios e despois git commit -m "borrado accidental" e revisamos o estado do repo.
12. Facemos un git reset --soft para desfacer o commit pero non o git add . nin os cambios e revisamos o estado do repo vendo que o git add ainda se conserva.
13. Facemos de novo git commit -m "borrado accidental" e un git log para ver o estado do repo.
14. Volvemos a última version anterior do repo utilizando o comando git reset --hard e vemos que o repo volveu o estado anterior.
