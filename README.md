


# Example shopping cart using addEventListener, Map and template.

##template
```html
    <template id="template">
            <li class="list-group-item d-flex justify-content-between aling-items-center">
                <span class="lead">Strawberry</span>
                <span class="badge bg-primary rounded-pill">12</span>
            </li>
        </template>
```
```js
document.addEventListener('click', e => {
    // console.log(e.target.matches(".card .btn-outline-primary"));
    if (e.target.matches(".card .btn-outline-primary")) {
        // console.log('ejecutar agregar al carro')
        agregarCarrito(e)
    }
    // console.log(e.target.matches(".list-group-item .btn-success"))
    if (e.target.matches("#carrito .list-group-item .btn-success")) {
        btnAumentar(e)
    }

    if (e.target.matches("#carrito .list-group-item .btn-danger")) {
        btnDisminuir(e)
    }
})

    const btnAumentar = (e) => {
        console.log('me diste click', e.target.dataset.id)
        carritoObjeto = carritoObjeto.map(item => {
            if (item.id === e.target.dataset.id) {
                item.cantidad++;
            }
            return item;

        })
        pintarCarrito();
    }
```
## Try Shopping cart at: 
### Have a nice day. Thank you for stopping by!