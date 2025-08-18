# Taller diseño y estructuración de aplicaciones distribuidas en internet

En este taller se explorará la arquitectura de las aplicaciones distribuidas. Concretamente, exploraremos la arquitectura de  los servidores web y el protocolo http sobre el que están soportados. 

El reto se consistió en diseñar e implementar un servidor web que soporta múlltiples solicitudes seguidas no concurrentes. El servidor es capaz de leer los archivos del disco local y retornar todos los archivos solicitados, incluyendo páginas html, archivos java script, css e imágenes. 
Además, se contruyó una pequeña aplicación web con  javascript, css, e imágenes para probar el servidor. Así mismo se incluyó en la aplicación la comunicación asíncrona con unos servicios REST en el backend.

## Primeros pasos

Para ejecutar nuestro proyecto primero debemos clonar este repositorio, para esto nos debemos dirigir a la consola de nuestro equipo y conlar el proyecto siguiendo los pasos a continuación:

En nuestra consola, compiamos y ejecutamos la siguiente linea:

```
git clone https://github.com/CamiloQuinteroR/Dise-o-y-estructuraci-n-de-aplicaciones-distribuidas.git
```

<img width="1170" height="166" alt="image" src="https://github.com/user-attachments/assets/c29b23f5-7738-4753-8551-11722f1823c4" />

Al ejecutar este comando, ya tendremos el proyecto de forma local. 





### Prerequistos

Para ejecutar este proyecto deberas tener instalado en tu maquina cualquier IDE, como los son NetBeasn o Visual Studio Code.
En este caso, abriremos y ejecutaremos el poryecto usando NetBeans. 

Sin importar el IDE deberás tener instalado JDK 23 y Maven. 

Si deseas instalar Maven basta con dirigirnos a la pagina de Maven y descargar el instalador que requiera nuestra maquina:

```
[Give examples](https://maven.apache.org/download.cgi)
```

Al descargar el archivo, seguiremos los pasos de la instalación, es realemente sencillo. 


### Instalando

Depsues de tener nuestro poryecto clonado de forma local, abrimos nuestro proyecto en el IDE de preferencia, en este caso los abriremos en NetBeans:

<img width="251" height="107" alt="image" src="https://github.com/user-attachments/assets/83c2326f-c74d-4fd5-aa1b-e231b0218896" />

Nos dirigimos a la clase principal, en este caso es HttpServer.java:

<img width="284" height="214" alt="image" src="https://github.com/user-attachments/assets/3aa96a41-3161-4c5e-ad1f-dabe86fbb708" />


A continuación ejecutamos la clase HttpServer.java:

(Si estamos en NetBeans, basta con dar clic derecho sobre la clase y dar clic sobre la opción "Run File")

<img width="293" height="304" alt="image" src="https://github.com/user-attachments/assets/4ef0931b-799e-46c9-902a-cad335653b28" />


Al ejecutar nuestro poryecto veremos en consola en mensaje incial de nuestro servidor:

<img width="590" height="267" alt="image" src="https://github.com/user-attachments/assets/0f75c8fc-7f5a-42f5-bf59-f3982b52b14c" />


Si deseamos, tambien podemos ejecutar nuestro proyecto desde consola, para esto ejecutaremos el siguiente comando:


```
mvn compile
```

<img width="1253" height="392" alt="image" src="https://github.com/user-attachments/assets/6fc2d9eb-bcb1-4689-b66d-dc1f2973f1b3" />


Hay que tener en cuenta que debemos ejecutar este comando en el directorio donde se encuentra ubicado nuestro archivo pom.xml. 

Posteriormente ejecutaremos el siguiente comando:

```
mvn compile
```

<img width="957" height="194" alt="image" src="https://github.com/user-attachments/assets/f8afbba4-5fe5-4c82-a0c8-29397242e606" />

Veremos en consola el mensaje inicial de nuestro servidor. 

## Ejecución de las pruebas

Teniendo nuestro servidor corriendo, ingresaremos al broswer y escribirimos la siguiente URL:

```
http://localhost:35000

```

Allí veremos la siguiente aplicación:

<img width="1132" height="521" alt="image" src="https://github.com/user-attachments/assets/f933650e-cf6a-4f15-91fb-13966ded4fa4" />

Podremos ver que hay un formulario en que podemos poner nombres de tareas pendientes, que se agregaran a una lista cuando damos clic en el boton "Agregar"

<img width="310" height="315" alt="image" src="https://github.com/user-attachments/assets/72fe909a-98db-4c7b-a9a2-c2c145e65697" />

Podemos ver que en la imagen anterior, se añadieron tareas como "Matematicas", "cvds" y "arep"

Ahora para probar la funcionalidad de que el servidor soporta múlltiples solicitudes seguidas no concurrente, veremos que en consola tendremos los siguientes resultados:

<img width="185" height="135" alt="image" src="https://github.com/user-attachments/assets/4b72632b-f5d2-41a9-ade1-fd5b55f3ffd9" />

Vemos como el servidor responde cada una de las solicitudes.

Así mismo, podemos usar la siguiente URL para probar el servicio REST:

```
http://localhost:35000/app/task?name=cvds
```

veremos que se nos genera un archivo JSON con la siguiente respuesta:


<img width="421" height="123" alt="image" src="https://github.com/user-attachments/assets/01b3b916-77b1-4819-aeb7-7b49b33a57ed" />

Como se evidencia, la URI de solicitud es:

```
/app/task?name=cvds

```

y la respuesta del servidor es:


```
"Tarea cvds"
```

## Desarrollado con

* https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html - Java 23
* https://maven.apache.org/ - Maven


## Autores

* **Camilo Andrés Quintero Rodriguez**

