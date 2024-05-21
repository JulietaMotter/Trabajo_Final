Introducción a las técnicas inteligentes de resolución de problemas de planificación, secuenciación y ejecución

TRABAJO FINAL
Estudiante: Julieta Motter

En el programa se desarrollan diferentes pasos para lograr calcular el índice NDVI sobre la zona del Dique los Molinos, Córdoba. 
Los pasos fueron los siguientes:
*Se instalaron las librerías necesarias
*Descomprimir el archivo zip mediante la librería zip.file
*Se seleccionaron las bandas a utilizar: Banda 3 (Green), Banda 4(Red), Banda 5(Near Infrared), Banda 6 (SWIR).
A cada una de ellas se le aplicó el mismo procedimiento:
*Se abrieron los archivos, se observaron la cantidad de datos
*Se analizaron las estadísticas básicas: valor máximo, mínimo, media, mediana, desvío estándar
*Se averiguó si las matrices eran de tipo float o no, para poder enmascarar los valores outliers.
*Como ninguna era del tipo float, se convirtieron a través de la función .astype (float)
*Se analizaron los percentiles 5 y 95 para determinar los valores que se encontraban fuera de ellos -por debajo del percentil 5 y por encima del percentil 95-.
Se generaron nuevas matrices y se enmascararon los outliers como "nan" -a través de la función np.nan-.
*Se calculó el MNDWI y luego se creó una máscara donde los valores de MNDWI eran menores a -0.025 
*Sobre esa máscara se calculó el NDVI