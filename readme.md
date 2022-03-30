# EJERCICIO DE CLASE 2

**Ejercicios básicos de MS-DOS**

## Ejercicio 1

---

1. **Crea la sigiente estructura de carpetas**

    ![Ejercicio 1](images/Screenshot%20from%202022-03-25%2019-21-03.png)

    Para crear directorios utilizamos el siguiente    commando:

    ```bat
    mkdir nombre_del_directorio
    ```

    Se podrá crear varios directorios al mismo tiempo de la sigiente manera:

    ```bat
    mkdir directorio1 directorio2/subdirectorio/subdirectorioN
    ```

    Así he creado la estructura de directorios indicada. He utilizado el comando `tree` para poder visualizar la estructura.

    ![Ejercicio 1](images/Screenshot%20from%202022-03-23%2017-11-58.png)

2. **Sitúate en la carpeta TABLAS:**

    Seguimos la estructura de directorios

    ``` bat
        cd ./PARTE1/APLI/EXCEL/TABLAS/
    ```

3. **Vuelve a la carpeta raíz.**

    ```bat
        cd ../../..
    ```

4. **Muestra el contenido de la carpeta PROG.**

    Para ver el contenido de la carpeta PROG lanzamos el comando `cd` para movernos al directorio PROG y después mostramos el contenido con el comando `ls`.

    ```bat
    cd ./PARTE1/PROG && ls
    ```

5. **Borra la carpeta PASCAL**

    Para elininar la carpeta `PASCAL` nos ubicamos en la carpeta `PROG` y ejecutamos el siguiente comando:

    ```bat
        rmdir ./PASCAL/
    ```

6. **Sitúate en la carpeta VARIOS y desde allí crea una nueva carpeta dentro de WORD llamado PRACT.**

    Primero nos movemos a la carpeta VARIOS con el primer comando mostrado abajo y después, para crear el directorio PRACT nos movemos a la carpeta anterior con `cd ..` y después a la carpeta WORD donde craremos la carpeta PRACT.

    ```bat
    cd ./PARTE1/VARIOS/
    cd .. && cd ./APLI/WORD && mkdir PRACT
    ```

7. **Sitúate en PRACT y desde allí muestra el contenido de la carpeta EXCEL.**

    ```bat
    cd ./APLI/WORD/PRACT/ && cd ../.. && ls ./EXEL/
    ```

8. **Desde TABLAS muestra el listado de archivos y carpetas de la carpeta raíz.** 

   Nos movemos a la carpeta TABLAS con el siguiente comando `cd ./APLI/EXCEL/TABLAS/` para después ver el contenido de la carpeta raíz: 

   ```bat
    PS /PARTE1/APLI/EXCEL/TABLAS> ls ../../..
   ```

9.  **Sitúate en la carpeta APLI y desde allí crea una subcarpeta llamada AGENDA dentro de VARIOS.**

    Perimero nos movemos a la carpeta APLI, y para crear una subcarpeta en VARIOS, nos movemos un directorio atras y, finalmente, creamos el directorio dentro de VARIOS.
    
    ```bat
    PS /PARTE1> cd ./APLI/ && cd .. && mkdir ./VARIOS/AGENDA
    ```

10. **Borra la carpeta EXCEL.**

    Para borrar la carpeta EXCEL, utilizamos `rm -r` puesto que el directorio no esta vacio. 

    ```bat
    PS /Desktop/PARTE1> rm -r ./APLI/EXCEL/
    ```

11. **Desde la carpeta raíz, crea en ella una subcarpeta llamada NUEVO.**

    Para crear un directorio NUEVO, utilizamos el comando `mkdir` desde la carpeta raíz:

    ```bat
    PS /PARTE1> mkdir NUEVO
    ```

12. **Desde PRACT muestra el contenido de WORD.**
    
    Nos movemos a la carpeta PRACT y despues hacemos un `ls` a la carpeta anterior. 
    ```bat
    PARTE1> cd ./APLI/WORD/PRACT/ && ls ..
    ```

## Ejercicio 2

---

1. **Utilizando el editor de textos de MS-DOS, crea un archivo de texto denominado EJER.TXT,
con el siguiente contenido, y almacénalo dentro de la carpeta TEXTOS (dentro de la estructura
del ejercicio anterior):**

    > “La información dentro de los discos se almacena en forma de archivos. Un archivo o fichero es un conjunto de datos que MS-DOS almacena en un disco y cuyo control interno es realizado por el sistema operativo, aunque desde el punto de vista lógico el control es del usuario”

    Para crear un documento utilizamos el comando `new-item` y después lo editamos con el comando `set-content` y añadimos el texto. 

    ```bat
    new-item ejer.txt

    set-content ./ejer.txt

    cp ejer.txt ./PARTE1/APLI/WORD/TEXTOS
    ```

2. **Copia el archivo EJER.TXT en AGENDA**
   
   ```bat
   copy ejer.txt ./PARTE1/VARIOS/AGENDA
   ```

3. **Borra el archivo almacenado en la carpeta TEXTOS.**
   
   Para eliminar el archivo de la carpeta TEXTOS debemos ejecutar el siguiente comando:

   ```bat
   rm -r ./PARTE1/APLI/WORD/TEXTOS/
   ```

