  
1. **Conéctate al servidor MySQL**  
  
   Abre la terminal y usa el siguiente comando para iniciar sesión en el servidor MySQL como root. Se te pedirá que introduzcas tu contraseña.  
  
   ```bash  
   mysql -u root -p  
   ```  
   
2. **Crea la base de datos**  
  
   Una vez que estés en el prompt de MySQL (`mysql>`), puedes crear una nueva base de datos utilizando el comando `CREATE DATABASE`. Por ejemplo, para crear una base de datos llamada `my_database`, usarías el siguiente comando:  
  
   ```sql  
   CREATE DATABASE my_database;  
   ```  
  
   Asegúrate de terminar el comando con un punto y coma.  
   
3. **Usa la base de datos**  
  
   Para empezar a usar la base de datos que acabas de crear, necesitas seleccionarla con el comando `USE`:  
  
   ```sql  
   USE my_database;  
   ```  
   
4. **Crea una tabla**  
  
   Ahora puedes empezar a crear tablas en tu base de datos. Por ejemplo, aquí te mostramos cómo crear una tabla simple llamada `my_table`:  
  
   ```sql  
   CREATE TABLE my_table (  
     id INT AUTO_INCREMENT,  
     name VARCHAR(100),  
     email VARCHAR(100),  
     PRIMARY KEY(id)  
   );  
   ```  
  
   Este comando crea una nueva tabla con tres columnas: `id`, `name` y `email`.  
   
5. **Verifica la creación de la tabla**  
  
   Puedes verificar si tu tabla se ha creado correctamente utilizando el comando `SHOW TABLES`:  
  
   ```sql  
   SHOW TABLES;  
   ```  

6. **Inserta datos en la tabla**  
  
   Ahora que has creado una tabla, puedes insertar datos en ella. Para ello, utiliza el comando `INSERT INTO`. Por ejemplo, para insertar un nuevo registro en la tabla `my_table`, usarías el siguiente comando:  
  
   ```sql  
   INSERT INTO my_table (name, email) VALUES ('John Doe', 'jon@doe.com')
   ```

7. **Actualizar App Web**

   npm install mysql

   npm install express

   ```javascript
   var express = require('express');
   var mysql = require('mysql');
   var app = express();
   var port = 8080;
   var con = mysql.createConnection({
   host: "",
   user: "admin",
   password: "",
   database: "my_database"
   });
   app.get('/', function (req, res) {
   con.query("SELECT * FROM my_table", function (err, result, fields) {
      if (err) throw err;
      res.send(result);
   });
   });
   app.listen(port, function () {
   console.log('App listening on port ' + port);
   });
   ```
   
