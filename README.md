[![Build Status](https://travis-ci.org/nokutu/proyectoips.svg?branch=master)](https://travis-ci.org/nokutu/proyectoips)
# Proyecto IPS. Grupo 1 Lab2
Este es el repositorio del proyecto de IPS de 3º de Ingeniería Informática del Software. Grupo de laboratorio 2, grupo de trabajo 1.

## Ciclo de desarrollo
Los pasos de un ciclo normal de desarrollo con Git son:

1. Hacer pull del repositorio para descargar los cambio.
2. Trabajar en las historias.
3. Cada vez que hagas algo significativo y **el código compile** hacer commit.
4. Si ya has terminado, hacer push al servidor. Sino, volver al paso 2.

## Importar el proyecto
* Clonar el repositorio para tenerlo en local. Se puede usar Sourcetree o otra herramienta a tu elección.
* Dependiendo del IDE tienes que:
    * Eclipse: (probado con Eclipse Neon, no puedo asegurar que funcione en versiones más antiguas). File -> Import -> Gradle -> Gradle project. Seleccionas el path al proyecto y le das a finish.

## Ejecutar el proyecto
Se está utilizando un sistema de buildeo llamado Gradle, similar a Maven. Este se encarga de la compilación, ejecución de tests y descarga de dependencias (jdbc y el driver de la bbdd por ahora). Hay dos formas principales de utilizarlo:

* Desde terminal. Tendrías que ir a la carpeta raiz y ejecutar:
    * Windows 
  
    ```
    gradelw run
    ```

    * Linux 

    ```
    ./gradelw run
    ```
* Desde el IDE. Eclipse, IntelliJ o Netbeans tienen soporte para gradle. Deberíais poder encontrar una lista de tasks, estan run entre ellas.
    * Eclipse: Las distintas opciones de gradle están en el menú inferior, donde pone *Gradle Tasks*. Las principales son *build* y *run*.

## Arrancar la base de datos
La base de datos más simple que pude encontrar se llama H2. Para arrancarla hay que hacer lo siguiente:

* Ir a la carpeta BBDD del proyecto.
* Descomprimir el archivo *.zip*
* Ir a h2 -> bin.
* Ejectutar el archivo *h2.bat* (Windows) o *h2.sh* (Linux).

## Travis
Travis es un sistema de integración continua. Su función es ejecutar builds cada vez que alguien hace un push al repositorio. Cada vez que haya un fallo, se mandará un email al dueño del repositorio (yo) y al autor del commit.
Travis está disponible [aquí](https://travis-ci.org/nokutu/proyectoips)
