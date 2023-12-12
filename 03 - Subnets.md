
   
1. **Inicia sesión en tu cuenta de AWS**  
  
   Accede a la consola de administración de AWS.  
   
2. **Navega hasta el servicio de VPC**  
  
   En la consola de administración de AWS, encuentra el menú de servicios y selecciona "VPC".  
   
3. **Accede a la sección de subredes**  
  
   En el panel de navegación izquierdo, haz clic en "Subnets".  
   
4. **Crea una nueva subred**  
  
   Haz clic en el botón "Create subnet". Esto te llevará a una nueva página.  
   
5. **Configura tu subred**  
  
   Aquí es donde especificarás las configuraciones para tu subred.  
  
   - En el campo "Name tag", introduce un nombre para tu subred. Por ejemplo, "publica" para la primera subred.  
     
   - En el campo "VPC", selecciona la VPC que acabas de crear en los pasos anteriores.  
     
   - En el campo "Availability Zone", puedes seleccionar una zona de disponibilidad específica o dejarla en "No preference" para que AWS la elija por ti.  
     
   - En el campo "IPv4 CIDR block", introduce el rango de direcciones IP para tu subred. Para la subred 'publica', el rango es 10.0.0.0/24.  
   
6. **Crea la subred**  
  
   Una vez que hayas configurado todo según tus necesidades, haz clic en "Create". AWS ahora creará una nueva subred con las configuraciones que especificaste.  
   
7. **Repite los pasos para las subredes 'frontend' y 'backend'**  
  
   Sigue los mismos pasos para crear las subredes 'frontend' y 'backend', asegurándote de darles los nombres y rangos de direcciones IP correctos (10.0.1.0/24 para 'frontend' y 10.0.2.0/24 para 'backend').  
   
Una vez que hayas seguido estos pasos, tendrás tus tres subredes creadas dentro de tu VPC. Recuerda que por el momento, todas las subredes son privadas. En pasos posteriores, configuraremos la subred 'publica' para que pueda aceptar tráfico de Internet.