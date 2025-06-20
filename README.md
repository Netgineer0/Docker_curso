# Curso Docker documentación

Lo primero que se realizo fue hacer las instalaciones ertinentes para que no hubiera ningún error. Se instalo Docker desktop

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/1_docker.PNG)

Se redirigio a la pagina de Git-hub en la que se encuentra toda la documentación y en especifico un documento con todos los atajos y comandos que se requiere en docker

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/2_docker.PNG)

En el software de Visual Basic, se instalo la extensión Acyvitus Bar
![docker](https://github.com/Netgineer0/Docker_curso/blob/main/3_docker.PNG)

## Introducción a Docker
 **Docker:** una plataforma que permite crear, distribuir y ejecutar aplicaciones dentro de contenedores ligeros.
 La diferencia entre un contenedor y una máquina virtual: los contenedores comparten el kernel del sistema operativo, haciendo que sean más eficientes

## ¿Para qué sirve Docker?
**Facilita la portabilidad del software:** "funciona en cualquier entorno" porque el contenedor incluye todo lo necesario.\
Permite aislamiento entre aplicaciones, evitando conflictos de dependencias.\
**Optimiza recursos:**, ya que múltiples contenedores pueden correr en una misma máquina sin peso de VMs completas.

Algunos de los comandos basicos dentro de docker son:

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/4_docker.PNG)

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/5_docker.PNG)

## Beneficios de los contenedores
![docker](https://github.com/Netgineer0/Docker_curso/blob/main/6_docker.PNG)

## Contenedores vs Máquinas Virtuales
- Los contenedores comparten el kernel del sistema operativo, ejecutándose como procesos aislados, mientras que las máquinas virtuales requieren un sistema operativo completo por instancia
- Esto los hace más eficientes en recursos y más rápidos al iniciar: ocupan megabytes en lugar de gigabytes, y arrancan en segundos 

## HOLA MUNDO en Docker
 Muestra cómo ejecutar imágenes sencillas como hello-world
 
![docker](https://github.com/Netgineer0/Docker_curso/blob/main/7_docker.PNG)

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/8_docker.PNG)

## Borrar contenedores e imágenes
A medida que se trabaja en docker se acumulan contenedores parados, imágenes antiguas y componentes intermedios que ocupan espacio en disco. Con el siguiente comando se elimino alguno de
los contenedores creados

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/9_docker.PNG)

Para visualizar el cambio hecho previamente se puede ejecutar el comando **container docker ls -a**. O simplemente dirigirnos hacía docker desktop y visualizar el resultado, como se muestra a continuación

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/10_container.PNG)

Otra alternativa que se emplea para realizar el mismo proceso es el siguiente

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/11_docker.PNG)

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/12_container.PNG)

Otra alternativa que presenta es el comando que se utiliza en la siguiente imagen. Es requerido cuando queremos eliminar todos los contenedores creados

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/13_docker.PNG)

## Borrar imagenes
Se puede eliminar por el nombre de la imagen

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/12_docker.PNG)


## Docker compose
Se utiliza para gestionar aplicaciones y aumentar la eficiencia en el desarrollo de contenedores. La configuración se guarda en un único archivo YAML, lo que permite crear y escalar aplicaciones fácilmente. Docker Compose se utiliza a menudo para configurar un entorno local

## Comandas básicos dentro de Docker compose
- **docker-compose up:**	Inicia los contenedores definidos en el YAML
- **docker-compose up -d:**	Inicia los contenedores en segundo plano 
- **docker-compose down:**	Detiene y elimina los contenedores, redes y volúmenes
- **docker-compose build:**	Construye las imágenes 
- **docker-compose ps:**	Muestra el estado de los contenedores
- **docker-compose logs:**	Muestra los servicios
- **docker-compose exec <srv>:**	Ejecuta un comando en un contenedor activo

## Ejemplo práctico de Docker compose

Se crea una nueva carpeta 

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/10_compose.PNG)

Luego, se dirige en la carpeta que se acaba de crear

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/11_compose.PNG)

Se crea el archivo app.py en la carpeta y se debe introducir el siguiente código

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/2_compose.PNG)

Se crea también el archivo requirements.txt con las dependencias necesarias:

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/compose_texto.PNG)

Dockerfile se utiliza para crear la imagen de Docker. Se crea un archivo sin extension

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/dockerfile.PNG)

Se debe configurar los servicios “redis” y “web” en docker-compose.yml

Se crea el archivo app.py en la carpeta y se debe introducir el siguiente código

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/3_compose.PNG)

Se inicia la aplicación desde la carpeta del proyecto

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/compose_correr.PNG)

Se ejecuta la aplicación. Como se muestra a continuación. Y cada vez que visitamos la imagen, aumenta la visita

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/6_1.PNG)


![docker](https://github.com/Netgineer0/Docker_curso/blob/main/corriendo.PNG)

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/er.PNG)

## Práctica
Lo primero que se realizo fue clonar el proyecto, seguido de establecerse en el directorio

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/1_pc.PNG)

Seguidamente iniciar el contenedor

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/2_pc.PNG)


Se debe de revisar cada uno de los archivos. Y verificar si la versión que tenemos instalada en nuestro equipo es el correcto. Para que el proyecto pueda levantar

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/3_pc.PNG)

2. Otro ejemplo práctico que se ejecuto dentro de consola. Pero que se incluyo archivos .json para ejecutar un contenedor que realice una petición HTTP a una API externa

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/3_pc2.PNG)

A continuación se muestra cuál fue el orden de los archivos y qué tipo se crearon

**docker-compose.yml:* Define el servicio que construirá y ejecutará el contenedor \
**Dockerfile:* Construye una imagen de Node.js para ejecutar la app \
**package.json:* Especifica las dependencias del proyecto \
**index.jsindex.js:*  realiza la petición HTTP a la API

En cuento a docker desktop. Se puede visualizar de manera gráfica si los contenedores estan dados de alta

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/4_pc2_2.PNG)

3. Por últim se creo un contenedor compose, para que se visualizará en el puerto 3000, la misma API que se ejecuto dentro de consola. A continuación se muestra los comandos ejecutados para que el contenedor levantará
   
![docker](https://github.com/Netgineer0/Docker_curso/blob/main/contenedor.PNG)

![docker](https://github.com/Netgineer0/Docker_curso/blob/main/contenedor2.PNG)
