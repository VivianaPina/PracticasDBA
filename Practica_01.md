# Práctica 01: 
## Ecosistema de un Administrador de Bases de datos y creación de una API


En esta práctica, primero creamos una máquina virtual (MV) en **Azure**.

Luego, usando la consola de nuestra computadora, nos conectamos a nuestra MV, en donde mediante los comandos proporcionados por el profesor instalamos el SMBD que elegimos: **Postgres**. 

Además, creamos en nuestra MV las carpetas en donde guardaremos nuestras prácticas del curso.


```
sudo mkdir practicas
```


En nuestra carpeta de *Practica_01* usando el comando 


```
 ls -l
```

listamos los componentes de nuestra carpeta, en esta misma podemos crear y editar nuestros archivos de código, con los comandos:



```
 sudo nano queries.js

 sudo nano puppies.sql

 sudo -u postgres psql -f puppies.sql

```

También necesitamos cambiar nuestro archivo *index* de JS usando


```
 cd routes/

 sudo nano index.js

```

Finalmente, para corroborar que nuestra API funcionara, iniciaremos nuestro servicio metiendo en consola:


```
 sudo npm start

```

Después en la barra de dirección de nuestro buscador escribiremos nuestra IP y el puerto, además del nombre de nuestra base de datos:


```
 http://52.170.151.33:3000/api/puppies
```

