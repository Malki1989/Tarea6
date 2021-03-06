## Apartado Malki1989 ##

Como yo he creado el proyecto no puedo usar la misma cuenta para hacer un fork, asi que 
he cogido una cuenta que uso de pruebas en el trabajo para probar nuevas funcionalidades i
hare el fork desde esa cuando, el nombre de usuario es u24061.

### Realizamos el fork ##

Iniciamos sesion con la cuenta u24061 y en el menu de la derecha pulsamos el boton FORK, 
asi se nos pasa el codigo que hay actualmente en el proyecto a nuestra cuenta.

Vamos al directorio y clonamos el proyecto, no es necessario hacer ramas, puesto que cada
miembro va a tocar solo su projecto.

$ git clone https://github.com/u24061/Tarea6.git
Cloning into 'Tarea6'...
remote: Enumerating objects: 42, done.
remote: Counting objects: 100% (42/42), done.
remote: Compressing objects: 100% (36/36), done.
remote: Total 42 (delta 6), reused 6 (delta 1), pack-reused 0
Receiving objects: 100% (42/42), 307.79 KiB | 1.76 MiB/s, done.
Resolving deltas: 100% (6/6), done.

Una vez clona nos metemos dentro para iniciar los cambios.

### Configuracion rama local y remota ###

- Es conveniente hacer que las ramas local y remota se apunten por defecto entre ellas, por ello ejecutamos el comando:

$ git branch --set-upstream-to origin main
Branch 'main' set up to track remote branch 'main' from 'origin'.

Asi no tendremos que especificar en el push a donde lo queremos subir, ya que por defecto lo hara donde nos interesa.

### Creación de archivos ###

Creamos y editamos los archivos necesarios para que el proyecto siga adelante. Una vez realizados los cambios, vamos realizando los commit de cada uno de ellos.

- Archivo *content.html*

```
$ touch content.html

$ vsc content.html

$ git add content.html

$ git commit -m "Añadir content.html"
[main d713ca7] Añadir content.html
 1 file changed, 17 insertions(+)
 create mode 100644 content.html
```
 
- Archivo *content.css*

```
$ touch css/content.css

$ vsc content.css

$ git add css/content.css 

$ git commit -m "Añadir content.css"
[main 9ceb57d] Añadir content.css
 1 file changed, 3 insertions(+)
 create mode 100644 css/content.css
```

- Creación e inclusión del archivo content.html al archivo index.html.

```
$ touch index.html

$ vsc index.html

$ git add index.html

$ git commit -m "Añadir index.html"
[main f9f3187] Añadir index.html
 1 file changed, 12 insertions(+)
 create mode 100644 index.html
```

- Modificación del archivo content.html para añadir incluya el archivo css correspondiente.

```
$ vsc content.html

$ git add content.html

$ git commit -m "Incluimos el css que no incluimos antes en el content.html"
[main fc4db71] Incluimos el css que no incluimos antes en el content.html
 1 file changed, 1 insertion(+)
```

- Quitamos margenes del body

$git vsc css/content.css

$git add css/content.css

$git commit -m "Quitar margenes content.css"
[main 84ea7f8] Quitar margenes content.css
 2 files changed, 109 insertions(+), 3 deletions(-)
```

### Subida de archivos a producción ###

Una vez realizados todos nuestros cambios, realizamos un **git push** para que los suba a nuestra rama.

```
$ git push 

Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 4 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (18/18), 3.01 KiB | 513.00 KiB/s, done.
Total 18 (delta 5), reused 0 (delta 0), pack-reused 0       
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/u24061/Tarea6.git
   3afd015..84ea7f8  main -> main
