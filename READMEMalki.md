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

