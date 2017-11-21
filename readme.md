* __Paso 11:__
	
		git reset --hard HEAD~1 
El comando reset mueve el puntero *HEAD* (y en el caso de que apunte a una rama también la mueve) al *commit* padre. Al aplicarle *--hard* modifica el working copy (a partir de ahora WC) y lo deja tal cual estaba cuando se realizó al *commit* al que ahora apunta *HEAD*.
	
* __Paso 12:__

		git reset --hard 590c20e (*)	(	
Es la manera más rápida que se me ha ocurrido para volver al *commit* anterior y arrastrar también la rama *styled*. 
Otras manera era haciendo un nuevo *commit*, pero para ello se tendría que haber modificado otra vez el archivo *git-nuestro.md*, luego aplicar:
	
		git add *
y por último realizar el *commit*:
		
		git commit -m 'vuelvo a modificar el santo grial de git y a dejarlo en la version 1.2'
También existía la posibilidad de realizarlo mediante un *checkout*, el problema de este comando es que solo hubiera desplazado el *HEAD* al commit deseado y no la rama *styled*. Si esto hubiera sido lo deseado el comando ejecutado sería el siguiente:
	
		git checkout  590c20e (*)
(*) 590c20e es el id del *commit* deseado.

* __Paso 13:__						
	El *merge* no genera ningún conflicto debido a que la rama *styled* pertenece a la misma fila que la rama *master*. Al pertenecer a la misma fila estan encadenados por una serie de *hunks*, en este caso uno. 

* __Paso 19:__			
En este caso si que ha habido un conflicto al realizar un *merge*. El motivo del conflicto es que ambas ramas pertenecen a filas distintas. En el paso anterior se ha producido una bifurcación, ya que el *commit* no se ha realizado sobre el último hijo de la fila. Por decirlo de alguna manera el motivo del conficto es que se han aplicado *hungs* distintos sobre el nexo común. En este caso la rama *master*.                          
* __Paso 21:__
Al aplicar este comando no se ha realizado ningún conflicto debido al mismo motivo que en el *paso 13*. Pertenecen a la misma linea, por lo que sus *hungs* estan correlacionados.
* __Paso 25:__

			git log --graph	
					
* __Paso 26:__

			git merge --no-ff title
Si que podria ser *fastforward* porque los *commits* forman parte de la misma linea. Solo no se puede aplicar *fastforward* entre dos *commits* que forman parte de una bifucarcación diferente. Se podría utilizar el comando de *fastforward* pero *git* aplicaría un *no fastforward*. 

* __Paso 27:__

		git reset HEAD~1
		
* __Paso 28:__

		git reset HEAD~1

* __Paso 29:__

		git branch -D title
		
* __Paso 30:__

		git reset --hard  4e72ec2 (*)
(*)4e72ec2 es el id del *commit*.

* __Paso 32:__

		git reset f9c5250 (*)
(*)f9c5250 es el id del *commit*


* __Paso 33:__

		git reset 044bd21 (*)
(*) 044bd21 es el id del *commit*		
		
