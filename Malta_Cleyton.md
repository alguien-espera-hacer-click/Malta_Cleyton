# Sitio maltaCleyton

El sitio de maltaCleyton se enfoca principalmente en el FrontEnd se utiliza  cshtml, css, bootstrap  y javascript para la gran mayoría de la operaciones de la página, su *Backend* solo contiene los controllers que retornan las vistas.

A diferencia de los demás proyectos de maltaCleyton, no se utiliza base de datos para crear el contenido de la página por lo que el contenido es estático.

### Metodología de diseño 
 `MVC`

### IDE de desarrollo
`Visual Studio 2019`
### Lenguajes

`css3`

`html 5`

`bootstrap v3.3.7`

`Jquery 2.1.1 y js`

`c# .net framework 4.6.1`

### Base de datos.

El sitio actual no contiene conexión a base de datos, sin embargo la versión anterior del sitio si tenía una base de datos administrada por maltaCleyton.

##Notas importantes

- El código fuente en el repositorio es un poco diferente al código compilado que está en producción, la diferencia es completamente visual, las artes del slider, banner y menú corresponden a la última campaña para puntos de venta **Círculo Api-Malta**, proyecto que se quedo en espera para su lanzamiento a producción, razón por la cual es diferente al productivo.
- La calculadora de porción alimenticia está hecha en js documento `main.js` .
- Los formulario de Contacto y Vuélvete distribuidor son de salesforce, administrado por maltaCleyton.

## Acciones a considerar 

- Por su carencia de una a conexión a base de datos, El Geolocalizado utiliza un archivo csv, ubicado en la carpeta Raíz\Content\docs\distribuidores.csv por lo que si un distribuidor solicita cambios se debe descargar el archivo modificarlo y volverlo a subir, los sitios de http://acuacultura.com.mx/ y http://solocaballos.com.mx/ utilizan una copia del mismo archivo por lo que si se desea que las tres páginas tengan los mismos distribuidores con los mismo cambios se debe modificar cada uno de estos archivos.
  *El archivo distribuidores_old.csv es un respaldo.*
- El nombre de las imágenes de los slider deben ser numéricos, dependiendo en qué posición van a aparecer se deben modificar los demás nombres de los slider existentes si es necesario.
- Modificar los textos `{Host}` `{Port}` `{UserName}` `{Password}` en el metodo sendEmailPtv línea 169 archivo HomeController.
