# DAW
Despliegue de aplicaciones web
comando git 

***************Configuracion de git**********************

lo minimo para tener git es tener un nombre de usuario y un gmail

`---> git config --global user.name "nombre_usuario"`
`---> git config --gloabal user.gmail "ejemplogmail@.com"`

**************************************************************


********************inicializar git ********************

---> git init . 
en el fichero que queramos controlar 

**************************************************************



***************cambiar nombre a la rama, crear rama,moverse de rama,combinar cambios entre rama, comparar ramas *************

 ---> git config --global init.defaultBranch main

para cambiar el nombre de la rama a la hora de crear una rama principal 
 
---> git branch -m main
cambiar nobre a la rama en la que estemos 

---> git branch -m (nombre de la rama que queremos cambiar) (nombre nuevo de la rama 

---> git branch nombre de la rama
crea un nuevo flujo de trabajo con todos los datos de la rama principal 

---> git switch nombre de la rama 
nos movemos a la rama que queramos 

---> git merge id_rama
nos trae los datos del id_rama indicado en el comando a la rama donde estemos en ese momento 

---> git diff nombre_rama 
nos permite comparar los cambios entre una rama y otra 

**************************************************************



******************fotografia de cambios ******************

---> git status 
muestra los ficheros que aun no se han añadido al stage
y de los que si se han añadido 

---> git add . 
añade todos los ficheros al stage para hacereles una fotografia 

---> git add nombre_fichero 
añade solo un fichero al stage 

---> git stash 
hace un guardado temporal a nivel local 


---> git stash list
muestra todos los guardados temporales 


---> git commit -m "añadir comentario"
hace la fotografia de los ficheros que esten añadidos en el stage y se le añade un identificador unico junto con el mensaje que se le añadio 



**************************************************************

******************Historial de fotografia ******************
---> git log
muestra todos los commit realizados anterior mente 
---> git log --graph 
nos mustra los mommit pero añadiendo un dibujo grafico 
---> git log --graph --pretty=oneline
 nos muetra la informacion en una linea 
 
---> git log --graph --decorate --all --oneline
nos da el id mas resumido y muestra donde esta el head

---> git reflog 
nos da un historial de todos los commit y movimeitos que hemos hecho durante todo el proyecto

**************************************************************

******************Alias Comandos******************
---> git config --global alias.tree "log --graph --decorate --all --oneline"
renombramos todo el comando que esta entre comillas dobles a tree
---> git config --global --get-regexp alias
nos muestra todos los comandos a los que le hayamos hecho un alias 

**************************************************************

******************Inorar ficheros ******************
---> touch .gitignore 
nos creare un fichero oculto donde si le ponemos dentro del fichero **/ nombre del fichero que queremos innorar de esta forma todos los ficheros que se llamen asi nunca git me va a recordar que meta ese fichero en el area de stage (los asteriscos significa que nos da igual donde este ese fichero )

**************************************************************

******************Desplazamientos**************

---> git diff 
 nos muestra los cambios nuevos y antigos de nuestro ficheros 

---> git checkout id_commit 
nos movemos al estado de nuestro proyecto en ese commit

**************************************************************

*************Borrar en git y recuperar lo borrado*************

---> git checkout nombre_fichero
 se nos borra todo lo modificado en el fichero hasta el ultimo commit que tengamos registrado 

---> git stash drop
borra los almacenamientos temporales que tengamos 

---> git reset --hard id_del _commit 
nos borra todo lo que hemos hecho posterior al id del commit

y si queremos recuparar lo borrado es el mismo comando pero con el id del commit al que queramos recuperar 

---> git branch -d nombre_de_rama 
elimina rama del proyecto 

**************************************************************

********************Etiquetar commit**************************
---> git tag nombre_tag 
esto añade un nombre al ultimo commit que hemos realizado

---> git tag nombre_tag "id_del_commit"
este comando le pone un nombre al commit que queramos 

---> git tags 
muetra los tag que tengamos creados 


***************************************************************											 *
*   		  			GITHUB					 *
*											 *
**************************************************************


*******************CONECTAR MEDIANTE SSH *********************
---> ls -al ~/.ssh
comprobar que existan claves públicas y privadas de ssh

---> ssh-keygen -t ed25519 -C "your_email@example.com"
generar una clave pública y privada 

---> Get-Service ssh-agent

en el powerShell iniciamos el ssh-agent

---> ssh-add c:/Users/omarb/.ssh/id_rsa

añadimos la clave al agente ssh
---> añadimos la clave a github

---> ssh -T git@github.com
lanzamos ese comando en la terminal y le demos yes 

*******************conectar con la nube *********************

--->git remote add origin https://github.com/OmarOrtez
 asociamos el repositorio de la nube 
--->git push -u origin main
lanzamos los datos a la nube

--->git fetch
Se descarga el historial de cambios, pero sin descargar los cambios  

--->git pull
Se descarga los cambios de la nube al local

--->git remote –v
Muestra los repositorios remotos

--->git pull origin nombre_rama

para traer cambios de la nube a una rama 

git push origin feature/footer
--->git push origin nombre_rama
Para subir los datos a la nube

