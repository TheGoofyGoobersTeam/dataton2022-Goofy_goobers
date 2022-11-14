# dataton2022-Goofy_goobers
 Proyecto Dataton 2022 Bancolombia en el cual tenemos dos procesos un categorizador y un recomendador de noticias
 
## Uso
Los notebooks usados en este repositorio se ejecutaron usando colab pro con GPU, por lo cual si se desea usar de esta forma solo se nesesita cambiar las direcciones de guardado de los archivos, en caso de correr estos archivos localmente se puede desccargar o clonar el repositorio e instalar las librerias usando el archivo [src/data/archivos_auxiliares/requirements.txt][requirements].
 
## Categorizador
para el categorizador utilizaremos dos algoritmos uno de deteccion de fake news y un zero-shot algoritm para poder clasificar la informacion para mas informacion de esto revisar [documentación/Documentación_Datatón.pdf][DocDat], y el codigo utilizado fue ejecutado inicialmente en colab con gpu y se puede encontrar en [src/recomendador/Categorizacion.ipynb][CatCod], este utiliza los archivos auxiliares que por motivos de peso no se encuentran en el repositorio por lo cual se creo un repositorio de zenodo en el cual se encuentran y es el siguiente:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7317351.svg)](https://doi.org/10.5281/zenodo.7317351)

## Cliente o Sector
para terminar el categorizaddor utilizaremos el notebook [src/recomendador/Cliente_y_Recomendacion.ipynb][RecCod] en la primera parte de este notebook encontramos una puntuacion que le llamaremos Acercamiento de cliente con el cual podemos diferenciar cada para Nit-Noticia si es cliente o sector, los resultados de esto los encontramos en :
[src/data/output/categorizacion.csv][CatRes]

## Recomendador
Para el recomendador tambien utilizaremos el notebook [src/recomendador/Cliente_y_Recomendacion.ipynb][RecCod] el cual en la segunda parte utilizaremos la siguiente ecuacion:

\begin{equation}\label{etiqueta:uno}
Puntaje = Probalidad \  de\ la\ clase * Peso\ de\ la\ clase + Acercamiento\ de\ cliente
\end{equation}

Con este puntaje se organizan las recomendaciones de noticias por cliente y este se puede ver con la estructura deseada en el archivo:
[src/data/output/recomendacion.csv][RecRes]
  



   [DocDat]: <https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/documentaci%C3%B3n/Documentaci%C3%B3n_Datat%C3%B3n.pdf>
   [CatCod]: <https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/src/recomendador/Categorizacion.ipynb>
   [CatRes]: <https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/src/data/output/categorizacion.csv>
   [RecCod]: <https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/src/recomendador/Cliente_y_Recomendacion.ipynb>
   [requirements]:<https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/src/data/archivos_auxiliares/requirements.txt>
   [RecRes]: <https://github.com/TheGoofyGoobersTeam/dataton2022-Goofy_goobers/blob/main/src/data/output/recomendacion.csv>