```

Una vez subidos los cambios, creamos un *pull request* hacia el proyecto original i lo validamos.

## Apartado Toni Gomila ##

### Creación, clonación y pull y asignación de branch ###

Primero de todo, creamos el *fork* a partir del repositorio base con las herramientas que nos ofrece la plataforma GitHub.

Una vez realizado el *fork*, clonamos el proyecto en un directorio local:

```
git clone https://github.com/agomilag/Tarea6.git
Cloning into 'Tarea6'...
remote: Enumerating objects: 64, done.
remote: Counting objects: 100% (64/64), done.
remote: Compressing objects: 100% (48/48), done.
remote: Total 64 (delta 13), reused 28 (delta 8), pack-reused 0 eceiving objects:
Receiving objects: 100% (64/64), 312.03 KiB | 2.81 MiB/s, done.
Resolving deltas: 100% (13/13), done.
```

Una vez clonado el repositorio, traemos los datos mediante el comando **git pull**. También asignamos que el repositorio local apunte directamente al remoto:

```
git pull
Already up to date.

Dirección branch

git branch --set-upstream-to origin main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

### Creación, modificación y puesta en producción de archivos ###

#### Archivo header.html ####

```
touch header.html

header>nav.menu>ul>li*5{Menú $}

<header>
    <nav class="menu">
        <ul>
            <li>Menú 1</li>
            <li>Menú 2</li>
            <li>Menú 3</li>
            <li>Menú 4</li>
            <li>Menú 5</li>
        </ul>
    </nav>
</header>


git add header.html

git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   header.html

git commit -m "Creación y estructura base header.html"
[main e50ee6d] Creación y estructura base header.html
 1 file changed, 11 insertions(+)
 create mode 100644 header.html
```

#### Archivo css/header.css ####

```
touch css/header.css

/*Escribo sentencia para añadir borde al menú entero.*/

nav.menu
{
    border: black solid 1px;
}


git add css/header.css

git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   css/header.css


git commit -m "Creación y primera sentencia archivo css/header.css"
[main a4536d1] Creación y primera sentencia archivo css/header.css
 1 file changed, 6 insertions(+)
 create mode 100644 css/header.css
```

#### Modificaciones header.html ####

- Volvemos a modificar el archivo header.html para añadir más estructura y poder enlazar el archivo css.
- Usamos la abrievatura de Emmet html:5 para generar la estructura básica de una página html
- Desplazamos nuestro header dentro del body y en el head generamos una etiqueta link para enlazar el css.
- Desplegamos el código y en el atributo href colocamos la ruta hacia nuestro archivo css

```
link:css

<link rel="stylesheet" href="css/header.css">
```
- Guardamos modificaciones, volvemos a añadir el archivo header.html al stage y realizamos commit.
```
git add header.html

git commit -m "Estructura básica html creada y enlace archivo css"
[main 17a6027] Estructura básica html creada y enlace archivo css
 1 file changed, 14 insertions(+)
```

#### Modificaciones css/header.css ####

- Una vez comprobado que el archivo css está bien vinculado, realizamos otros pequeños cambios, esta vez añadimos un color de fuente al menú y un padding-bottom a los elementos li.

```
/*Escribo sentencia para añadir borde al menú entero.*/

/*Añado color de fuente y un padding abajo de los elementos li*/

nav.menu
{
    border: black solid 1px;
    color: darkblue;
}

.menu ul li
{
    padding-bottom: 5px;
}
```

- Guardamos modificaciones, volvemos a añadir el archivo css/header.css al stage y realizamos commit.

```
git add css/header.css

git commit -m "Añadir color de fuente y padding abajo de los elementos li"
[main 220956e] Añadir color de fuente y padding abajo de los elementos li
 1 file changed, 8 insertions(+)
```

Por ultimo, creamos el archivo READMEToniGomila.md donde estoy guardando todas estas instrucciones de mi trabajo

-- A partir de este punto, las instrucciones se han añadido mediante via web para poder documentar todo el trabajo --

Realizamos el commit del archivo READMEToniGomila.md y al tener ya los 5 commits, realizamos el **push**.

