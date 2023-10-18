# my-proyecto-millonario
Practica de ETS: Manipulación Avanzada en Git (trabajo con tags y ramas).
Nabil León Álvarez - 1ºDAM

## Índice
* [Iniciacion tareas](#iniciación-de-la-tarea)
* [Ignorar archivos](#ignorar-archivos)
* [Añadir fichero 1.txt](#añadir-fichero-1txt)
* [Tag v0.1](#tag-v01)
* [Crear una rama v0.2](#crear-una-rama-v02)
* [Añadir fichero 2.txt](#añadir-fichero-2txt)
* [Crear rama remota v0.2](#crear-rama-remota-v02)
* [Merge directo](#merge-directo)
* [Merge con conflicto y arreglar conflicto](#merge-con-conflicto-y-arreglar-conflicto)
* [Listado de ramas](#listado-de-ramas)
* [Borrar rama](#borrar-rama)
* [Listado de cambios](#listado-de-cambios)


## Iniciación de la tarea
* Crear un repositorio en vuestro GitHub llamado my-proyecto-millonario.
* Clonar vuestro repositio en local.
* Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md. __El README.md ha sido añadido durante la creación del repositorio, por lo tanto este paso no es realizado.__
* Añadir al README.md los dos utilizados hasta ahora y hacer un coomit inicial con el mensaje commit inicial.
* Subir los cambios al repositorio remoto.

Operaciones realizadas:
```code
git clone git@github.com:alumno-XXX/my-proyecto-millonario.git
touch README.md
git add .
git commit -m "commit inicial"
git push origin master
```

Salida:
```code
dam@a108pc11:~$ git clone https://github.com/nalleon/my-proyecto-millonario
Clonando en 'my-proyecto-millonario'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Recibiendo objetos: 100% (3/3), listo.
dam@a108pc11:~$ cd my-proyecto-millonario
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Commit inicial."
[main 12fbd70] Commit inicial.
 1 file changed, 17 insertions(+), 1 deletion(-)
dam@a108pc11:~/my-proyecto-millonario$ 
dam@a108pc11:~/my-proyecto-millonario$ git push origin main
Username for 'https://github.com': nalleon
Password for 'https://nalleon@github.com': 
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 551 bytes | 551.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
To https://github.com/nalleon/my-proyecto-millonario
   7f6b0a0..12fbd70  main -> main
```

## Ignorar archivos
* Crear en el repositorio local un fichero llamado privado.txt.
* Crear en el repositorio local una carpeta llamada privada.
* Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

Operaciones a realizar:
```code
touch privado.txt
mkdir privada
echo "privado.txt" >> .gitignore
echo "/privada" >> .gitignore
git add .
git commit -m "añadido fichero .gitignore"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ touch privado.txt
dam@a108pc11:~/my-proyecto-millonario$ mkdir privada
dam@a108pc11:~/my-proyecto-millonario$ echo "privado.txt" >> .gitignore
dam@a108pc11:~/my-proyecto-millonario$ echo "/privada" >> .gitignore
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Añadido fichero .gitignore."
[main fb30080] Añadido fichero .gitignore.
 2 files changed, 50 insertions(+), 2 deletions(-)
 create mode 100644 .gitignore
dam@a108pc11:~/my-proyecto-millonario$ 

```
**Pregunta:** el fichero y el directorio privado debe de subir al repositorio si se encuentra añadido al fichero .gitingnore. [Si/No]. Justifica tu respuesta en el fichero README.md.

**Respuesta:** No, el fichero .gitignore funciona de manera que independiene a que si el archivo es privado o no, este no sera subido a git y se vera desde el repositorio en la nube. 

## Añadir fichero 1.txt
* Añadir fichero 1.txt al repositorio local.



Operaciones a realizar:
```code
touch 1.txt
git add .
git commit -m "añadido 1.txt"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ touch 1.txt
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Añadido 1.txt"
[main 96bb08f] Añadido 1.txt
 2 files changed, 40 insertions(+), 3 deletions(-)
 create mode 100644 1.txt
```

**Pregunta:** Si he ejecutado las acciones add y commit, que realiza cada una sobre el/los ficheros. Justifica tu respuesta en el fichero README.md.

**Respuesta:**  La acción add se utiliza para seleccionar los cambios que se van a realizar en un fichero previamente a subirse a la nube, este además se ve complementa con la acción commit, la cual confirma los cambios a realizar (al añadir -m podemos incluir un comentario relacionado).


## Tag v.01
* Crear un tag v0.1.
* Subir los cambios al repositorio remoto.


Operaciones a realizar:

```code
git tag v0.1
git push --tag origin master
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git tag v0.1
dam@a108pc11:~/my-proyecto-millonario$ git push --tag origin main
Username for 'https://github.com': nalleon
Password for 'https://nalleon@github.com': 
Enumerando objetos: 10, listo.
Contando objetos: 100% (10/10), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (6/6), listo.
Escribiendo objetos: 100% (8/8), 1.87 KiB | 1.87 MiB/s, listo.
Total 8 (delta 1), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/nalleon/my-proyecto-millonario
   12fbd70..96bb08f  main -> main
 * [new tag]         v0.1 -> v0.1
dam@a108pc11:~/my-proyecto-millonario$ 
```
**Pregunta:** ¿Qué es un tag sobre un repositorio git, en nuestro caso Github?. Justifica tu respuesta en el fichero README.md.

**Respuesta:** Los tags se utilizan (en nuestro caso en GitHub) para dejar una referencia/marca de versiones anteriores.

## Crear una rama v0.2
* Crear una rama v0.2.
* Posiciona tu carpeta de trabajo en esta rama.

Operaciones a realizar:
```code
git branch v0.2
git checkout v0.2
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git branch v0.2
dam@a108pc11:~/my-proyecto-millonario$ git checkout v0.2
M	README.md
Cambiado a rama 'v0.2'
```

## Añadir fichero 2.txt
* Añadir un fichero 2.txt en la rama v0.2.

Operaciones a realizar:
```code
touch 2.txt
git add .
git commit -m "añadido 2.txt"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ touch 2.txt
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Añadido 2.txt"
[v0.2 5432118] Añadido 2.txt
 2 files changed, 86 insertions(+), 5 deletions(-)
 create mode 100644 2.txt

```

**Pregunta:** Cuando estamos trabajando con ramas, cual es su fin, y sentido en organizaciones pequeñas/medianas/grandes. Justifica tu respuesta en el fichero README.md.

**Respuesta:** Las ramas son uno de los pilares fundamentales de la organización al trabajar en un proyecto de Git, ya que permiten el aislamiento de cambios para llevar acabo correciones o añadir cambios. Las organizaciones pequeñas son principalmente utilizadas para evitar conflictos mientras que las medianas tienen un uso de cara a la gestión de multiples versiones, y las grandes se encargan de la cordinación de proyectos complejos.

## Crear rama remota v0.2
* Subir los cambios al reposiorio remoto.

Operaciones a realizar:
```code
git push origin v0.2
```

Salida:

```code
dam@a108pc11:~/my-proyecto-millonario$ git push origin v0.2
Username for 'https://github.com': nalleon
Password for 'https://nalleon@github.com': 
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 977 bytes | 977.00 KiB/s, listo.
Total 3 (delta 2), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'v0.2' on GitHub by visiting:
remote:      https://github.com/nalleon/my-proyecto-millonario/pull/new/v0.2
remote: 
To https://github.com/nalleon/my-proyecto-millonario
 * [new branch]      v0.2 -> v0.2
```

## Merge directo
* Posicionarse en la rama master/main según sea tu rama principal.
* Hacer un merge de la rama v0.2 en la rama master/main.

Operaciones a realizar:
```code
git checkout master
git merge v0.2 -m "merge v0.2 sin conflictos"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git checkout main
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
dam@a108pc11:~/my-proyecto-millonario$ git merge v0.2 -m "merge v0.2 sin conflictos"
Actualizando 96bb08f..8649519
Fast-forward (no commit created; -m option ignored)
 2.txt     |   0
 README.md | 145 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++---
 2 files changed, 140 insertions(+), 5 deletions(-)
 create mode 100644 2.txt
```

**Pregunta:** Se tendrían que producir conflictos en esta acción. [Si/No] Justifica tu respuesta en el fichero README.md.

**Respuesta:** No se produjo ningún conflicto al fusionar las ramas. Los cambios y contenidos de la rama principal main y la rama v0.2 coinciden.


## Merge con conflicto y arreglar conflicto
* En la rama maste/main poner Hola en el fichero 1.txt y hacer commit. 

Operaciones a realizar:
```code
git checkout master
echo "Hola" >> 1.txt
git add .
git commit -m "hola en 1.txt"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git checkout main
M	README.md
Ya en 'main'
Tu rama está adelantada a 'origin/main' por 2 commits.
  (usa "git push" para publicar tus commits locales)
dam@a108pc11:~/my-proyecto-millonario$ echo "Hola" >> 1.txt
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Hola en 1.txt"
[main cb6dcbe] Hola en 1.txt
 2 files changed, 39 insertions(+), 1 deletion(-)
```
* Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

Operaciones a realizar:
```code
git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"
```

Salida:
```code
am@a108pc11:~/my-proyecto-millonario$ echo "Adios" >> 1.txt
çdam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Adios en 1.txt"
[v0.2 58c1f05] Adios en 1.txt
 1 file changed, 1 insertion(+)
```
* Posicionarse de nuevo en la rama master/main y hacer un merge con la rama v0.2

Operaciones a realizar:
```code
git checkout master
git merge v0.2
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git checkout main
Cambiado a rama 'main'
Tu rama está adelantada a 'origin/main' por 4 commits.
  (usa "git push" para publicar tus commits locales)
dam@a108pc11:~/my-proyecto-millonario$ git merge v0.2
Auto-fusionando 1.txt
CONFLICTO (contenido): Conflicto de fusión en 1.txt
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
dam@a108pc11:~/my-proyecto-millonario$ vim 1.txt
No se ha encontrado la orden «vim», pero se puede instalar con:
apt install vim         # version 2:8.2.3995-1ubuntu2.12, or
apt install vim-tiny    # version 2:8.2.3995-1ubuntu2.12
apt install vim-athena  # version 2:8.2.3995-1ubuntu2.12
apt install vim-gtk3    # version 2:8.2.3995-1ubuntu2.12
apt install vim-nox     # version 2:8.2.3995-1ubuntu2.12
apt install neovim      # version 0.6.1-3
Solicite al administrador que instale uno de ellos.
dam@a108pc11:~/my-proyecto-millonario$ vi 1.txt
dam@a108pc11:~/my-proyecto-millonario$ vi 1.txt
dam@a108pc11:~/my-proyecto-millonario$ git checkout v0.2
1.txt: needs merge
error: necesitas resolver tu índice actual primero
dam@a108pc11:~/my-proyecto-millonario$ vi 1.txt
dam@a108pc11:~/my-proyecto-millonario$ git add .
dam@a108pc11:~/my-proyecto-millonario$ git commit -m "Arreglado merge en 1.txt"
[main f49d5e0] Arreglado merge en 1.txt
dam@a108pc11:~/my-proyecto-millonario$ 
```


## Listado de ramas
* Listar las ramas con merge y las ramas sin merge.

Operaciones a realizar:
```code
git branch --merged
git branch --no-merged
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git branch --merged
* main
  v0.2
dam@a108pc11:~/my-proyecto-millonario$ git branch --no-merged
dam@a108pc11:~/my-proyecto-millonario$ 
```

## Borrar rama
* Crear un tag v0.2
* Borrar la rama v0.2

Operaciones a realizar:
```code
git tag v0.2
git branch -d v0.2
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git tag v0.2
dam@a108pc11:~/my-proyecto-millonario$ git branch -D v0.2
Eliminada la rama v0.2 (era 58c1f05).
```

## Listado de cambios
* Listar los distintos commits con sus ramas y sus tags.

Operaciones a realizar:
```code
git config --global alias.list 'log --oneline --decorate --graph --all'
git list
```

Salida:
```code
dam@a108pc11:~/my-proyecto-millonario$ git config --global alias.list 'log --oneline --decorate --graph --all'
git list
*   f49d5e0 (HEAD -> main, tag: v0.2) Arreglado merge en 1.txt
|\  
| * 58c1f05 Adios en 1.txt
* | 1d15376 Actualización del README
* | cb6dcbe Hola en 1.txt
|/  
* 8649519 Actualización del README
* 5432118 (origin/v0.2) Añadido 2.txt
* 96bb08f (tag: v0.1, origin/main, origin/HEAD) Añadido 1.txt
* fb30080 Añadido fichero .gitignore.
* 12fbd70 Commit inicial.
* 7f6b0a0 Initial commit
```
