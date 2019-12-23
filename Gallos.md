# Gallos
El dominio gallos.com.mx aparece como sitio en mantenimiento, sin embargo el sitio de pruebas es un WordPress, por lo tanto  la página de pruebas y el sitio en  productivo tienen diferentes características en su alojamiento para funcionar, la página de pruebas se iba a  insertar por medio de un`<frame>` que se dirige a WordPress administrado por Alguien espera hacer click S.C, por lo que en el drive encontrará en la carpeta Gallos la página WordPress y la base datos que deberá desplegar en el nuevo dominio, este debe seguir las características de WordPress, al tenerlo en línea y ser aprobada por maltaCleyton para su vista en producción se debe cambiar la propiedad src del `<frame>` de la  página `index.html` que se encuentra en la carpeta raíz de http://gallos.com.mx/

### Características del sitio
`CMS WordPress`,

**lenguajes**, `php`; `css`;  `html` y `javascript`,

`Gestor phpmyadmin`

### Notas importantes:

- La calculadora es una integración independiente de WordPress por lo que se encuentra en la carpeta `Calculadora` en la carpeta raíz del sitio, está basada en la calculadora de porción alimenticia de la página http://maltacleyton.com.mx/ , antes de ponerla en productivo debe modificar las cantidades de días de consumo y periodo de consumo.
- Foro ya integrado en WordPress.

### Acciones a considerar 

Para poner el sitio en productivo debe eliminar la siguiente etiqueta 
```html
<section class="page1">
	<div class="huge-title centered">
	  <h1 style="font-family:'Raleway', sans-serif; font-size:24px; letter-spacing:4px; font-weight:600;">
      <img alt="YOURLOGO" src="img/logo-phone.png"><br><br> SITIO EN MANTENIMIENTO
    </h1>
  </div>
</section>
```
y descomentar lo siguiente, también debe cambiar la propiedad src del frame

```html
<!--<iframe id="marco" src="" target="_self" style="border: 0; position:absolute; top:0; left:0; right:0; bottom:0; width:100%; height:100%">-->
```
Por último reemplace el texto marcado `{nuevo Dominio}` del siguiente script por el nombre del nuevo dominio en donde se encuentra la página Wordpress.
```js
  var frame=document.getElementById('marco');
  var sPaginaURL = window.location.search.substring(1);
  var sURLVariables = sPaginaURL.split('&');
  console.log(frame);
  for (var i = 0; i < sURLVariables.length; i++) {
    var sParametro = sURLVariables[i].split('=');

    if (sParametro[0] == "pre_starter") {
      frame.src="http://{nuevo Dominio}/pre-starter";
    }
  }
### Accesos wp-admin para foro
vea el archivo contraseñas en el drive.

