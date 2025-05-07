# CURSO GIT SCESI
---
## MI PRIMERA EXPERIENCIA EN GIT/PRIMERA CLASE EN GIT 
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

### *Comando :*`git commit` *|Confirma las modificaciones en la rama|*

Agrega el/los archivos a tu repositorio local.
`git commit` Este comando si bien te ayuda a subir a tu repositorio local, se necesita de un titulo o si quieres una descripcion, al utilizar `git commit *archivo/s que agregaste*` se abrira tu editor de texto donde puede colocar el titulo y una descripcion, luego tenemos la opcion `git commit -m "el titulo de tu commit"` que te ahorra un poco de tiempo.




