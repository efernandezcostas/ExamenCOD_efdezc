# Pasos

## Creamos rama_readme
- Creamos la nueva rama y hacemos checkout a ella con `git checkout -b rama_readme`
- Creamos el `README.md` y los primeros pasos.

## Revisamos el código de la Interface
- Primero accedemos a la rama desde el IDE con la opción `New branch from Origin/Interface`
- Eliminamos el último commit desde el IDE utilizando la opción `Undo commit`
- Desde la consola hacemos `git status` y seguimos las indicaciones:
    - `git restore --staged src/Interface.java` para quitarlo del área del stage.
    - `git restore src/Interface.java` para restaurar el estado que tenía antes del commit (Eliminar el código que había en este commit)

## Hacemos merge de las ramas hacia main
- Desde el IDE, hacemos `checkout main`. Una vez en main hacemos merge de las ramas que queremos, en este caso:
- Usamos la opción `Merge "rama" onto main` con cada una de las ramas que queremos (Interface y Datos)

## Hacemos --squash a los anteriores merge
- Como olvidé hacer merge --squash y solo hice merge, para solucionar el diseño de los commit hice:
  - Cambio el nombre a la anterior rama main con `git branch -m old-main`
  - Checkout al anterior main `git checkout old-main`
  - Creamos y checkout a nuevo main `git checkout -b main`
  - Merge squash con `git merge --squash old-main`

## Añadimos el tag

## Editamos el .gitgignore