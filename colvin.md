>[ENUNCIADO](S7-recursos/enunciado-colvin.pdf)

>[SOLUCIÓN](S7-recursos/solucion-colvin.zip)

---

Unos amigos de una floristería, no han pedido si les podemos ayudar a hacer el siguiente módulo.

La idea es que a partir de un array de objetos, pintemos botones por cada producto de manera dinámica, al pulsarlos irá apareciendo el producto en la parte derecha con una imagen, el precio y un botón de comprar. Al pulsarlo nos aparecerá un mensaje de ‘Gracias por tu compra’

Lo primero que haremos antes de trabajar con JS es maquetar la página.

 

```html
<section class="section">
        <header class="header">
            <img class="logo" src="./assets/logo.png">
        </header>
        <div class="container">
            <div class="productList">
                <button class="btn">RAMO DE ROSAS</button>
                <button class="btn">RAMO DE GIRASOLES</button>
                <button class="btn">LAVANDA</button>
                <button class="btn">BUGANVILLA</button>
                <button class="btn">CACTUS</button>
            </div>
            <div class="product">
                <img class="img-product" src ="./assets/cactus.png">
                <p class="price-producto"> 40.00€</p>
                <button class="btn-product">COMPRAR</button>
            </div>
        </div>
    </section>
```

```css
body{
    font-family: sans-serif;
}

.section {
    width: 600px;
    border: 2px solid #0C3938;
    margin: 20px auto;
    padding: 30px;
}

.header{
    border-bottom: 2px solid #0C3938;
    padding-bottom: 10px;
}

.logo {
    width: 150px;
}

.container{
    padding: 40px 0;
    display: flex;
    justify-content: left;
    align-items: flex-start;
}

.productList {
    width: 250px;
    height: 500px;
}

.product {
    border-left: 2px solid #0C3938;
    height: 500px;
    padding-left: 20px;
}

.btn{
    background-color: #0C3938;
    font-size: 16px;
    color: #fff;
    border: none;
    width: 200px;
    padding: 15px 0;
    margin:  5px;
}

.img-product{
    width: 300px;
}

.price-product{
    font-weight: bold;
    color: #0C3938;
}

.btn-product{
    border: 2px solid #0C3938;
    color: #0C3938;
    background-color: #fff;
    font-weight: bold;
    padding: 5px 20px;
}
```

Vamos ahora a crear dinámicamente la sección productlist:

```js
let elementProductList = document.querySelector('.productList');
let elementProduct = document.querySelector('.product');

function renderProductList (){
    for ( let i = 0; i <products.length; i++){
        let elementBtn = document.createElement('button');
        elementBtn.textContent = products[i].name;
        elementBtn.classList.add('btn');
        elementBtn.addEventListener('click', function(){ renderProduct (products[i])});
        elementProductList.appendChild(elementBtn);
    }
}
```

Y renderizamos los productos:

```js
function renderProduct(item){
    elementProduct.textContent = '';
    let elementProductImg = document.createElement('img');
    elementProductImg.setAttribute('src', item.urlImg);
    elementProductImg.classList.add('img-product');

    let elementProductPrice = document.createElement('p');
    elementProductPrice.textContent = item.price + '€';
    elementProductPrice.classList.add('price-product');

    let elementProductBtn = document.createElement('button');
    elementProductBtn.textContent = 'COMPRAR';
    elementProductBtn.classList.add('btn-product');
    elementProductBtn.addEventListener('click', purchase);

    elementProduct.appendChild(elementProductImg);
    elementProduct.appendChild(elementProductPrice);
    elementProduct.appendChild(elementProductBtn);
}
```

Y por último el mensaje de finalización de compra:

```js
function purchase(){
    elementProduct.textContent = '';
    let elementPurchase = document.createElement('p');
    elementPurchase.textContent = 'GRACIAS POR TU COMPRA';
    elementProduct.appendChild(elementPurchase);
}
```
