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

-> Sirve para ver las ramas que hay, y también te dice en cual estás.

git branch

### Comando para cambiar de rama

-> Sirve para irse a otra rama del repositorio, hay dos maneras.

- Clásica:

git checkout "nombre de la rama existente"

- Moderna:

git switch "nombe de la rama existente"

### Comando para hacer cambios de una rama a otra

-> Sirve para que los cambios de una rama estén en la otra. 
En este caso, sólo pondré el merge y no el rebase.

1. Debes ir primero a la rama que quiere que tenga los cambios

git switch/checkout "rama que tendrá los cambios"

2. Traer los cambios de la rama que quieras con el merge

git merge "rama que tiene los cambios"

En caso no haber conflictos el merge se hace de manera automática,
de lo contrario, se deberá resolverlos y hacer después:

git add .
git commit

### Comando para quitar los archivos del "staging"

-> Sirve para quitar los archivos en staging, Es como el contrario de add.

git reset 

El contrario de add .

git reset "El nombre del archivo"

El contrario de git add "El nombre del archivo"

### Comando para deshacer los cambios

-> Sirve para eliminar las modificaciones que hayas hecho al fichero.
Se quitan del unstaging (No deshace el commit). Hay dos formas.

- Clásica: 

 git checkout -- "El nombre del archivo"

- Moderna:

git restore "El nombre del archivo"
