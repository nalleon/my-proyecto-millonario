# my-proyecto-millonario
Practica de ETS: Manipulación Avanzada en Git (trabajo con tags y ramas).
Nabil León Álvarez - 1ºDAM

## Índice
* [Ejercicio 1](#ejercicio-1)


## Iniciación de la tarea
* Crear un repositorio en vuestro GitHub llamado my-proyecto-millonario.
* Clonar vuestro repositio en local.
* Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md. __El README.md ha sido añadido durante la creación del repositorio, por lo tanto este paso no es realizado.__
* Añadir al README.md los comanddos utilizados hasta ahora y hacer un coomit inicial con el mensaje commit inicial.
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

**Pregunta:** el fichero y el directorio privado debe de subir al repositorio si se encuentra añadido al fichero .gitingnore. [Si/No]. Justifica tu respuesta en el fichero README.md.

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
**Respuesta:**

## Añadir fichero 1.txt
* Añadir fichero 1.txt al repositorio local.

**Pregunta:** Si he ejecutado las acciones add y commit, que realiza cada una sobre el/los ficheros. Justifica tu respuesta en el fichero README.md.

Operaciones a realizar:
```code
touch 1.txt
git add .
git commit -m "añadido 1.txt"
```

Salida:
```code
```