## Configuration
Caricare il container docker

[Jupyter official image](https://hub.docker.com/r/jupyter/pyspark-notebook)
```bash
    docker run -v $(pwd)/data:/home/jovyan/data -p 8888:8888 quay.io/jupyter/pyspark-notebook 
```


Copiare l'URL del server jupyter per poter utilizzare il notebook 
![alt text](images/image.png)

Procedura su VS code
![alt text](images/image-1.png)
![alt text](images/image-2.png)
![alt text](images/image-3.png)


## TODO
- trovare un dataset per applicare qualcosa di machine learning
- salvare il dataset nella cartella data
- seguire la guida qui ((https://spark.apache.org/docs/latest/ml-guide.html)
