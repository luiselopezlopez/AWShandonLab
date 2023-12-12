**Importar el módulo http**
var http = require('http');

**Crear el servidor**
Crear una carpeta /app
Dentro crear el archivo server.js

```javascript

http.createServer(function (req, res) {

  // Escribir la cabecera de la respuesta
  res.writeHead(200, {'Content-Type': 'text/plain'});

  // Escribir el cuerpo de la respuesta
  res.end('¡Hola Mundo!');

// Escuchar en el puerto 8080
}).listen(8080);

// Imprimir un mensaje para indicar que el servidor está en marcha
console.log('Servidor funcionando en http://localhost:8080/');

```
Ejecutar con 

```bash 
node server.js
```  
Para hacer que tu aplicación se inicie al inicio con PM2, sigue estos pasos:  
   
**Paso 1: Instalar PM2**  
   
Primero, necesitas instalar PM2 globalmente en tu sistema. Puedes hacer esto con el siguiente comando:  
   
```bash  
$ npm install -g pm2  
```  
   
**Paso 2: Iniciar tu aplicación con PM2**  
   
Una vez que PM2 esté instalado, puedes iniciar tu aplicación con él. Navega hasta el directorio de tu aplicación y ejecuta el siguiente comando:  
   
```bash  
$ pm2 start app.js  
```  
   
Esto iniciará tu aplicación con PM2. PM2 asignará un ID a tu aplicación, que puedes usar para administrarla.  
   
**Paso 3: Configurar el inicio automático con PM2**  
   
Para configurar tu aplicación para que se inicie automáticamente en el arranque, puedes utilizar la función `startup` de PM2. Ejecuta el siguiente comando:  
   
```bash  
$ pm2 startup  

