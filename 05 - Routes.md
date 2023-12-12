Una vez que se han creado las subredes, el siguiente paso es crear las tablas de rutas. Las tablas de rutas determinan dónde se dirige el tráfico de red para cada subred.   
  
**Crear la tabla de rutas para la subred 'publica'**  
   
1. En la consola de AWS, ve a la sección "VPC" y selecciona "Route Tables" en el panel de navegación izquierdo.  
   
2. Selecciona la Default Route  
   
6. Haz clic en "Edit subnet associations".  
   
7. En la lista de subredes, selecciona la subred 'publica', 'Frontend' y 'Backend' y haz clic en "Save".  
   
  
**Añadir rutas a las tablas de rutas**  
   
Por último, necesitarás añadir rutas a tus tablas de rutas. Para la tabla de rutas 'publica', necesitarás añadir una ruta que permita el tráfico de Internet. Para las tablas de rutas 'frontend' y 'backend', necesitarás añadir rutas que permitan el tráfico entre las subredes.  
   
1. En la sección "Route Tables", selecciona la tabla de rutas 'publica'.  
   
2. Haz clic en "Routes" y luego en "Edit routes".  
   
3. Haz clic en "Add route". En "Destination", introduce "0.0.0.0/0". En "Target", selecciona "NAT Gateway" y luego selecciona tu NAT Gateway. Haz clic en "Save routes".  
   
