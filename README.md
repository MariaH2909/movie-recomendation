<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº1 Maria Helena Molina ** </h1>

# <h1 align=center>**`Machine Learning Operations (MLOps)`**</h1>

<p align="center">
<img src="https://user-images.githubusercontent.com/67664604/217914153-1eb00e25-ac08-4dfa-aaf8-53c09038f082.png"  height=300>
</p>

 

<hr>  

## **Descripción del problema (Contexto y rol a desarrollar)**



## **Propuesta de trabajo **

**`Transformaciones`**: 


+ La primera transformacion fue desanidar **`belongs_to_collection`**, **`production_companies`** 

+ Los valores nulos de los campos **`revenue`**, **`budget`** se reemplazaron con el número **`0`**.
  
+ Los valores nulos del campo **`release date`** se eliminaron.

    las fechas se dejaron en  formato **`AAAA-mm-dd`**, se creo la columna **`release_year`** donde extraen el año de la fecha de estreno.

+ se creo la columna con el retorno de inversión, llamada **`return`** con los campos **`revenue`** y **`budget`**, dividiendo estas dos últimas **`revenue / budget`**, cuando no habian datos disponibles se calculo ,toma el valor **`0`**.

+ se eliminaron las columnas que no serán utilizadas, **`video`**,**`imdb_id`**,**`adult`**,**`original_title`**,**`poster_path`** y **`homepage`**.

<br/>



**`Desarrollo API`**:  

Se crean 6 funciones para los endpoints que se consumirán en la API.
  
+ def **peliculas_idioma**:
    Se ingresa un idioma y Devuelve la cantidad de películas producidas en ese idioma.



+ def **peliculas_duracion**:
    Se ingresa una pelicula. Debe devolver la duracion y el año.


+ def **franquicia**:
    Se ingresa la franquicia, retorna la cantidad de peliculas, ganancia total y promedio
    

+ def **peliculas_pais**:
    Se ingresa un país , retorna la cantidad de peliculas producidas en el mismo.
    

+ def **productoras_exitosas**
    Se ingresa la productora, entregando el  total y la cantidad de peliculas que realizo. 
    
+ def **get_director**:
    Se ingresa el nombre de un director que se encuentre dentro de un dataset debiendo devolver el éxito del mismo medido a través del retorno. Además, devuelve el nombre de cada película con la fecha de lanzamiento, retorno individual, costo y ganancia de la misma, en formato lista.



**`Análisis exploratorio de los datos`**: _(Exploratory Data Analysis-EDA)_

Ya los datos limpios , ahora es tiempo de investigar las relaciones que hay entre las variables de los datasets, ver si hay outliers o anomalías (que no tienen que ser errores necesariamente :eyes: ), y ver si hay algún patrón interesante que valga la pena explorar en un análisis posterior. Las nubes de palabras dan una buena idea de cuáles palabras son más frecuentes en los títulos, ¡podría ayudar al sistema de recomendación! En esta ocasión vamos a pedirte que no uses librerías para hacer EDA automático ya que queremos que pongas en practica los conceptos y tareas involucrados en el mismo. 

**`Sistema de recomendación`**: 

Una vez que toda la data es consumible por la API, está lista para consumir por los departamentos de Analytics y Machine Learning, y nuestro EDA nos permite entender bien los datos a los que tenemos acceso, es hora de entrenar nuestro modelo de machine learning para armar el sistema de recomendación de películas. El EDA incluye las  gráficas interesantes para extraer datos, como por ejemplo una nube de palabras con las palabras más frecuentes en los títulos de las películas. Éste consiste en recomendar películas a los usuarios basándose en películas similares, por lo que se debe encontrar la similitud de puntuación entre esa película y el resto de películas, se ordenarán según el score de similaridad y devolverá una lista de Python con 5 valores.
