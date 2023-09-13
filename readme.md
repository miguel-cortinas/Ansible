# Configuración de un Servidor en Docker

Este README te guiará a través de los pasos para configurar un servidor en un contenedor Docker.

## Paso 1: Acceder al Contenedor


```bash
docker exec -ti nombre_del_contenedor /bin/bash

Sustituir nombre_del_contenedor por el nombre de nuestro contenedor.

## Paso 2: Actualizar el Sistema

```bash
apt update

## Paso 3: Instalar Python

```bash
apt install python3

## Paso 4: Instalar OpenSSH Server

```bash
apt install openssh-server

## Paso 5: Iniciar el Servicio SSH

```bash
service ssh start

## Paso 6: Navegar al Directorio .ssh

```bash
cd .ssh/

## Paso 7: Instalar el Editor de Texto Nano

```bash
apt install nano

## Paso 8: Configurar el archivo authorized_keys

```bash
nano authorized_keys


Luego, copiamos la llave pública que proviene de cat id_rsa.pub y la pegamos en el archivo authorized_keys. Guardamos los cambios y salimos de Nano.

y con esta serie de pasos configuramos con éxito un servidor en tu contenedor Dock.

Por ultimo, creamos nuestro playbook, con dos tareas, una para crear la carpeta, y otro para crear el archivo. 