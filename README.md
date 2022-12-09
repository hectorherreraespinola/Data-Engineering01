
# <h1 align=center> **PROYECTO INDIVIDUAL Nº1** </h1>


<hr>  

## **Introducción**

Proyecto individual como parte del bootcamp de ciencia de datos de Henry.
El proyecto consiste en realizar una ingesta de datos desde varias fuentes entregado por la cátedra, para aplicar las transformaciones necesarios, para obtener datos limpios para que luego pueda realizarse consultas a través de una API (mediante un entorno virtual dockerizado.)
Link al repositorio del proyecto: https://github.com/HX-FAshur/PI01_DATA05




## **Propuesta de trabajo**

Se realiza un analisis exploratorio y se utiliza como herramienta de transformaciones el lenguaje Python con la librería Pandas.
Luego se creo una APO mediante FastAPI para luego crear un entorno en Docker que contenga dicha API.
Al realizar este puso se realiza las consultas solicitadas por consiga.

**FastAPI**
Para la creación de la API, se utilizó el archivo main.py. Con eso se levantó la API de manera local, y se configuraron las funciones para la realización de consultas. La API carga el CSV ya transformado para realizar las consultas, y devuelve los resultados esperados.

Para este proyecto, se solicitaban únicamente 4 tipos de consultas

+ Máxima duración según tipo de film (película/serie), por plataforma y por año:
    El request debe ser: get_max_duration(año, plataforma, [min o season])

+ Cantidad de películas y series (separado) por plataforma
    El request debe ser: get_count_plataform(plataforma)  
  
+ Cantidad de veces que se repite un género y plataforma con mayor frecuencia del mismo.
    El request debe ser: get_listedin('genero')  
    Como ejemplo de género pueden usar 'comedy', el cuál deberia devolverles un cunt de 2099 para la plataforma de amazon.

+ Actor que más se repite según plataforma y año.
  El request debe ser: get_actor(plataforma, año)

**Entorno Docker**

Para la creación del contenedor, se utilizó Dockerfile. Este nos indica que vamos a utilizar un contenedor que ya trae las funciones de Python, con las librerías necesarias para cargar la API. Esto se realiza con la aplicación Docker Desktop para Windows, y con algunas líneas en la terminal del Visual Studio Code.
Consultas
Una vez que ya está activo el contenedor, se carga la URL docs para realizar las consultas, o también con la URL directa:
localhost:8000/get_max_duration(2018,'Hulu','min')
Al revisar que las consultas entregan los resultados esperados, se dan por finalizadas las consignas requeridas.
