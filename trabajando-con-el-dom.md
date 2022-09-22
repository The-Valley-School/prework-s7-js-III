## EJERCICIO 1

```js
/*
	Dado el siguiente HTML:
	<body>
		<h2> Hola Don Pepito <h2>
	</body>
		
	Modificar el texto de la etiqueta h1 por "Hola Don José" 
*/

let elementoH2 = document.querySelector('h2');
elementoH2.textContent = 'Hola Don José';
```

## EJERCICIO 2

```js
/*
	Dado el siguiente HTML:
	<body>
		<div id="contenedor">
		</div>
	</body>
		
	Crea una lista con los elementos del siguiente array:
	['Homer','Lisa','Marge','Bart']
*/

let listado = ['Homer','Lisa','Marge','Bart'];

let elementoContenedor = document.getElementById('contenedor');
let elementoLista = document.createElement('ul');

for ( let i = 0; i < listado.length; i++){
    let elementoItem = document.createElement('li');
    elementoItem.textContent = listado[i];

    elementoLista.appendChild(elementoItem);
}

elementoContenedor.appendChild(elementoLista);

```

## EJERCICIO 3

```js
/*
	Dado el siguiente HTML:
	<body>
		<div id="contenedor">
		</div>
	</body>
		
	Crea dos listados, uno con las palabras que tengan más de 5 letras, otros 
	con el resto
	['VERDE','AMARILLO','AZUL','MARRÓN','ROJO','NARANJA']
*/

let listado = ['VERDE','AMARILLO','AZUL','MARRÓN','ROJO','NARANJA'];

let elementoContenedor = document.getElementById('contenedor');
let elementoLista1 = document.createElement('ul');
let elementoLista2 = document.createElement('ul');

for ( let i = 0; i < listado.length; i++){
    let elementoItem = document.createElement('li');
    elementoItem.textContent = listado[i];
    if(listado[i].length > 4){
        elementoLista1.appendChild(elementoItem);
    } else{
        elementoLista2.appendChild(elementoItem);
    }
}

elementoContenedor.appendChild(elementoLista1);
elementoContenedor.appendChild(elementoLista2);
```

## EJERCICIO 4

```js
/*
	Dado el siguiente HTML:
	<body>
		<h1>El texto tiene que estar en rojo</h1>
		<h2>El texto tiene que estar en verde</h2>
		<h1>El texto tiene que estar en rojo</h1>
		<h2>El texto tiene que estar en verde</h2>
	</body>
		
	Cambia el color de las etiquetas según indica el html
*/

let elementosH1 = document.querySelectorAll('h1');
let elementosH2 = document.querySelectorAll('h2');

function changeColor(elementos, color) {
    for (let i = 0; i < elementos.length; i++){
        elementos[i].style.color = color;
    }
}

changeColor(elementosH1,'red');
changeColor(elementosH2,'green');
```
