# Laboratrio 3: detección defamilias de Malware

En este laboratorio se identificaron distintas familias de malware utilizando los archivos infectados que fueron obtenidos en clase. 

## Datasets

Para identificar las familias se extrajeron los imports y el timestamp de complicación de cada archivo para formar un dataset y ya con ese dataset se implementaron varios algoritmos como clustering o el coeficiente de Jaccard. 

Puede ver el proceso aquí: [Notebook](./lab3.ipynb)

El dataset inicial fue formado usando Pefile para extraer los imports en el header de cada archivo y el timestamp de complicación, este dataset incial se encuentra disponible en: [Dataset](./raw_data.csv)

Luego, para implementar el clustering, se realizó TF-IDF sobre los imports y esto dio como resultado que cada conjunto de imports de cada archivo se convirtiera en un vector de 360 componentes. Este dataset se encuentra disponible en: [Dataset TF-IDF](./transformed.csv)

Después se implementaron los algoritmos de clustering y se guardó un archivo que contiene la etiqueta que indica a que clúster pertenece cada archivo: [Clustering](./labeled.csv)

Finalmente se realizón un dataset con los embeddings de cada archivo usando Gemini: [Embeddings](./embeddings.csv)


## Implementación de algoritmos

Una vez con los datasets, se implementaron 2 algoritmos de particionamiento, K-means y K-Metroids, los datos de los datasets fueron normalizados para implementar los algoritmos 




