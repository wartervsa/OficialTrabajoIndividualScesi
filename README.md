# CURSO GIT SCESI
---
## MI PRIMERA EXPERIENCIA EN GIT 
---
### *¿Que es git?*

Git es un controlador de versiones, considerado por muchos como el mas optimo para controlar los distintos parches de tu proyecto.

---
### *Comando :* `git init` *|Iniciar un repositorio|*

Comienzas a usar git en tu repositorio seleccionado, en mi caso se llama *PRUEBASGIT* asi que en este directorio iniciara todo el control.

--- 

### *Comando :*`git status` *|Ver estado de archivos|*

Con este comando podras ver en que estado se encuentran tus archivos.-

```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
```

Aqui puede ver en que rama de encuentras(*On branch master*), (*Untacked files*) y tambien tenemos el *No commits yet* que son archivos ya rastreados y que esperan confirmacion se denomina *staged*

---
### *Comando :*`git add` *|Rastrear un archivo|*

Usar este comando para agregar un archivo que no aun no toma en cuenta git para las confirmaciones(commits).

---

### *Comando :*`git commit` *|Confirma las modificaciones en la rama|*

Agrega el/los archivos a tu repositorio local.
`git commit` Este comando si bien te ayuda a subir a tu repositorio local, se necesita de un titulo o si quieres una descripcion, al utilizar `git commit *archivo/s que agregaste*` se abrira tu editor de texto donde puede colocar el titulo y una descripcion, luego tenemos la opcion `git commit -m "el titulo de tu commit"` que te ahorra un poco de tiempo.

---

## Comandos de informacion:

---

### *Comando :* `git log` 

Te muestra el historial de tus commits, incluidos el autor del commit, la fecha en la que se realizo, el nombre del commit, el hash completo, el apuntador(HEAD) y la rama.

---

### *Comando :*`git log --oneline`

Es una version recortada del `git log`.

---

### *Comando :*`git log --graph`

Es una version grafica.

Si gustarias de mas comandos para ver distitas opciones de presentacion de informacion de tu repositorio, puedes usar `git log --help`. Pero con las ya mencionadas ya seria suficiente.

---

## Configuracion del name y email(error commits)

---

### *Comando :*`git config --global user.name "tu nombre"` && `git config --global user.email "tu email"`

Seguramente tuviste problemas con los commit, y se debe a la falta de aplicacion de usuario, con este comando ya estableces tu usuario y ya puedes hacer todo lo que quieras.




