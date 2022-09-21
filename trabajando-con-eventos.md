**EJERCICIO 1**

```js
/*
	Crea un programa que cuando pulses el botón 'Ver GIF' muestre un gif y a su vez
  elimine el botón
*/

/* JS */ 

let elementoBtn= document.querySelector('button'); 
elementoBtn.addEventListener('click', mostrarGIF);

function mostrarGIF (){
    let elementoImg = document.createElement('img');
    elementoImg.setAttribute('src','./imagen.gif');

    let elementoBody = document.querySelector('body');
    elementoBody.textContent = '';
    elementoBody.appendChild(elementoImg);
}

//HTML

<body>
    <button id="btn">Pulsa para ver un GIF</button>
</body>
```

**ELERCICIO 2**

```js
/*
	Contador. Crea un programa con un botón + y otro - que vaya sumando o restando
	números al 100 según vayas pulsando.
*/

/* JS */

let numero = 100;

elementoBtnSuma = document.getElementById('btnSuma'); 
elementoBtnResta = document.getElementById('btnResta'); 
elementoP = document.getElementById('numero'); 

elementoBtnSuma.addEventListener('click', function () { operacion('suma')});
elementoBtnResta.addEventListener('click', function () { operacion('resta')});

function operacion (valor) {
    if(valor == 'suma'){
        numero += 1;
    } else {
        numero -= 1;
    }
    elementoP.textContent = numero;
}

/* HTML */

<body>
    <p id="numero"> 100 </p>
    <button id="btnSuma">+</button>
    <button id="btnResta">-</button>
</body>
```

**EJERCICO 3**

```js
/*
Teniendo un array de colores: ['green', 'red', 'blue', 'yellow'];
Y un html:
	<body>
		<h2>Soy un texto que cambia de color<h2>
	</body>

Generar dinámicamente botones para cada elemento del array que al pulsarlos pinten 
del color que contienen el texto.
*/

let colores = ['green', 'red', 'blue', 'yellow'];

let elementoH2= document.querySelector('h2'); 
let elementoBody = document.querySelector('body');

function crearBotones (colores){
    for (let i = 0; i < colores.length; i++) {
        let elementoBtn = document.createElement('button');
        elementoBtn.textContent = colores[i];
        elementoBtn. addEventListener('click', function() { pintarTexto(colores[i])});
        elementoBody.appendChild(elementoBtn);
    }
}

function pintarTexto(color){
    elementoH2.style.color = color;
}

crearBotones(colores);

```
