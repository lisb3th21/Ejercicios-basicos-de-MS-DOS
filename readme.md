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

1. Utilizando el editor de textos de MS-DOS, crea un archivo de texto denominado EJER.TXT,
con el siguiente contenido, y almacénalo dentro de la carpeta TEXTOS (dentro de la estructura
del ejercicio anterior):

    > “La información dentro de los discos se almacena en forma de archivos. Un archivo o fichero es un conjunto de datos que MS-DOS almacena en un disco y cuyo control interno es realizado por el sistema operativo, aunque desde el punto de vista lógico el control es del usuario”

    Para crear un documento utilizamos el comando `new-item` y después lo editamos con el comando `set-content` y añadimos el texto. 

    ```bat
    new-item ejer.txt

    set-content .\ejer.txt

    cp ejer.txt ./PARTE1/APLI/WORD/TEXTOS
    ```

2. **Copia el archivo EJER.TXT en AGENDA**
   
   ```bat
   cp ejer.txt ./PARTE1/VARIOS
   ```

3. Borra el archivo almacenado en la carpeta TEXTOS.
   
   Para 