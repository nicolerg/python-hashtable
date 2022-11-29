# `nicolerg/python-hashtable`: HashTable Docker image

This Python-based Docker image includes an installation of the [hashtable-nicolerg](https://github.com/nicolerg/python-hashtable/tree/master/hashtable-nicolerg) Python package,
created by following [this tutorial](https://realpython.com/python-hash-table/) written by Bartosz Zaczyński. 
The `HashTable` class replicates many methods from Python dictionaries, including
`HashTable.clear()` and `HashTable.update()`.  

## Installation

This Docker image is available on [Docker Hub](https://hub.docker.com/repository/docker/nicolerg/python-hashtable). 
Pull the image:
```bash
docker pull nicolerg/python-hashtable
```

## Usage 

Run an interactive container over the image to work with `HashTable` in a Python interpreter.
Note that the `HashTable` module is automatically imported: 
```
$ docker run -it nicolerg/python-hashtable
Python 3.11.0 (main, Nov 15 2022, 19:58:01) [GCC 10.2.1 20210110] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> hash_table = HashTable(capacity=100)
```
See `HashTable` usage [here](https://github.com/nicolerg/python-hashtable#usage). 

## Motivation 

Creating this image reinforced knowledge in the following areas:  
* Containerization with [Docker](https://docs.docker.com/)
* [Using the `PYTHONSTARTUP` environment variable](https://stackoverflow.com/questions/74609139/can-i-import-default-python-modules-in-a-python-docker-image)  

## Dev notes

1. Write a [Dockerfile](Dockerfile)  
2. Create a new repository on [Docker Hub](https://hub.docker.com/)
3. Build an image  
    ```bash
    docker build -t nicolerg/python-hashtable .
    ``` 
4. Test the image locally  
    ```bash
    docker run -it nicolerg/python-hashtable
    ```
5. Push the image to Docker Hub (must be signed in on Docker Desktop) 
    ```bash
    docker push nicolerg/python-hashtable
    ```
