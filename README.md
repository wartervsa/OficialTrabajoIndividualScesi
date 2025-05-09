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

---

## Branch(Ramas)

---

Una rama es una copia de tu linea/rama principal de trabajo.

![Representacion grafica de las ramas](https://gitbookdown.dallasdatascience.com/img/git_branch_merge.png)

---

 ### *Comando :*`git branch <nombre de tu rama>`*|Creacion de una rama|*

 Crea una rama a partir de la rama padre(master/main). Cabe recalcar que los cambios en esta rama no afectan a la rama padre/principal.

 ---

### *Comando :*`git branch` *|Lista de ramas|*

Se puede ver todas las ramas de tu repositorio local, la rama en la que te encuentras esta marcada con un (*).

---
### *Comando :*`git branch -r` *|Lista de ramas remotas|*

Muestra solo las ramas de tu repositorio remoto.

---

### *Comando :*`git branch -a` *|Lista TODAS las ramas|*

Se muestran las ramas tanto de tu repositorio local como de tu repositorio remoto.

---

### *Comando :*`git branch -d <nombre de la rama>` *|Elimina la rama|*

Es importante resaltar que no te elimanara la rama si antes no fusionaste (*merged*) esa rama con la rama principal. Hay una opcion para poder eliminar sin necesidad de merged y es  `git branch -D <nombre de la rama>`.


## Movimiento y fusion(merge) entre ramas

---

### *Comando :*`git merge` *Fusiona ramas*

*IMPORTANTE!!* Debes encontrarte en la rama a cla ual quieres agregar la rama.

---

### *Comando :*`git checkout <rama>` *|Cambiar de rama|*

Con este comando podras moverte entre ramas. Tambien tenemos la variante `git checkout -b "nombre de la rama nueva"` esta nos ayuda a crear y movernos directamente a esa rama.

---

### Consideraciones antes de hacer un merge

---

#### No fast forward

Si tu separaste una rama en un cierto punto de la rama principal e hiciste commits en ambas ramas de igual cantidad, se crea un commit auxiliar de representacion a la fusion de ambas ramas.

![representacion grafica del fast forward](https://mascandobits.es/blog/wp-content/uploads/2021/03/Merge_Fast-Forward_vs_No_Fast-Forward.png)

#### Fast forward

Pongamos de ejemplo que tu modificaste una rama, la commiteaste e hiciste todo esto fuera de la principal, si a tu rama principal no se le hizo ningun commit desde la particion de la rama, entonces tu rama principal directamente salta al ultimo commit de la rama particionada.

 *TIP :* Si quieres que si o si se cree un commit de la fusion, aunque no sea un fast forward, entonces puedes usar el siguiente comando `git merge --no-ff "nombre de la rama"` de esta manera si gusta puede tener un mejor registro de las fusiones.

 ---

 ## Para tomar en cuenta 
 
 ---

 ### *Comando :*`git log --oneline --graph --all` *|Historial|*

 Te apoyara a la hora de necesitar ver todos tus commits, tus ramas, tu apuntador, comando de gran ayuda para el seguimiento.

 *No olvidar que debes estar en la rama a la que quieres que se fusione otra rama.*

 *Utiliza el `git status` recurremente para dar seguimiento.*

 *Si modificaste el mismo archivo/linea en distintas ramas, entonces git notara el conflicto y no te permitira hacer el merge, esto debes resolverlo manualmente.*

---

# GITHUB

---

## *¿Que acaso GIT y GITHUB no son lo mismo?*

Respuesta directa no, la explicacion es que GIT es un controlador de versiones que se puede manejar de manera local y GITHUB es un servidor en la nube que nos ayuda a tener un punto donde podemos subir todos nuestros repositorios locales, aparte de que su caracteristica principal es el trabajo en equipo.

## Repositorios remotos

Son repositorios hospedados en un servidor que sirven como punto de sincronizacion para diferentes repositorios locales.

GITHUB puedes encontrarlo en cualquier navegador y descargarlo en tu dispositivo, con una interfaz muy amistosa a la vista. Para dar tus primeros pasos en GITHUB debes crearte una cuenta, una vez hecho esto podras curiosear y darte cuenta de la importancia de GITHUB, la creacion de repositorios remotos, la cantidad inmensa de codigos disponibles, poder trabajar colaborativamente, son algunas ventajas.

---

## Repositorios remotos en github

### Crea tu primer repositorio remoto

1. Dale al boton "*create repository*

![Create repository](https://www.programacionfacil.org/images/cursos/git_github/github_crear_repositorio.png)

2. Escribe el nombre de tu repositorio.
3. Selecciona si prefieres que sea publico o privado.
4. Marcar si gusta el archivo README(aqui puede hacer un informe de lo que necesite explicar).
5. Marcar si gusta el archivo gitignore(Nos ayuda a ocultar archivos que no utilizaremos).
6. Selecciona la licencia, la licencia indica el uso, modificacion o distribucion sobre tu codigo.

![Tutorial de creacion de repositorio](https://programacionfacil.org/images/cursos/git_github/github_create_repository.png)

---

## Configuracion del repositorio remoto

---

### *Comando :*`git remote add origin <direccion de tu repositorio` *|enlace|*

Esto nos permitira conectar el repositorio local y el repositorio remoto, dandole el nombre de `origin` al servidor remoto.

### *¿Que direccion colocar?*

Se nos presentaran 3 opciones.- HTTPS, SSH y Github CLI

![Direccion del repositorio remoto](https://juncotic.com/wp-content/uploads/2021/03/github-clone.png)

La mas recomendable es SSH.

---


## Configuracion direccion HTTPS y SSH

Seguido de conectar los servidores, necesitamos seguir ciertos pasos para las Keys.

### Configuracion de direccion HTTPS

1. Colocamos el comando `git push -u origin main/master` seguido de esto nos saldra.-

```

Username for 'https://github.com': wartervsa   
Password for 'https://wartervsa@github.com': 

```
2. Username, colocas el nombre que gustes para identificarte.
3. Ahora viene lo importante, necesitas dirigirte a Github.
4. Presiona tu perfil(derecha superior).
5. Entra a las configuraciones(settings).
6. Baja al final de las opciones de la izquierda y dale a `<>Developer settings` .
7. Continua con `Personal access tokens` y dale a `Tokens(clasic)`.
8. Presiona `Generate new Token`, selecciona el clasico.
9. Escribe tu nota, selecciona la fecha de expiracion y escoge como basico repo, listo ya tienes tu llave.

Ahora copias la llave a Password ya estaria, esto te pedira cada vez que hagas un pull o fetch o push.

### Configuracion de direccion SSH

1. Primero nos aseguramos de tener o no una llave SSH, en la terminal con el comando `ls ~/.ssh/id_ed25519.pub`
Te aseguras si lo tienes o no.

2. Si no la tienes es hora de crearla, coloca el comando `ssh-keygen -t ed25519 -C "tucorreo@example.com"` 
Le das enter a todo, hay una parte que te dice sobre agregar *passphrase* si no quieres que te pregunte cada vez por tu contraseña entonces dale enter, enter y enter.

3. Ahora añadimos esta clave SSH a github, nos dirigimos al sitio https://github.com/settings/keys 

4. Seleccionamos `New SSH key`, agregar tu titulo de la llave y en *key* colocamos la llave 

5. La llave la conseguimos con el comando `cat ~/.ssh/id_ed25519.pub` y comienza desde *ssh...* seguido de esto copias hasta antes de tu correo, lo pegas en key y ya estaria.

Con esto ya podras hacer todo de forma segura y comoda.






