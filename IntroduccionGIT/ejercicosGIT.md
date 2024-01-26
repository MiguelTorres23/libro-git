## Ejercicio 1. Repositorio Local.

Realizar un primer commit en el que añades dos ficheros .txt Uno con tu nombre y otro con el nombre actividades; por ejemplo (sabela.txt y actividades.txt). En el primero introduce una breve descripción de ti y en el segundo añade alguna de tus aficciones (leer, hacer deporte, etc.).

```bash
git init
```

```bash
Inicializado repositorio Git vacío en /home/vagrant/.git/
```

```bash
echo "Descripción: Soy miguel tengo 22 años y estoy haciendo el ciclo superior de DAW" > miguel.txt
nano miguel.txt
```

```bash
La descripcion que ponga dentro, salgo y guardo
```

```bash
echo "Tus aficiones: Me encanta hacer deporte sobre todo baloncento y atletismo" > actividades.txt
nano actividades.txt
```


**Para hacer el commit**
```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$  git add actividades.txt
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git add miguel.txt

Y para subirlo
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git commit -m "dfsd"
```
**Realizar otro commit modificando el primer .txt añadiendo una nueva línea, comentando por qué estás en este ciclo.**

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ nano miguel.txt
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git add miguel.txt
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git commit -m "hola" 
[master e55f722] hola
 1 file changed, 2 insertions(+)
 ```


**Crear una carpeta con dos ficheros, todo desde línea de comandos.**

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ mkdir carpeta
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ cd carpeta
vagrant@lubuntu-vagrant:~/Desktop/repositorio/carpeta$ nano vigo
vagrant@lubuntu-vagrant:~/Desktop/repositorio/carpeta$ nano cangas
 ```


**Realizar otro commit con las siguientes modificaciones:**


1 Eliminar del segundo fichero una de tus aficciones.
Ignora la carpeta con los dos ficheros.

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ nano actividades.txt 
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git add actividades.txt
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git commit -m "borrado de una actividad" 
[master 0311631] borrado de una actividad
 1 file changed, 1 insertion(+), 2 deletions(-)
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ 
 ```

**2 Realiza un checkout para volver a las primeras versiones de los ficheros .txt (el primer commit).**

La herramienta más básica y potente para hacer esto es el comando git log.

```bash
$ git log
 ```

Para revertir los cambios tenemos que copiar los 10 primeros números del commit donde está la versión de nuestro documento que nos interesa (en este caso mensaje inicial) y pegarlos juntos al comando git 
checkout

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git checkout 66c134a3f1
Nota: cambiando a '66c134a3f1'.
 ```
Y la comprobacion de que esta bien

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ git log
commit 66c134a3f16fc2e5f8c2df6e70da0bf3ece5a077 (HEAD)
Author: Miguel Angel Torres Moreno <a23migueltm@iessanclemente.net>
Date:   Mon Jan 15 09:16:53 2024 +0100
 ```


 ## Ejercicio 2. Trabajando con repositorios locales
 
**Crear un repositorio nuevo (todo desde línea de comandos) con el nombre pagina_web y muestra su contenido desde línea de comandos.**

```bash
mkdir pagina_web
vagrant@lubuntu-vagrant:~/Desktop/repositorio$ cd pagina_web
vagrant@lubuntu-vagrant:~/Desktop/repositorio/pagina_web$ git init
```

**Comprueba y explica el estado del repositorio.**
```bash
ls -la
```
**Crear un fichero index.html con el siguiente contenido :**

```bash
echo '<html>\n\t<head>\n\t\t<title>Página de tu_nombre</title>\n\t</head>\n\t<body>\n\t    Página en la que vamos a mostrar un listado de ciudades/países que visitar. \n\t</body>\n</html>' > index.html
```
**Realizar un commit con el mensaje “Primera página html”.**

```bash
git add index.html
git commit -m "Primera página html"
```
**Muestra y explica el estado del repositorio.**

```bash
git status
```

**Cambiar la página web para que muestre en un listado 3 ciudades que te gustaría visitar:**

```bash
echo '<html>\n\t<head>\n\t\t<title>Página de tu_nombre</title>\n\t</head>\n\t<body>\n\t    Página en la que vamos a mostrar un listado de ciudades que visitar. \n\t    <ul>\n\t        <li>Oslo</li>\n\t        <li>Venecia</li>\n\t    </ul>\n\t</body>\n</html>' > index.html
```
**Hacer un commit de los cambios, con el mensaje “Añadidas 3 ciudades que visitar”.**

```bash
vagrant@lubuntu-vagrant:~/Desktop/repositorio/pagina_web$ git commit -m "Añadidas 3 ciudades que visitar"
```
**Muestra el historial de commits del repositorio**

```bash
git log
```

**Crea una carpeta por cada ciudad que hayas indicado en el listado anterior. Introduce dentro de cada carpeta un fichero index.html con información por cada ciudad. Por ejemplo:**

```bash
mkdir Oslo Venecia
```
**Hacer un commit de los cambios, con el mensaje “Añadida información sobre las ciudades a visitar”.**

```bash
git add .
git commit -m "Añadida información sobre las ciudades a visitar"
```
**Volver a mostrar el historial de cambios.**
```bash
git log
```

## Ejercicio 3. Fundamentos de GIT
**Crear un repositorio nuevo con el nombre libro y mostrar su contenido.**
```bash
mkdir libro
cd libro
git init
```
**Comprueba el estado del respositorio.**
```bash
git status
```
**Crear un fichero indice.txt con el siguiente contenido:**
Capitulo 1: Introducción
Capitulo 2: Los tres cerditos
Capitulo 3: Caperucita roja 

```bash
nano 'Capitulo 1: Introducción\nCapitulo 2: Los tres cerditos\nCapitulo 3: Caperucita roja' > indice.txt
```

**Realizar un commit con el mensaje “Añadido índice del libro”**
```bash
git add indice.txt
git commit -m "Añadido índice del libro"
 
