# Respuestas - Tarea Multimedia y Formularios

## Parte 2 - Medición de imágenes

| Formato    | Peso en KB | ¿Se ve peor? | ¿Dónde exactamente? 
|------------|------------|--------------|---------------------
| Original   | 97.3 KB    |     No       | No presenta perdida de calidad. 
| JPG        | 97.3 KB    |     No       | La calidad es practicamente igual a la imagen original. 
| PNG        | 911 KB     |     No       | Conserva la calidad pero el archivo es mucho mas pesado. 
| WebP       | 34.7 KB    |     No       | Mantiene una buena calidad con un tamaño de archivo menor. 
| AVIF       | 54.5 KB    |     No       | Conserva buena calidad y reduce considerablemente el tamaño del archivo. 

### 1. ¿Cuál eligió para su hoja de vida y por qué?

Elegí el formato AVIF como formato principal porque ofrece una buena calidad de imagen con un tamaño de 54.5 KB, aunque picture elige la mejor opcion segun el navegador

### 2. ¿El resultado se parece al de la imagen de clase o salió distinto?

Mi resultado fue un poco similar al de la imagen de clase, esto se debe a que cada imagen tiene caracteristicas distintas, como la resolucion, los colores y la cantidad de detalles, no note mayor diferencia entre los distintos tipos de imagenes, solo minimo cambio en los colores y resolucion. 


# Parte 3 - Investigación

## Pregunta 1
# Su formulario tiene un campo de fecha con un calendario que aparece al hacer clic. Averigüe si ese calendario se puede cambiar de color, de tamaño o de tipografía. Explique qué encontró y por qué es así. #
basicamente no es posible cambiar la aparienicia del calendario de date, esto es por la compatibilidad de navegadores y del dispositivo, cada navegador tiene su forma y estilos para esta entrada. aunque existe forma de aplicar diseño a los controles de formulario con la propiedad CSS -webkit-appearance o el selector de pseudoclase ::-webkit-foo. Sin embargo, la ventana emergente del calendario no proporciona esas formas en WebKit porque está separada del documento, como un menú emergente para " select, y actualmente no hay un estándar para controlar el diseño de sus subelementos

# Fuentes: #
https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/input/date#compatibilidad_con_navegadores

https://es.stackoverflow.com/questions/229840/estilo-datepicker-en-un-input-tipo-fecha-date

https://developer.chrome.com/blog/quick-faqs-on-input-type-date-in-google-chrome?hl=es-419#how_do_i_change_the_appearance_of_the_date_picker


## Pregunta 2
# En clase escribió required y min en su HTML. Averigüe qué son :valid e :invalid, y explique qué relación tienen con esos atributos que ya escribió. #

:valid 
La pseudo-clase :valid de CSS representa cualquier elemento de input u otro elemento form que su contenido se valide satisfactoriamente. Esto permite que los campos validos adopten facilmente una apariencia que ayuda al usuario a confirmar que sus datos esten ingresados correctamente.

:invalid
La pseudo-clase :invalid de CSS representa cualquier elemento input u otro elemento form cuyos contenidos no se puedan validar. como por ejemplo en mi formulario, el campo de la hora sera :invalid si el usuario selecciona 07:30 am, ya que el valor minimo permitido es 08:00 am.

:valid indica que el dato cumple las reglas de validacion y :invalid indica que no las cumple. Son complementarias y no iguales.

fuentes: 
https://developer.mozilla.org/es/docs/Web/CSS/Reference/Selectors/:valid
https://developer.mozilla.org/es/docs/Web/CSS/Reference/Selectors/:invalid

## Pregunta 3
# Su img tiene width y height con las dimensiones reales del archivo. Si esa imagen se abre en un teléfono, va a salirse de la pantalla. Averigüe qué hace falta para que se adapte al ancho disponible, y por qué no alcanza con cambiar los números del width. # 

para que se adapte a cualquier pantalla debe reducirse de tamaño segun el espacio disponible, para mantenerse dentro de la pagina y no desbordarse. Para esto se puede usar CSS con max-width: 100% y height: auto. No basta solo con cambiar los numeros de width y height, porque esos valores siguen siendo medidas fijas; en cambio, el CSS permite que la imagen se ajuste automáticamente al ancho disponible de cada pantalla.

fuentes: 
https://developer.mozilla.org/es/docs/Web/HTML/Guides/Responsive_images
https://www.w3schools.com/css/css_rwd_images.asp?utm_source=chatgpt.com
