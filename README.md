# Explicación del Repo

Esto es un repositorio en el que iré haciendo pruebas en el entorno git/github,
con la finalidad de ir aprendiendo más sobre dichas herramientas.

## Comandos

### Comando de inicio (Initialize)

-> Sirve para inicializar el repositorio "en memoria".

git init

### Comando para agregar directorios/ficheros
 
-> Sirve para agregar al repositorios mi estructura o cosas. También para guardar
los nuevos cambios a al repositorio al momento, en cuando a ficheros no rastreados.

git add "Nombre del directorio/fichero"

git add . 

(Sirve para añadir todo lo que está)

### Comando para guardar cambios

-> Sirve para guardar los cambios que he hecho en mi respositorio.

git commit -m "Nombre del commit que le quiera dar, es el mensaje"

git commit -a -m "mensaje"

Añade todos los ficheros que ya han sido modificados y que están rastreados
(tracked). Pero sólo afecta a los ficheros que git ya conocía, entonces,
los que están no rastreados (untracked) toca hacerles un git add . antes.


### Comando para ver mis commits

-> Sirve para ver los commits que se han hechos

git log 

git log --online 

El --online sirve para verlos en formato de una línea

### Comando para crear una nueva rama

-> Sirve para crear una nueva rama (branch).

git checkout -b "Nombre de la rama"

### Comando para ver las ramas del repositorio

-> Sirve para ver las ramas que hay

git branch
