# Git

---

Es un software de control de versiones, se creo pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un gran número de archivos de código fuente.

### Cómo instalar Git

---

##### Distribución basada en Debian \(Ubuntu, por ej\)

```
apt-get install git
```

###### 

##### Distribución basada en Fedora

```
yum install git-core
```

###### 

##### En Mac

```
http://sourceforge.net/projects/git-osx-installer/
```

###### 

##### En Windows

```
https://git-scm.com/download/win
```

# Ordenes básicas

Para añadir un fichero o varios al control de versiones

```
git add [ <Nombre-del-fichero> o una expresión regular ] 
```

Para confirmar los cambios realizados

```
git commit -m "Nombre del commit"
```

Mostrar el estado actual de la rama , con los cambios que hay que guardar

```
git status
```

Respecto a las ramas

* Listar todas las ramas locales:

  `git branch`

* Listar tanto las ramas locales como las remotas

  `git branch -a`

* Crear una nueva rama

  `git branch <Nombre-de-rama>`

* Eliminar una rama

  `git branch -d <Nombre-de-rama>`

Para irnos a una rama

```
git checkout <Nombre-de-rama>
```

Para guardar los cambios desde la rama locar "origin" a la rama "Nombre-de-rama"

```
git push origin <Nombre-de-rama>
```

Para traer a local los cambios realizados en el repositorio remoto

```
git fetch
```

Mezcla en la rama en la que te encuentras parado, los cambios de la rama "Nombre-de-rama"

```
git merge <Nombre-de-rama>
```

Unifica los comando fetch y merge en un único comando respecto a un repositorio a la rama local

```
git pull <Nombre-de-rama-remota>
```

# GitHub

---

Github es una plataforma de desarrollo colaborativo para alojar proyectos utilizando el sistema de control de versiones Git. Utiliza un framework llamado Ruby on Rails creado por GitHub, Inc.

El primer paso para acceder a GitHub es crear una cuenta.

![](/assets/githubjoin.png)

A continuación se adjunta el enlace que  lleva directamente a la creación de una cuenta en GitHub:

[https://github.com/join?source=header-home](Crea tu cuenta de GitHub aquí)