```
git commit -m "Añadir archivo READMEToniGomila.md"
[main 1f2e59d] Añadir archivo READMEToniGomila.md
 1 file changed, 153 insertions(+)
 create mode 100644 READMEToniGomila.md

git push
Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 4 threads
Compressing objects: 100% (17/17), done.
Writing objects: 100% (17/17), 3.45 KiB | 1.73 MiB/s, done.
Total 17 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
To https://github.com/agomilag/Tarea6.git
   91dbdee..1f2e59d  main -> main
```
## Alex ###

### Pasos a realizar una subida a una rama "Portada" de Github a traves de fork ###

- Pulsamos en el boton donde pone tenedor en el repositorio de la Tarea 5. Y vemos como se me ha creado correctamente ya que pone 1 donde pone "tenedor" 
   ![Clonar tarea](img/portada/0.png)


- Utilizamos el comando **git clone** con el repositorio correspondiente. Una vez clonada, podemos entrar en ella con el comando **cd nombre-del-repositorio**.
   ![Clonar tarea](img/portada/1.png)

- Ahora creamos una nueva Rama que se va llamar Portada-Alejandro con el comando **git checkout -b portada-Alejandro** y nos movera automaticamente ha la rama que hemos creado ![Clonar tarea](img/portada/1.png)

- Una vez dentro, crearemos el archivo con el comando de nuestra preferencia **touch/nano/vi** y lo llamaremos portada.html.

- Para añadir el archivo al proyecto tenemos que usar el comando **git add**.
   ![Añadir archivo](img/portada/4.png)

- Ejecutamos **git status** para comprobar que si se ha sincronizado correctamente. Si aparece en verde, está todo correcto.
 
- Ahora pasamos a registrar cambios en el historial con el comando **git commit -m "Comentario que queramos poner** y vemos que se ha realizado correctamente 
   ![Comando commit](img/portada/5.png)

- Ahora toca subir el archivo a Github a través del comando **git push origin portada-Alejandro**.
   ![Comando push](img/portada/7.png)

- Ahora tenemos que hacer 4 commit más:

   - El primero será la modificación del archivo portada.html poniendo una estructura básica de una página html.
      ![Estructura HTML](img/portada/8.png)

   - Creamos la carpeta portada para las imágenes. 
      ![Creación carpeta imágenes](img/portada/9.png)

   - Colocamos las imágenes dentro de la carpeta creada anteriormente 
      ![Subida imágenes](img/portada/10.png)

- Por ultimo pasamos a fuionar los proyectos ![Subida imágenes](img/portada/11.png)

### Readme - Vicente ###

- Git fetch

En esta Tarea, cómo la anterior debemos trabajar en equipo, vamos a hacer un Fetch del repositorio original. Esto sirve para poder hacer una copia exacta del repositorio y añadirlo a nuestro GitHub. Se hace pulsando sobre el botón de Fork. En esta práctica no necesitaremos hacer ninguna rama nueva por que trabajamos sobre un "reopsitorio propio" para posteriormente fusionar los cambios.

![Imagen1](./img/footer/1.PNG)
![Imagen2](./img/footer/2.PNG)

- Git clone

Ahora sí podemos usar el comando ***git clone nombre_repositorio*** y cambiar a la nueva carpeta para empezar a modificar nuestro proyecto.

![Imagen3](./img/footer/3.PNG)

- Git add y git commit

Después de realizar los cambios que requería la práctica y he realizado en el vídeo debemos hacer ***git add .***  y después ***git commit*** para dejar estos cambios preparados para subir.

![Imagen4](./img/footer/4.PNG)

- Git push

Una vez ya tengamos todos los cambios necesarios y estemos preparados para hacer el push, vamos a lanzarlo con el comando ***git push origin main***. No debemos especificar ramas nuevas ya que estamos trabajando "sólos".

![Imagen5](./img/footer/5.PNG)

- Pull request y merge

Para finalizar, lo que debemos hacer es solicitar un pull request y esperar a que el propietario o encargado del proyecto revise y acepte los cambios que queremos incorporar y fusionar al repositorio original.

![Imagen6](./img/footer/6.PNG)

![Imagen7](./img/footer/7.PNG)

![Imagen8](./img/footer/8.PNG)
