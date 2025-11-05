# Gabriel Méndez

# Repositorios de Ejercicios de Linux.

## Segundo Bloque


### 1. ¿En qué directorio se encuentran los ficheros de configuración del sistema?
    En el directorio /etc.


### 2. Para entrar en un sistema Linux hace falta...
    a. Nombre de usuario, contraseña y dirección IP
    b. Nombre de usuario y contraseña
    c. Únicamente una contraseña.
### Respuesta: 
    b. Nombre de usuario y contraseña

### 3. Muestra el contenido del directorio actual.

```bash
ls
```



<img src="../Repaso_Linux_2/images/Ejercicio 3.png" style="zoom:67%;" />


### 4. Muestra el contenido del directorio que está justo a un nivel superior.

```bash
ls ..
```



<img src="../Repaso_Linux_2/images/Ejercicio 4.png" style="zoom:67%;" />

### 5. ¿En qué día de la semana naciste?, utiliza la instrucción cal para averiguarlo.

```bash
sudo apt install ncal
cal 09 1998
```






<img src="../Repaso_Linux_2/images/Ejercicio 5.png" style="zoom:67%;" />

### 6. Muestra los archivos del directorio /bin

```bash
ls /bin
```




<img src="../Repaso_Linux_2/images/Ejercicio 6.png" style="zoom:67%;" />

### 7. Suponiendo que te encuentras en tu directorio personal (/home/nombre), muestra un listado del
contenido de /usr/bin...
    a. Con una sola línea de comando
    b. Moviéndote paso a paso por los directorios
    c. Con dos líneas de comandos.

```bash
ls /usr/bin
```



<img src="../Repaso_Linux_2/images/Ejercicio 7-a.png" style="zoom:67%;" />

```bash
cd ../../
cd usr
cd bin
ls
```



<img src="../Repaso_Linux_2/images/Ejercicio 7-b.png" style="zoom:67%;" />

```bash
cd /usr
ls bin
```



<img src="../Repaso_Linux_2/images/Ejercicio 7-c.png" style="zoom:67%;" />

### 8. Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva (con un solo comando).

```bash
ls -R /etc
```



<img src="../Repaso_Linux_2/images/Ejercicio 8.png" style="zoom:67%;" />



### 9. Muestra todos los archivos del directorio /usr/X11R6/bin ordenados por tamaño (de mayor a menor). Sólo debe aparecer el nombre de cada fichero, sin ninguna otra información adicional.

```bash
ls -S /usr/bin
```



<img src="../Repaso_Linux_2/images/Ejercicio 9.png" style="zoom:67%;" />



### 10. Muestra todos los archivos del directorio /etc ordenados por tamaño (de mayor a menor) junto con el resto de características, es decir, permisos, tamaño, fechas de la última modificación, etc. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

```bash
ls -lhS /etc
```



<img src="../Repaso_Linux_2/images/Ejercicio 10.png" style="zoom:67%;" />



### 11. Muestra todos los archivos del directorio /bin ordenados por tamaño (de menor a mayor). Sólo debe aparecer el tamaño y el nombre de cada fichero, sin ninguna otra información adicional. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

<img src="../Repaso_Linux_2/images/Ejercicio 11.png" style="zoom:67%;" />



### 12. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta absoluta

```bash
ls /
```



<img src="../Repaso_Linux_2/images/Ejercicio 12.png" style="zoom:67%;" />



### 13. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta relativa. Suponemos que el directorio actual es /home/elena/documentos.

```bash
ls ../../../
```



<img src="../Repaso_Linux_2/images/Ejercicio 13.png" style="zoom:67%;" />



### 14. Crea el directorio gastos dentro del directorio personal.

```bash
mkdir gastos
```



<img src="../Repaso_Linux_2/images/Ejercicio 14.png" style="zoom:67%;" />



### 15. ¿Qué sucede si se intenta crear un directorio dentro de /etc?

```bash
mkdir /etc/prueba
```



<img src="../Repaso_Linux_2/images/Ejercicio 15.png" style="zoom:67%;" />

Habria que utilizar el siguiente:

```bash
sudo mkdir /etc/prueba
```





### 16. Muestra el contenido del fichero /etc/fstab

```bash
cat /etc/fstab
```



<img src="../Repaso_Linux_2/images/Ejercicio 16.png" style="zoom:67%;" />



### 17. Muestra las 10 primeras líneas del fichero /etc/bash.bashrc

```bash
head -n 10 /etc/bash.bashrc
```



<img src="../Repaso_Linux_2/images/Ejercicio 17.png" style="zoom:67%;" />

### 18. Crea la siguiente estructura de directorios dentro del directorio de trabajo personal:

```bash
mkdir multimedia
cd multimedia
mkdir musica
mkdir video
mkdir presentaciones
mkdir imagenes
cd imagenes
mkdir personales
mkdir otras
```



<img src="../Repaso_Linux_2/images/Ejercicio 18.png" style="zoom:67%;" />

### 19. Crea un fichero vacío dentro del directorio musica, con nombre estilos_favoritos.txt

```bash
cd Música
touch estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 19.png" style="zoom:67%;" />



### 20. Utiliza tu editor preferido para abrir el fichero estilos_favoritos.txt e introduce los estilos de música que más te gusten. Guarda los cambios y sal.

```bash
nano /Música/estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 20-1.png" style="zoom:67%;" />

<img src="../Repaso_Linux_2/images/Ejercicio 20-2.png" style="zoom:67%;" />



### 21. Muestra todo el contenido de estilos_favoritos.txt

```bash
cat estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 21.png" style="zoom:67%;" />



### 22. Muestra las 3 primeras líneas de estilos_favoritos.txt

```bash
head -n 3 estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 22.png" style="zoom:67%;" />



### 23. Muestra la última línea de estilos_favoritos.txt

```bash
tail -n 1 estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 23.png" style="zoom:67%;" />



### 24. Muestra todo el contenido del fichero estilos_favoritos.txt excepto la primera línea. Se supone que no sabemos de antemano el número de líneas del fichero.

```bash
tail -n +2 estilos_favoritos.txt
```



<img src="../Repaso_Linux_2/images/Ejercicio 24.png" style="zoom:67%;" />