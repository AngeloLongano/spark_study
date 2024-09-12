## Configurazione per usare il notebook Jupyter dentro il container Docker
Occorre scaricare l'immagine uffuciale di Jupyter [pyspark-notebook](https://hub.docker.com/r/jupyter/pyspark-notebook) attraverso il seguente comando:

```bash
    docker pull quay.io/jupyter/pyspark-notebook
```

Successivamente sarà necessario far eseguire il container con questo comando:

```bash
    docker run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work quay.io/jupyter/pyspark-notebook
```
In questo modo verrà eseguito un container docker con Python, PySpark, Jupyter, Java e tutti i pacchetti per permettere a Spark di funzionare.  
Inoltre la directory corrente verrà montanta sul container.

A questo punto ci basta solo selezionare dal nostro Jupyter notebook il servere Jupyter che abbiamo appena fatto partire.  

Svolgere i seguenti passaggi:
1. Copiare l'URL del server Jupyter dal terminale del Container Docker
![alt text](images/image.png)
1. Se usate VS code, basta indicare di volersi connettere ad un server esistente e incollare l'url copiato prima.
![alt text](images/image-1.png)
![alt text](images/image-2.png)
![alt text](images/image-3.png)

Per approfondimenti si manda al link dei vari [stacks docker per Jupyter](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-pyspark-notebook
) e alla [documentazione per far eseguire l'immagine](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/running.html).
# Sperimentazione
Nel notebook verrà fatta un addestramento di Machine Learning utilizzando il Random Forest per una classificazione multipla.  
Il dataset [connect-4](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/multiclass.html#connect-4) è stato scelto dai dataset LIBSVM di [Chih-Jen Lin](https://www.csie.ntu.edu.tw/~cjlin/index.html) con più 67k esempi. 


