# Gabriel Méndez

# Repositorios de Ejercicios de Forty-Git.

## Trabajo en local.

### 1. Inicializa un nuevo repositorio Git en una carpeta llamada "forty" y agrega los archivos proporcionados en el aula virtual.

```bash
git init 
```



### 2. Renombra la rama master a main

```bash
git branch -M main
```



### 3. Haz que los ficheros README.txt , LICENSE.txt y passwords.txt sean ignorados por el control de versiones

```bash
touch .gitignore
nano .gitignore
```

<img src="../Forty/images/local/Ejercicio 1-3.png" style="zoom: 67%;" />

<img src="../Forty/images/local/Ejercicio 3.png" style="zoom:50%;" />

### 4. Crea el archivo passwords.txt . Comprueba que el control de versiones lo ignora

```bash
touch passwords.txt
git ls-files --others -i --excluda-standard
```

<img src="../Forty/images/local/Ejercicio 4.png" style="zoom: 67%;" />





### 5. Crea una rama llamada "feature-content" . Muévete a esa rama. Cambia, en la línea 3477, el font-size por 1.5em en el archivo main.css . Confirma cambios y haz commit. Muestra los logs de la forma más gráfica posible.

```bash
git branch feature-content
git checkout feature-content
cd assets/css
nano main.css
cd ../../
git add .
git commit -m "font-size linea 3477 modificado"
```



<img src="../Forty/images/local/ejercicio 5-1.png" style="zoom:67%;" />

<img src="../Forty/images/local/ejercicio 5-2.png" style="zoom:67%;" />



### 6. Elimina el archivo "passwords.txt" en la carpeta forty . Verifica el estado del repositorio. ¿Hay cambios pendientes?

```bash
rm passwords.txt
git status
```



<img src="../Forty/images/local/Ejercicio 6.png" style="zoom:67%;" />



### 7. Crea un nuevo archivo llamado " about.html ", partiendo del archivo generic.html y agrégalo al repositorio, haz un nuevo commit.

```bash
touch about.html
git add .
git commit -m "about view añadida"
```



<img src="../Forty/images/local/Ejercicio 7.png" style="zoom:67%;" />

### 8. Cambia a la rama main . Examina los logs del repositorio de forma gráfica.

```bash
git checkout main
git log --graph --all
```



<img src="../Forty/images/local/Ejercicio 8.png" style="zoom:67%;" />

### 9. Modifica algo en el archivo generic.html , comprueba que hay cambios, y realiza otro commit. Examina los logs del repositorio de forma gráfica.

```bash
nano generic.html
git status
git add .
git commit -m "generic.html modificado"
git log --graph --all
```



<img src="../Forty/images/local/Ejercicio 9.png" style="zoom:67%;" />

### 10. Modifica algo en el fichero elements.html . Confirma los cambios, pero no hagas commit.

```bash
nano elements.html
```



<img src="../Forty/images/local/Ejercicio 10.png" style="zoom:67%;" />

### 11. Mira las diferencias de elements.html . Los cambios no nos gustan, deshaz los cambios de elements.html. Comprueba que no hay cambios pendientes.

```bash
git status
git diff elements.html
git restore elements.html
git status
```



<img src="../Forty/images/local/Ejercicio 11-1.png" style="zoom:67%;" />

### 12. Muestra las diferencias entre dos ramas.

```bash
git diff main..feature-content
```



<img src="../Forty/images/local/Ejercicio 12.png" style="zoom:67%;" />

### 13. Fusiona la rama "feature-content" con la rama principal (main). Muestra los logs del repositorio de una forma gráfica y completa

```bash
git checkout main
git merge feature-content
```



<img src="../Forty/images/local/Ejercicio 13.png" style="zoom:67%;" />

### 14. Crea una nueva rama llamada " hotfix " y en ella, corrige un error crítico en el archivo "index.html". (Por ejemplo, añade el enlace a la nueva página about.html)

```bash
git checkout -b hotfix
nano index.html
git commit -m "About link fixed"
```



<img src="../Forty/images/local/Ejercicio 14.png" style="zoom:67%;" />

### 15. Fusiona la rama "hotfix" con la rama principal y verifica el historial de commits de forma que se vean todas las ramas gráficamente. ¿Borrarías la rama hotfix ? ¿En qué caso? ¿Cómo?

```bash
git checkout main
git merge hotfix
git log --graph --all
```



<img src="../Forty/images/local/Ejercicio 15.png" style="zoom:67%;" />

### 16. Muestra el historial de cambios limitado a los últimos 3 commits

```bash
git log -3
```