4. **Añade el siguiente párrafo al archivo EJER.TXT:**

    >“Cada archivo tiene un nombre y una extensión que los distingue del resto de archivos”

    ```bat
    Set-Content EJER.txt
    ```

    A continuación veremos algo parecido a esto:

    ```bat
    Supply values for the following parameters:
    Value[0]: Cada archivo tiene un nombre y una extensión que los distingue del resto de archivos
    Value[1]: 
    ```

    Aquí añadiremos el texto y saldremos del editor.

5. **Copia el archivo EJER.TXT en la carpeta BASIC.**

    Para copiar el archivo EJER.txt realizamos el siguiente comando:

    ```bat
    cp EJER.txt ./PARTE1/PROG/BASIC
    ```

6. **Cambia el nombre del archivo almacenado en AGENDA por FICHERO.TXT**

    Para cambiar el nombre del archivo que esta en agenda hacemos lo siguiente:

    ```bat
    Ren ejer.txt fichero.txt
    ```

7. **Mueve el archivo FICHERO.TXT a la carpeta BASIC**
   
   ```bat
   move fichero.txt ./PARTE1/PROG/BASIC
   ```

8. **Abre el archivo EJER.TXT y borra la primera frase; almacena el nuevo archivo con el nombre NUEVO.TXT dentro de la carpeta BASIC.**

    Para eliminar la primera línea del fichero utilizamos lo siguiente: 

    ```powershell
    edit ejer.txt
    ```

    Se nos abrirá un editor de texto que va integrado en la terminal y eliminamos la primera línea del documento. Escribiremos `:x` y `enter`. Después cambiaremos el nombre del fichero: 

    ```powershell
    Ren ejer.txt fichero.txtç
    ```

9. **Copia el archivo NUEVO.TXT en la carpeta NOTAS.**

    ```bat
    Copy nuevo.txt ./PARTE1/APLI/WORD/NOTAS/
    ```

10. **¿Cuántos archivos hay en la carpeta BASIC? ¿Y en NOTAS?**

    En la carpeta *BASIC* nos encontramos con 2 archivos. Mientras que en *NOTAS* nos encontramos con 1 solo archivo.

## Ejercicio 3

---

1. **Borra la carpeta ACCESS y en su lugar crea una nueva carpeta llamada ASTRO**

    Puesto que `ACCES` es un directorio vacio bastara con realizar lo siguiente: 

   ```powershell
   rmdir .\PARTE1\APLI\ACCESS\
   ```

    A continuación realizamos el siguiente comando para crear la carpeta ASTRO:

    ```bat
    mkdir .\PARTE1\APLI\ASTRO
    ```

    Así quedará la estructura del directorio:

    ![Ejercicio 3.1](images/ejercicio3.png)

2. **Crea la siguiente estructura de subcarpetas dentro de la carpeta ASTRO.**

    ![Ejercicio 3.2](images/ejercicio32.png)

   Para crear la estructura mostrada debemos hacer lo siguiente:

   a. Primero nos movemos a la carpeta ASTRO:

   ```bat
     cd .\PARTE1\APLI\ASTRO\
   ```

   b. Procedemos a crear la estructura de directorios:

   ```bat
   mkdir HISTORIA
   mkdir CIENCIA
   cd .\HISTORIA\
   mkdir DATOS1
   mkdir DATOS2
   cd ..\CIENCIA\
   mkdir ASTRO1
   mkdir ASTRO2
   ```

   Después de hacer esto nos quedara la siguiente estructura:

   ![Ejercicio 3.2.1](images/ejercicio321.png)

3. **Sitúate en la carpeta CIENCIA y desde allí muestra el listado de archivos y subcarpetas de la carpeta HISTORIA**

    Primero nos ubicamos en la carpeta CIENCIA:

    ```bat
    cd .\APLI\ASTRO\CIENCIA\
    ```

    Después mostramos el listado de archivos y subcarpetas de HISTORIA con `tree`. Utilizamos el parametro `/f` para que muestre tambien los archivos:

    ```bat
    tree /f ..\HISTORIA\
    ```

    Esto nos mostrará lo siguiente: 

    ![Ejercicio 3.3](images\ejercicio33.png)

4. **Utilizando el editor de MS-DOS crea el siguiente archivo de texto y guárdalo con el nombre TYCHO.TXT dentro de la carpeta DATOS1**

    >“La importancia de Tycho Brahe (1546-1601) es debida a sus trabajos observacionales, que registraron posiciones notables del Sol, la Luna y los planetas”

    Ubicados en la carpeta raíz realizamos el siguiente comando para crear el archivo con texto:

    ```powershell
    cd .\APLI\ASTRO\HISTORIA\DATOS1\
    New-Item TYCHO.txt 
    Set-Content .\TYCHO.txt
    ```

    Con `set-content` se nos mostrará una interfaz donde podremos introducir el texto. 

5. **Utilizando de nuevo el editor de textos de MS-DOS crea el siguiente archivo de texto, y guárdalo con el nombre KEPLER.TXT dentro de la carpeta DATOS2**

    ```powershell
    Set-Content -Path .\KEPLER.txt
    ```

