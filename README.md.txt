# Tarea 6 #

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



