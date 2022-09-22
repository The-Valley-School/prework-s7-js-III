>[DIAPOSITIVAS](S7-recursos/introduccion.pdf)

---

Bienvenidos a la séptima sesión del prework. En esta sesión seguimos trabajando con javascript con el objetivo de aprender:

- Qué son las funciones y cómo trabajar con ellas
- El DOM y la formas de modificarlo
- Eventos que nos permitirán mayor interacción en nuestra página.

## ¿QUÉ SON LAS FUNCIONES?

Podemos entender las funciones en javascript como un bloque de código que realiza un procedimiento. Un conjunto de instrucciones, líneas de código, que realizan una tarea concreta, como calcular un valor. Para que estos bloques sean considerados funciones, tienen que tener una entrada y devolver un salida que tenga una relación obvia.

Sin darnos cuenta, ya hemos estado trabajando con funciones,

```js
console.log("esto es una función");
```

La función console.log es una función que recibe un valor (”esto es una función”) y devuelve una acción en consonancia que es pintar por consola la frase que ha recibido.

## DECLARACIÓN DE FUNCIONES

Vamos a seguir entendiéndolo mejor con otro ejemplo y así aprendemos a declararlas.

```
let valorA = 30;
let valorB = 50;

// Creamos nuestra función
function suma(num1, num2) {
	return num1 + num2;
}

// Utilizamos nuestra función
let resultado = suma(valorA, valorB); // Aquí estamos llamando a nuestra función
console.log(resultado); // Mostramos por consola el resultado
```

La sintaxis para la declarar una función  es la siguiente:

```js
function NOMBRE_FUNCION (ARGUMENTO1, ARGUMENTO2, ..., ARGUMENTO N) {
	return INFO_DEVUELTA;
}
```

- Tenemos la palabra **function** que es una palabra reservada que utilizamos para crear las funciones.
- Tenemos el **NOMBRE_FUNCION** que será un nombre descriptivo de lo que hace esa función. No puede haber dos funciones con el mismo nombre
- **(ARGUMENTO1, ARGUMENTO2, ..., ARGUMENTO N)** que son los denominados parámetros o argumentos. Es la información que entra a la función y con la que trabajaremos, podemos usar el nombre que queramos.
- **return** es la palabra que utilizamos para devolver la información, la salida de la función. Tenemos que intentar que las funciones que hagamos tengan return
- **{}** Los corchetes indican el cuerpo de la función

Ahora que ya la tenemos declarada podemos hacer uso de ella, tan sencillo como poner el nombre y entre paréntesis los argumentos de entrada.

```js
NOMBRE_FUNCION(ARGUMENTO1, ARGUMENTO2, ..., ARGUMENTO N);
```

 Puede darse el caso que existan funciones tan sencillas que no necesiten parámetros de entrada. En este caso no pasaría nada, dejaríamos vacíos los paréntesis.

```js
// Declaración

function NOMBRE_FUNCION () {
	return INFO_DEVUELTA;
}

// Uso
NOMBRE_FUNCION ();
```

¿Y si no proporciono el argumento? Pongamos otro ejemplo:

```js
function mostrarEntrada(pelicula, precio) {
	console.log(película + ' ' + precio);
}

entradaCine('Titanic');
```

Todos los valores que no incluyamos se volverán **undefined.** 

```
"Titanic undefined" //Esto es lo que saldrá por consola.
```

La no existencia de parámetros podemos controlarlo dentro de la función, por ejemplo, asignando un precio estándar en caso de que no nos llegue.

```js
function mostrarEntrada(pelicula, precio) {
	if(precio === undefined){
		precio = 10;		
	}
	console.log(película + ' ' + precio);
}

entradaCine('Titanic');

//Mostrará por pantalla "Titanic 10"
```

A realizar unos cuantos ejercicios con los que asentemos conocimientos.
