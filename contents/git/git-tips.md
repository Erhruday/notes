# Git Tips

***

## Tags de Git

* Ver tags (sólo lista nombres):

	git tag

* Ver tags con sus mensajes:

	git tag -n


*NOTA: Los nombres de los tags serán únicos (suele usarse número de versión).*

* Guardar tag (sólo con nombre):

	git tag tag_name

* Guardar tag (con nombre y mensaje):

	git tag tag_name -m "mensaje del tag"

* Reescribir el mensaje de un tag:

	git tag tag_name -f -m "Nuevo mensaje"

* Eliminar un tag:

	git tag -d tag_name


*NOTA: Los tags, por defecto, sólo se guardan en el repo local.*

* Enviar los tags al repo remoto:

	git push --tags


***

## Varios Git

* Eliminar todos los cambios del espacio de trabajo (sobre ficheros ya en seguimiento)

	git checkout .


* Decartar último commit local y remoto:

	git reset HEAD~1
	git push -f


***

[Go to index](../../README.md)
