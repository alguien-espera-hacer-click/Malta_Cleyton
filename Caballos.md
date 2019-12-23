# Caballos
### Metodología de diseño 
 `MVC`
### IDE de desarrollo
`Visual Studio 2019`

### Herramientas utilizadas
`JetBrains`

### Lenguajes
`css 3` `(bootstrap v3.3.7)`

`html 5` 

`js` `(Jquery 3.1.1)`

`c# .net framework 4.6.1`

### Base de datos.

administrada por maltaCleyton.

### Notas importantes:

- No se cuenta con un código fuente, por lo que para hacer cambios se debe modificar el código compilado. En el caso del FrontEnd no es necesario usar herramientas de descompilación (`JetBrains`), sin embargo para el BackEnd si es necesario usar este tipo de herramientas, el contratiempo más grande es que Al descompilar el código se mostrará Cifrado.
- El foro es un WordPress, por lo tanto el foro y la página tiene diferentes características en su alojamiento para funcionar, el foro se inserta por medio de un *\<frame\>* que se dirige a WordPress administrado por Alguien espera hacer click S.C, por lo que en la soloCaballos encontrará la página WordPress comprimida y la base datos que deberá desplegar en el nuevo dominio, este debe seguir las características de WordPress, al tener en línea el foro debe cambiar la propiedad src del frame de la página **foro.html** que se encuentra en la carpeta raíz, esto se hizo así ya que no se puede modificar los archivos controller de la página. Una vez modificado debe habilitar la última opción del menú  en **_Layout.cshtml**.
- Para añadir o modificar los pop up ingrese a http://www.solocaballos.com.mx/popups
- Para cambiar o añadir noticias en la sección de noticias, ingrese a http://www.solocaballos.com.mx/blog, consulte el archivo contraseñas del drive.

### Acciones a considerar 

- El Geolocalizador utiliza un archivo csv, ubicado en la carpeta Raíz\Content\assets\docs\distribuidores.csv por lo que si un distribuidor solicita cambios se debe descargar el archivo modificarlo y volverlo a subir, los sitios de http://maltacleyton.com.mx/ y http://acuacultura.com.mx/ utilizan una copia del mismo archivo por lo que si se desea que las tres páginas tengan los mismo distribuidores con los mismo cambios se debe modificar cada de estos archivos.
- El geolocalizador necesita un certificado SSL para funcionar, según la documentación de la api de google maps.

### Accesos wp-admin para foro
vea el archivo contraseñas en el drive.