<img src="../Forty/images/local/Ejercicio 16.png" style="zoom:67%;" />

### 17. Etiqueta el commit actual como "v1.0" y muestra las etiquetas existentes.

```bash
git tag v1.0
git tag
```



<img src="../Forty/images/local/Ejercicio 17.png" style="zoom:67%;" />




## Trabajo en Remoto

### 1. Sube al remoto los ficheros de tu repositorio local.

```bash
git remote add origin https://github.com/GabriMF/Forty.git
git push origin main
```



<img src="../Forty/images/remoto/Ejercicio 1.png" style="zoom:67%;" />

### 2. En local, crea una rama 'feature-head'. Cambia el título en la sección head de index.html , borra los comentarios del head , o previos, también. Confirma y sube los cambios al remoto

```bash
git branch feature-head
git checkout feature-head
nano index.html
git add .
git commit -m "index title modified and comments removed"
git push origin feature-head
```



<img src="../Forty/images/remoto/Ejercicio 2.png" style="zoom:67%;" />

### 3. En remoto, crea una rama 'feature-articulo'. Duplica la página generic , nómbrala como articulo.html , y añade como contenido un artículo sobre Git. Confirma los cambios y realiza un commit. Muestra los commits del repositorio tal como se ven en GitHub.

<img src="../Forty/images/remoto/Ejercicio 3-1.png" style="zoom:50%;" />

<img src="../Forty/images/remoto/Ejercicio 3-2.png" style="zoom:50%;" />



<img src="../Forty/images/remoto/Ejercicio 3-3.png" style="zoom:50%;" />

<img src="../Forty/images/remoto/Ejercicio 3-4.png" style="zoom:50%;" />

### 4. En el repositorio local examina los cambios. Actualiza el repositorio con el remoto. Fusiona en 'main' las dos ramas 'feature'. Crea la etiqueta 'v2.0'. Muestra los logs, commits, etiquetas y ramas actuales, en local y en remoto

```bash
git checkout main
git merge feature-head
```

<img src="../Forty/images/remoto/Ejercicio 4-1.png" style="zoom: 67%;" />



```bash
git pull origin feature-articulo
git merge feature-articulo
```

<img src="../Forty/images/remoto/Ejercicio 4-2.png" style="zoom:67%;" />

```bash
git merge origin/feature-articulo
git tag v2.0
```

<img src="../Forty/images/remoto/Ejercicio 4-3.png" style="zoom:67%;" />

```bash
git log --graph --all
```

<img src="../Forty/images/remoto/Ejercicio 4-4.png" style="zoom:67%;" />



```bash
git branch
git tag
```

<img src="../Forty/images/remoto/Ejercicio 4-5.png" style="zoom:67%;" />



<img src="../Forty/images/remoto/Ejercicio 4-6.png" style="zoom:67%;" />

<img src="../Forty/images/remoto/Ejercicio 4-7.png" style="zoom:67%;" />



### 5. En tu copia local, crea una rama nueva . En la rama nueva, cambia los enlaces de la página index.html para que apunten correctamente a la nueva página articulo.html . Confirma los cambios.

```bash
git branch feature-linksIndex
git checkout feature-linksIndex
nano index.html
git add .
git commit -m "Link to articulo.html created"
```

<img src="../Forty/images/remoto/Ejercicio 5.png" style="zoom:67%;" />

### 6. Muestra los logs de forma que se vean las ramas en tu copia local.

```bash
git checkout main
git log --graph --all
```



<img src="../Forty/images/remoto/Ejercicio 6.png" style="zoom:67%;" />

### 7. Te gusta el resultado de los cambios. Incorpora los cambios de la rama nueva a la principal.

```bash
git merge feature-linksIndex
```

<img src="../Forty/images/remoto/Ejercicio 7.png" style="zoom:67%;" />

### 8. Sube los cambios al remoto borrando la rama nueva , si es necesario. Comprueba primero con un comando en local, las ramas que hay en el repositorio remoto.

```bash
git fetch
git branch -r
git push origin main
```

<img src="../Forty/images/remoto/Ejercicio 8.png" style="zoom:67%;" />

### 9. Muestra en local los cambios en el archivo index.html entre la versión actual y la anterior.

```bash
git diff HEAD^ HEAD -- index.html
```

<img src="../Forty/images/remoto/Ejercicio 9.png" style="zoom:67%;" />

### 10. En el repositorio en GitHub, navega hasta el archivo index.html y selecciona la opción "History".

<img src="../Forty/images/remoto/Ejercicio 10.png" style="zoom:67%;" />

