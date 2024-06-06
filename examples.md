# Post

This allows us to create data

```javascript
const firebaseUrl = 'https://tu-app.firebaseio.com/tu-coleccion.json';

const nuevoElemento = {
  nombre: 'Ejemplo',
  descripcion: 'Descripción del ejemplo'
};

fetch(firebaseUrl, {
  method: 'POST',
  body: JSON.stringify(nuevoElemento)
})
.then(response => response.json())
.then(data => console.log('Elemento creado:', data))
.catch(error => console.error('Error al crear el elemento:', error));
```

# Read

```javascript
const firebaseUrl = 'https://tu-app.firebaseio.com/tu-coleccion.json';

fetch(firebaseUrl)
.then(response => response.json())
.then(data => console.log('Datos:', data))
.catch(error => console.error('Error al obtener datos:', error));
```