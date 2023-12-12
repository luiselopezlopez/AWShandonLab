Crear y configurar un NAT Gateway en AWS permite a las instancias en subredes privadas acceder a Internet para descargar actualizaciones, por ejemplo, mientras impide que el tráfico de Internet inicie una conexión con esas instancias.  
   
Aquí te dejo los pasos para configurar un NAT Gateway en tu subred 'publica':  
   
1. **Inicia sesión en tu cuenta de AWS**  
  
   Accede a la consola de administración de AWS.  
   
2. **Navega hasta el servicio de VPC**  
  
   En la consola de administración de AWS, encuentra el menú de servicios y selecciona "VPC".  
   
3. **Accede a la sección de NAT Gateways**  
  
   En el panel de navegación izquierdo, haz clic en "NAT Gateways".  
   
4. **Crea un Internet Gateway y anexalo a la VPC**

NAT Gw Necesita un Internet GW para funcionar.

4. **Crea un nuevo Elastic Public IP**  

NAT GW Necesita una IP Publica que define la IP de Salida.

4. **Crea un nuevo NAT Gateway**  
  
   Haz clic en "Create NAT Gateway". Esto te llevará a una nueva página.  
   
5. **Configura tu NAT Gateway**  
  
   Aquí es donde especificarás las configuraciones para tu NAT Gateway.  
     
   - En el campo "Subnet", selecciona la subred 'publica' donde quieres ubicar el NAT Gateway.  
     
   - En el campo "Elastic IP Allocation ID", debes proporcionar una dirección IP elástica. Si no tienes una, haz clic en "Allocate New EIP" y AWS creará una nueva dirección IP elástica para ti.  
   
6. **Crea el NAT Gateway**  
  
   Una vez que hayas configurado todo según tus necesidades, haz clic en "Create a NAT Gateway". AWS ahora creará un nuevo NAT Gateway con las configuraciones que especificaste.  
   
