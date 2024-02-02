## Ejercicio Ramas remotas

**Crear una nueva rama llamada autoria y cambiate a ella.**
```bash
git branch autoria
git checkout autoria
```
**Añadir el nombre del usuario (a22…) y su correo al fichero autores.txt.**
```bash
nano autores.txt
```
**Hacer un commit con el mensaje.**
```bash
git add autores.txt
git commit -m "usuario y correo en autores.txt"
```
```bash
[autoria 8c05163] usuario y correo en autores.txt
1 file changed, 1 insertion(+)
```
**Subir los cambios de la rama autoria al repositorio remoto en GitHub. Crea un diagrama como los vistos en teoría que hagan un resumen de tu repositorio hasta este momento.**

![ramas](./img/Captura%20de%20pantalla%202024-02-02%20121007.png)