# Acuacultura
## Metodología de diseño 
`MVC`
## IDE de desarrollo
`Visual Studio 2019`
## Lenguajes
`css 3` (`bootstrap v3.3.7`)

`html 5`

`js` (`Jquery 2.1.1`)

`c# .net framework 4.6.1`
## Base de datos.

administrada por maltaCleyton.

## Acciones a considerar 

- El Geolocalizador utiliza un archivo csv, ubicado en la carpeta raíz\Content\assets\docs\distribuidores.csv por lo que si un distribuidor solicita cambios se debe descargar el archivo modificarlo y volverlo a subir, los sitios de http://maltacleyton.com.mx/ y http://solocaballos.com.mx/ utilizan una copia del mismo archivo por lo que si se desea que las tres páginas tengan los mismo distribuidores con los mismo cambios se debe modificar cada de estos archivos.
- El geolocalizador necesita un certificado SSL para funcionar, según la documentación de la  api google maps.
