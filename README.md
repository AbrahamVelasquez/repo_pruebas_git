# Explicación del Repo

Esto es un repositorio en el que iré haciendo pruebas en el entorno git/github,
con la finalidad de ir aprendiendo más sobre dichas herramientas.

## Comandos

### Comando de inicio (Initialize)

-> Sirve para inicializar el repositorio "en memoria".

```
git init
```

### Comando para agregar directorios/ficheros
 
-> Sirve para agregar al repositorios mi estructura o cosas. También para guardar
los nuevos cambios a al repositorio al momento, en cuando a ficheros no rastreados.

```
git add "Nombre del directorio/fichero"

git add . 
```

(Sirve para añadir todo lo que está)

### Comando para guardar cambios

-> Sirve para guardar los cambios que he hecho en mi respositorio.

```
git commit -m "Nombre del commit que le quiera dar, es el mensaje"

git commit -a -m "Mensaje"
```

Añade todos los ficheros que ya han sido modificados y que están rastreados
(tracked). Pero sólo afecta a los ficheros que git ya conocía, entonces,
los que están no rastreados (untracked) toca hacerles un git add . antes.

### Comando para ver mis commits

-> Sirve para ver los commits que se han hechos

```
git log 

git log --online 
```

El --online sirve para verlos en formato de una línea

### Comando para crear una nueva rama

-> Sirve para crear una nueva rama (branch).

```
git checkout -b "Nombre de la rama"
```

La -b significa crear una nueva rama

### Comando para ver las ramas del repositorio

-> Sirve para ver las ramas que hay, y también te dice en cual estás.

```
git branch
```

### Comando para cambiar de rama

-> Sirve para irse a otra rama del repositorio, hay dos maneras.

- Clásica:

```
git checkout "Nombre de la rama existente"
```

- Moderna:

```
git switch "Nombre de la rama existente"
```

### Comando para hacer cambios de una rama a otra

-> Sirve para que los cambios de una rama estén en la otra. 
En este caso, sólo pondré el merge y no el rebase.

1. Debes ir primero a la rama que quiere que tenga los cambios

```
git switch/checkout "Rama que tendrá los cambios"
```

2. Traer los cambios de la rama que quieras con el merge

```
git merge "Rama que tiene los cambios"
```

En caso no haber conflictos el merge se hace de manera automática,
de lo contrario, se deberá resolverlos y hacer después:

```
git add .
git commit
```

### Comando para quitar los archivos del "staging"

-> Sirve para quitar los archivos en staging, Es como el contrario de add.

```
git reset 
```

El contrario de add .

```
git reset "Nombre del archivo"
```

El contrario de git add "El nombre del archivo"

### Comando para deshacer los cambios

-> Sirve para eliminar las modificaciones que hayas hecho al fichero.
Se quitan del unstaging (No deshace el commit). Hay dos formas.

- Clásica: 

```
 git checkout -- "Nombre del archivo"
```

- Moderna:

```
git restore "Nombre del archivo"
```

### Comando para subir repositorio a GitHub

-> Sirve para añadir el repositorio a GitHub, es decir, de manera remota.

```
git remote add origin https://github.com/NombreDeUsuario/NombreDelRepositorio.git
```

### Comando para subir cambios a GitHub

-> Sirve para que después de hacer cambios de manera local se suban a GitHub.

```
git push -u origin "Nombre de la rama central Ej: master o main"
```

La -u significa que se vincule con la rama origen del repositorio en GitHub, 
depués de ello, sólo habra que user git push o git pull.

```
git push origin "Nombre de la nueva rama"
```

Esto último es para subir una nueva rama de local a GitHub

### Comando para traer los cambios del GitHub

-> Sirve para que cuando haga cambios en el Github, los pueda ver de manera
local.

```
git pull origin "Nombre de la rama que quieres traer, Ej: master o main"
```

### Comando para volver a un commit anterior

-> Sirve para poder irte a un versión anterior de tu repositorio.
Primero debes hacer un git log o git log --online para ver el hash 
del commit y poder ir a él.

```
git checkout "hash del commit"
```

Para esto primero hay que hacer git log o git log --online para ver el hash
del commit a ir. Lo que ocurre en este caso es de manera "temporal", como 
si fuera "modo lectura" sin cambiar la historia.
