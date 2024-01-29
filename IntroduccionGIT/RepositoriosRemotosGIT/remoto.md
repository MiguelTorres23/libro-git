
## REPOSITORIOS REMOTOS GIT


### Para realizar las pruebas con los repositorios remotos utilizaremos el GitHub, por lo que, lo primero que tenéis que hacer es daros de alta en la plataforma con el correo del iessanclemente.net.


**Crea un repositorio en GitHub con el nombre libro-git. Añádelo como url remota en nuestro repositorio local de libro creado en el ejercicio anterior.**

```bash
git remote add origin https://github.com/MiguelTorres23/libro-git.git

git push -u origin master

```

**Añade todo lo que tenemos que el repositorio libro al repositorio remoto y comprueba que los cambios están subidos correctamente.**

```bash
git add .
git commit -m 
git push origin master

```

### Colaborando con repositorios

**Colabora en el repositorio remoto de otro compañero. Clona su repositorio. Añade el fichero autores.txt que contenga tu nombre y tu correo electrónico. Haz un commit y sube los cambios al repositorio remoto de tu compañero.**

```bash
git clone "https://github.com/raquetm/libro-git.git"
Clonando en 'libro-git'...
remote: Enumerating objects: 37, done.
remote: Counting objects: 100% (37/37), done.
remote: Compressing objects: 100% (24/24), done.
remote: Total 37 (delta 4), reused 37 (delta 4), pack-reused 0
Desempaquetando objetos: 100% (37/37), 4.38 KiB | 224.00 KiB/s, listo.

cd "nombre que tenga el repositorio"           
```

### Resolviendo conflictos

**Cuando un compañero/a haya realizado el paso anterior en tu repositorio remoto, sincroníza tu repositorio en local. El resultado debe ser que en local debes tener ese fichero autores.txt.**
```bash
git pull origin master


```

**Modifica ese fichero, cambiando el nombre de tu compañero/a por el tuyo y añadiendo la fecha y la hora donde lo realizas. Sube los cambios al repositorio remoto.**

*Por ejemplo. Fichero autores.txt en repositorio local del propietario del repositorio remoto:*

*Sabela Sobrino*

*Ana Pérez*

```bash
git add autores.txt
git commit -m
git push origin master
```

**Al mismo tiempo, avisa a tu compañero/a para que, en su repositorio local, vuelva a modificar el fichero autores.txt añdiendo tu nombre en un línea nueva, la fecha y la hora así como el lugar donde se realiza el ejercicio. Una vez modificado, debe subir los cambios a remoto.**



*Por ejemplo. Fichero autores.txt en repositorio local del colaborador del repositorio remoto:*

*Sabela Sobrino*

*Ana Pérez*

```bash


```

**Resolver los conflictos que se puedan producir en ambos repositorios.**

```bash


```