# aplicación multicapa en una red privada virtual (VPC).

Esta VPC se configurará con el rango 10.0.0.0/16 y contendrá tres subredes.

**Subred Pública**

La primera subred se llamará 'publica' y tendrá el rango 10.0.0.0/24. Al ser una subred pública, permite la entrada y salida de tráfico de Internet.  
   
En esta subred, ubicaremos un Application Load Balancer (ALB). Un ALB se utiliza para distribuir automáticamente el tráfico entrante de Internet entre múltiples instancias EC2, permitiendo así una alta disponibilidad y escalabilidad. En este caso, el ALB se configura para dar acceso a las dos instancias EC2 que contienen el frontend de la aplicación.  
   
Además, en esta subred publica, tendremos una máquina virtual Windows 2022 a la que se podrá acceder a través de RDP desde Internet. Esta máquina tendrá acceso total a las redes frontend y backend, permitiendo así la administración y resolución de problemas de las instancias en estas redes.  
   
Además, en la subred pública, configuraremos un NAT Gateway. Un NAT Gateway permite que las instancias en una subred privada accedan a Internet para actualizaciones y otras tareas, pero impide que el tráfico de Internet inicie una conexión con esas instancias.  
   
**Subred Frontend**  
   
La segunda subred se llamará 'frontend' y tendrá el rango 10.0.1.0/24. Esta es una subred privada que alberga las instancias EC2 que ejecutan la aplicación Node.js.  
   
Las instancias EC2 en esta subred se configurarán para publicar en el puerto 8080. Sin embargo, para que estas aplicaciones sean accesibles desde Internet a través del puerto 80 (HTTP), se configurará el ALB en la subred pública para reenviar el tráfico del puerto 80 al puerto 8080 en las instancias EC2.  
   
Además, estas instancias EC2 serán accesibles desde la subred pública a través del puerto 22 para SSH. Esto permite la administración y resolución de problemas de estas instancias.  
   
**Subred Backend**  
   
La tercera subred se llamará 'backend' y tendrá el rango 10.0.2.0/24. Esta es una subred privada en la que ubicaremos una instancia RDS MySQL.  
   
RDS es un servicio administrado que se encarga de tareas como el mantenimiento del sistema operativo, la configuración de MySQL y la realización de copias de seguridad. A esta instancia RDS se le permitirá el acceso desde la subred frontend y la subred pública para las operaciones de la base de datos.  
   
