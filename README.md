# fastapi-docker

Este repositorio contiene una aplicación básica de **FastAPI** que responde con "Hello World" y un **Dockerfile** para containerizar la aplicación.

## Tabla de Contenidos
- [Requisitos](#requisitos)
- [Instalación de FastApi](#instalación_de_FastApi)
-  [Construcción de la Imagen Docker](#construccion_de_imagen_docker)


## Requisitos

- [Docker](https://docs.docker.com/get-docker/) instalado en tu sistema.
- Fast API
- Python
- (Opcional) Cuenta en [Docker Hub](https://hub.docker.com/) para subir la imagen.
- (Opcional) Git para gestionar el control de versiones del proyecto.


## Instalación de FastApi
```bash
python -m pip install --upgrade pip

pip install "fastapi[standard]"
```

## Construcción de la Imagen Docker

Desde el directorio raíz del proyecto, ejecuta el siguiente comando (reemplaza `<tu_usuario>` con tu nombre de usuario, por ejemplo, `victxr10`):

```bash
docker build -t <tu_usuario>/fastapi:v1 .

docker run -d -p 8000:8000 --name fastapi_app <tu_usuario>/fastapi:v1

docker login

docker tag <tu_usuario>/fastapi:v1 <tu_usuario>/fastapi:v1

docker push <tu_usuario>/fastapi:v1

docker stop fastapi_app && docker rm fastapi_app

docker rmi <tu_usuario>/fastapi:v1