```

**Comprueba y explica el estado del repositorio.**
```bash
git status
```

**Cambiar el índice.txt para que contenga lo siguiente:**
Capitulo 1: Introducción
Capitulo 2: Los tres cerditos
Capitulo 3: Caperucita roja 
Capitulo 4: La bella y la bestia 

```bash
echo -e 'Capitulo 1: Introducción\nCapitulo 2: Los tres cerditos\nCapitulo 3: Caperucita roja\nCapitulo 4: La bella y la bestia' > indice.txt
```

**Hacer un commit de los cambios con el mensaje “Añadido 4: La bella y la bestia”.**

```bash
git add indice.txt
git commit -m "Añadido 4: La bella y la bestia"

```
**Comprueba el estado del repositorio.**

```bash
git status
```



**Crea la carpeta capítulos y dentro de ella el fichero capitulo2.txt con el siguiente texto:**
Y el lobo sopló y sopló y la casa derribó. 

```bash
mkdir capitulos
echo 'Y el lobo sopló y sopló y la casa derribó.' > capitulos/capitulo2.txt
```

**Hacer un commit con el mensaje “Añadido capitulo 2”**

```bash
git add .
git commit -m "Añadido capitulo 2"
```

**Volver a mostrar el historial de cambios.**

```bash
git log
```

**Crear el fichero capitulo3.txt en la carpeta capitulos con el siguiente texto:**

Abuelita qué ojos más grandes tienes.

```bash
echo 'Abuelita qué ojos más grandes tienes.' > capitulos/capitulo3.txt
```

**Ver el estado del repositorio de forma abreviada e indicar qué significa cada letra.**

```bash
git add .
git commit -m "Añadida información sobre las ciudades a visitar"
```

**Modificar el índice.txt añadiendo “Capitulo 5: Forzen”**

```bash
echo 'Capitulo 1: Introducción\nCapitulo 2: Los tres cerditos\nCapitulo 3: Caperucita roja\nCapitulo 4: La bella y la bestia\nCapitulo 5: Frozen' > indice.txt
```

**”Subir los cambios al repositorio ingorando el capitulo3.txt**

```bash
echo 'capitulos/capitulo3.txt' > .gitignore
git add .
git commit -m "Añadido Capitulo 5: Frozen"
```

```bash
[master 155bc02] Añadido Capitulo 5: Frozen
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
```

**Modificar el fichero para que se ignoren todos aquellos ficheros que comiencen por _ a excepción del fichero _ayuda.txt (ya no se debe ignorar capitulo3.txt)**

```bash
echo -e '_*\n!_ayuda.txt' > .gitignore
```

**Crear un fichero _logs.txt con el siguiente contenido:**
Fichero para almacenar logs

```bash
echo 'Fichero para almacenar logs' > _logs.txt
```

**Crear un fichero _ayuda.txt con el siguiente contenido**
Fichero de ayuda. 

```bash
echo 'Fichero de ayuda.' > _ayuda.txt
```

**Preparar todo con git add **

**Hacer un commit de los cambios con el mensaje “Añadido capitulo 2”. Comprobar/explicar qué se sube al repositorio.**
git commit -m "Añadido capitulo 2"

**Modificar el fichero capitulo2.txt (elimina lo que había antes).**
 Caperucita iba por el bosque 
con su capa roja 

```bash
echo -e 'Caperucita iba por el bosque \ncon su capa roja' > capitulos/capitulo2.txt
```

**Ver y explicar qué ha cambiado y aún no has preparado.**

```bash
git diff
```

**Hacer un commit con el mensaje “Capitulo 2 modificado”**

```bash
git add .
git commit -m "Capitulo 2 modificado"
```

**Vuelve a modificar el capitulo con el siguiente contenido:**
Caperucita iba por el bosque con su capa roja 
cuando llegó a casa de su abuela le dijo 
"Abuela qué ojos más grandes tienes"

```bash
echo -e 'Caperucita iba por el bosque con su capa roja \ncuando llegó a casa de su abuela le dijo \n"Abuela qué ojos más grandes tienes"' > capitulos/capitulo2.txt
```

**Prepara tus cambios y comprueba qué ha cambiado con la última instantánea confirmada.**

```bash
git add capitulos/capitulo2.txt
git diff --cached
```
```bash
iff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
index c8bd280..ec80859 100644
--- a/capitulos/capitulo2.txt
+++ b/capitulos/capitulo2.txt
@@ -1,2 +1,3 @@
-Caperucita iba por el bosque 
-con su capa roja
+Caperucita iba por el bosque con su capa roja 
+cuando llegó a casa de su abuela le dijo 
+"Abuela qué ojos más grandes tienes"
vagrant@lubuntu-vagrant:~/libro$ 
```

**Elimina del repositorio el fichero _ayuda.txt**

```bash
git rm _ayuda.txt
git commit -m "Eliminado _ayuda.txt del repositorio"
```

**Cambia el nombre del fichero indice.txt por indice_libros.txt y sube los cambios.**

```bash
git mv indice.txt indice_libros.txt
git commit -m "Cambiado nombre de indice.txt a indice_libros.txt"
```

**Cambia el mensaje del último commit.**

```bash


git commit -m "ultimo"
```

