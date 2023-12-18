# "PROYECTO INDIVIDUAL Nro. 01: MARCHINE LEARNING OPERATIONS (MLops) APLICADO EN LA PLATAFORMA DE VIDEOJUEGOS STEAM"

## ROL A DESARROLLAR
El objetivo de este proyecto es REALIZAR un SISTEMA DE RECOMENDACIÓN de videojuegos para la plataforma de videojuegos STEAM para usuarios. Para empezar con el proyecto se deberá trabajar con una fuente de datos que contiene los elementos necesarios para el trabajo, dichas fuentes deberá ser sometidas a diferentes procesos de EXTRACCIÓN TRANSFORMACIÓN Y LIMPIEZA de datos a causa de que dichos elementos se encuentran anidados, diversidad de datos, entre otras cosas.

## PROCESO DEL PROYECTO INDIVIDUAL

### PROCESO DE EXTRACCIÓN - TRANSFORMACIÓN - LIMPIEZA DE LOS DATOS EN BRUTO...
En el archivo **ETL.ipynb** se encuentra el código que permite el trabajo de ETL al dataset de la plataforma STEAM, una vez finalizado dicho proceso, los archivos se guardarán en la carpeta **DATASETS_STEAM_LIMPIO**.

### DATASETS_STEAM_LIMPIO...
En esta carpeta se tiene TRES (03) archivos que se detallan a continuación:

**games_limpio.csv**: Es el archivo que contiene los datos de steam_games.gz.json después del proceso de ETL, dicho archivo contiene los datos relacionados con los aspectos más relevantes de los videojuegos, como por ejemplo, nombres de videojuegos, empresa responsable, fecha de lanzamiento, entre otros aspectos.

**items_limpio.csv**: Es el archivo que contiene los datos de user_items.gz.json después del proceso de ETL, dicho archivo contiene los datos relacionados con los aspectos más relevantes de la relación entre los usuarios de la plataforma y los items de usuario, como por ejemplo, nombres y numeros de identificación de usuarios, cantidad de horas jugadas de los usuarios por videojuego, entre otros aspectos.

**user_reviews.csv**: Es el archivo que contiene los datos de user_reviews.gz.json después del proceso de ETL, dicho archivo contiene los datos relacionados con los aspectos más relevantes relacionados con los usuarios, las recomendaciones y comentarios de los videojuegos de la plataforma, como por ejemplo, nombres y numeros de identificación de usuarios, recomendaciones y comentarios, última edición, entre otros aspectos.

### PROCESO DE PREPARACIÓN DE LOS DATOS PARA SU USO EN FastAPI...
En el archivo **Dataset_para_Funciones_API.ipynb** se encuentra el código que permite el trabajo de preparación de los datos para ser usados y consumidos por FastAPI. Dichos archivos son los siguientes:

+ **PlayTimeGenre.csv**
+ **SentimentAnalysis.csv**
+ **SystemTheRecommendation.csv**
+ **UserForGenre.csv**
+ **UsersRecommend.csv**

### PROCESO DE ANÁLISIS EXPLORATORIO DE DATOS...
En el archivo **EDA.ipynb** se encuentra el código que permite el trabajo de EDA al dataset con los datos ya procesados.

### SISTEMA DE RECOMENDACIÓN DE VIDEOJUEGOS "item - item"...
En el archivo **Sistema_de_Recomendacion.ipynb** se encuentra el proceso para preparar ciertos datos para la recomendación de videojuegos y ser usados para fastAPI. Dichos datos serán guardados en el archivo **cosine_sim_item.parquet** que se guardará en la carpeta **Archivos_para_SISTEMA_DE_RECOMENDACIÓN**.

### FastAPI...
Finalmente en el archivo **main.py** contendrá el código para el uso de la interfaz para la interacción entre el usuario y los datos basados en SEÍS (06) edpoint, donde también incluye el sistema de recomendación de videojuegos.