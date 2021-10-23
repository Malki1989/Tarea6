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