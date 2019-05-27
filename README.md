# notas de docker

## Contenedor

Un contenedor docker es como una función con un decorador que define limitaciones, recursos y dependencias. También esta definición podría ser extrapolada a como funcionan las clases, con propiedades y métodos, donde las propiedades, son las limitaciones, recursos, dependencias, y los procesos son las funciones.

## Comandos

```
docker ps = lista los contenedores
docker ps -a = lista contenedores a detalles
docker ps -aq = lista solo los ID de los contenedores (la q significa quiet, tranquilo o silencioso)
docker inspect id_contenedor = detalles internos del contenedor
docker inspect nombre_contenedor = lo mismo que el anterior
docker inspect -f {{}} nombre_contenedor = filtra una variable especifico del contenedor
docker rm nombre_contenedor = elimina un contenedor
docker rm $(ps -aq) = borra TODOS los contenedores
```

## Run an nginx server as container

```bash
sudo docker run -d --name <server_name> -p <port>:80 nginx
sudo docker run -d --name serve1 -p 8000:80 nginx
sudo docker run -d --name serve2 -p 7000:80 nginx
```