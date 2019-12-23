# Círculo Api-Malta
Este proyecto esta basado en la página http://catalogo.maltacleyton.com.mx/ (http://fidelidad.alopruebas.com.mx/index.html)
En la carpeta **Circulo Api-Malta** encontrará el código fuente hasta la ultima modficación emitida por maltaCleyton, tome encuenta que 
este proyecto es similar que Plan de Lealtad, sin embargo debe tomarlo  como dos diferentes tanto la base de datos como el código fuente sufrierón modificaciones ya que se integrarón nuevas funciones.

### Modificaciones en contraste a Plan de Lealtad

- Integración de productos maltaCleyton a cambio de puntos, tenga en cuenta que solo los puntos de venta pueden adquirir este producto y que no se envían por el servicio Estafeta.
- Registro de Puntos de venta con código BIENVENIDA.
- Proceso de recuperación de contraseñas en el inicio de sesión.
- Cambio en página base.html por (Tabla productos de alimentos participantes).
- Integración de caje de precintos.
- Integración del sistema de cúpones, si un punto de venta elije un alimento este deberá ser intercambaido como cupón con su distribuidor maltaCleyton mas cercano.
- Integración de aceptación de términios y condiciones al registrarse y/o iniciar sesión.

### Características del sitio

- servicio de alojamiento Windows Server panel de control plesk 12.5,
- Gestor SQL Server Expres administrado con myLittleAdmin.
- Lenguaje de programación `c#`, `css (bootstrap)` y `javasrcipt(jquery)`.
- Completo desacoplamiento entre FrontEnd y BackEnd.
- comunicación asíncrona, el BackEnd es una web api alojada en el mismo dominio, ver documentación técnica de plan de lealtad para su configuración.

### Base de datos
Revise la Carpeta **Círculo Api-Malta** y elija el fichero BD.

### Notas importantes:

- Este proyecto nunca estuvo en productivo.
- Para hacer modificaciones en el BackEnd debe usar el código fuente de la carpeta Back y al terminar la modificación debe publicar la Web Api en la carpeta Front.
- Antes de desplegar la página en el nuevo dominio modifique el archivo `Web.config` de la carpeta Back, Agregue la conexión a la base de datos y modifique el siguiente código:
```xml
 <appSettings>
    <add key="Mail-Subject-Buy" value="Compra realizada en Plan Lealtad maltaCleyton. "/>
    <add key="Mail-Template-Buy" value="Buy.html"/>
    <add key="Mail-Template-Bcc" value="  {pruebas@pruebas.com.mx}  "/>
    <add key="Mail-Subject-Buy-Detail" value="Nuevo pedido de un cliente. "/>
    <add key="Mail-Template-Buy-Detail" value="Buy-Detail.html"/>
    <add key="Mail-Template-Bcc-Detail" value="  {Correos en donde llegarán los correos de detalles de compra}  "/>
    <add key="Mail-Subject-New-User" value="Bienvenido a Plan Lealtad maltaCleyton"/>
    <add key="Mail-Template-New-User" value="AddUser.html"/>
    
    <add key="Mail-Subject-Contact" value="Contacto Plan Lealtad maltaCleyton"/>
    <add key="Mail-Template-Contact" value="Contact.html"/>
    <add key="Mail-Template-Contact-Email" value="  {pruebas@pruebas.com.mx}  "/>
	  
    <add key="Mail-From" value="fidelidad@maltacleyton.com.mx"/>
    <add key="Mail-Port" value="587"/>
    <add key="Mail-Credentials-User" value="  {Usuario Servidor de Correo}  "/>
    <add key="Mail-Credentials-Password" value="   {Contraseña Servidor de Correo}  "/>
    <add key="Mail-Host" value="    {Servidor de correo}    "/>
  </appSettings>
```
**Nota:** Cambie los correos pruebas@pruebas.com.mx y reemplace los textos entre {} según corresponda.

Al terminar la modificación péguelo en el comentario <--PEGAR AQUÍ--> del `Web.config` en la carpeta Back->Services.
- Revise la documentación técnica para configurar correctamente los archivos `EndPoint.js` de la carpeta Front.
- Modifique los correos de los usuarios de prueba a los suyos en la base de datos.
- Modifique el correo del administrador en la base de datos.

### Acciones a considerar:

Después de subir el sitio y la base de datos, debe configurar el servidor de correo electrónico, para ello diríjase al administrador del sitio: 
**http(s)://nuevo_dominio/administrator->en el menú->Configuración**

Modifique el campo servidor, puerto, usuario y contraseña.
 
### Accesos 

Se recomienda cambiar los correos electrónicos pruebas@pruebas.com.mx y admin@admin.com.mx a los propios.
Vea el archivo contraseñas en el drive.


