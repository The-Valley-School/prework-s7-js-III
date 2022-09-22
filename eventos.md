 Ya llevamos unas cuantos vídeos de JS donde hemos aprendido un montón de cosas (tipos de datos, bucles, funciones, DOM), aunque de momento no hemos ofrecido mucha interacción.

A lo largo de todos nuestros ejercicios ejecutamos el código javascript según se carga. En este video vamos a trabajar con EVENTOS que nos van a permitir que dad una acción, lancemos las funciones que les indiquemos. Por ejemplo, tenemos eventos de:

- **RATÓN**: Hacer click [click], pasar el ratón sobre un elemento [mouseover], sacar el ratón de un elemento [mouseout] …
- **TECLADO**: Cuando pulsamos por ejemplo una tecla [keypress]…
- **ELEMENTOS**: Cuando quitamos el foco [blur], lo ponemos [focus], cambiamos el contenido de un output [change]…
- **FORMULARIOS**: Cuando pulsamos el [submit] o el [reset]…
- **VENTANA:** Un cambio de tamaño [resize] o un scroll [scroll]

En esta sesión vamos a trabajar con el elemento CLICK, a lo largo del máster iremos profundizando en diferentes elementos.

## onclick

La forma más fácil de trabajar con el elemento CLICK es mediante el atributo **onclick** en HTML. 

Lo podemos usar en cualquier etiqueta, no hace falta que sea un botón.

```html
<body>
	<p>Si pulsas en el botón saldrá un mensaje por consola</p> 
	<button onclick="mensajeConsola()">Haz click</button>
</body>
```

```js
function mensajeConsola () {
	console.log('Aquí está el mensaje por consola');
}
```

## eventListener

Otra manera de tratar con eventos en JS sería mediante el uso de eventListeners, escuchadores de eventos. Lo que hacemos con ello es dejar preparada una función que salta cuando se produzca ese evento. Por ejemplo:

```html
<body>
	<p>Si pulsas en el botón saldrá un mensaje por consola</p> 
	<button id="btn">Haz click</button>
</body>
```

```js
function mensajeConsola () {
	console.log('Aquí está el mensaje por consola');
}

document.getElementById("btn").addEventListener("click", mensajeConsola);
```

A nivel de buenas prácticas, deberíamos usar estos eventos en lugar de el onclick y así mantener

toda la lógica en javascript.

En caso de que quisiésemos pasar argumentos mediante la función dentro del addEventListener debemos usar una función anónima para ello:

```js
document.getElementById("btn").addEventListener("click", funcion () { mensajeConsola ('Hola') });
```

¡Y ya tenemos interacción con el usuarios! En el siguiente vídeo practicamos.
