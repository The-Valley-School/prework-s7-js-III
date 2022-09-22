## EJERCICIO 1

```js
/*
	Crea una función que calcule el descuento de una prenda sabiendo 
	el precio y el descuento
*/

function calcularPrecioDescuento(precio, descuento) {
	return precio - precio * ( descuento / 100 );
}

let precioFinal=calcularPrecioDescuento(120, 30);
console.log(precioFinal);

```

## EJERCICIO 2

```js
/*
	Crea una función que recibiendo un array de lista de la compra y un alimento nuevo
	añada ese alimento a la lista de la compra.
	Crea otra que sirva para sacar el último alimento
*/

let listaCompra = ['carne', 'pescado', 'jabón'];

function anadirElemento(lista, alimento) {
	lista.push(alimento);
}

anadirElemento(listaCompra, 'fruta');
console.log(listaCompra);

function eliminarElemento(lista) {
	lista.pop();
}

eliminarElemento(listaCompra);
console.log(listaCompra);

```

## EJERCICIO 3

```js
/*
	Debemos crear una función que reciba un objeto cliente.
	Si la suma de sus compras ha sido superior a 500 euros, el tipo de cliente
	pasa a ser VIP, si son inferiores el tipo de cliente será NORMAL

	Ejemplo de objeto cliente
	usuario = {
		nombre: "Fernando",
		apellido: "García",
		email: "fgarcia@mail.com",
		compras: [100, 20, 100, 50, 300],
		tipo: "NORMAL"
	};
*/

let usuario = {
		nombre: "Fernando",
		apellido: "García",
		email: "fgarcia@mail.com",
		compras: [100, 20, 100, 50, 300],
		tipo: "NORMAL"
};

function actualizarTipoCliente (cliente) {
	let suma = sumadorCompras(cliente.compras);	
	if(suma > 500 ){
		cliente.tipo = "VIP";
	} else { 
		cliente.tipo = "NORMAL";
	}
}

function sumadorCompras(compras){
	let sumaCompras = 0;
	for( let i= 0; i < compras.length; i++){
		sumaCompras += compras[i];
	}
	return sumaCompras;
}

actualizarTipoCliente (usuario);
console.log(usuario);

```
