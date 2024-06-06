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

# Update

```javascript
const elementoId = 'ID_DEL_ELEMENTO_A_ACTUALIZAR';
const datosActualizados = {
  nombre: 'Nuevo nombre',
  descripcion: 'Nueva descripción'
};

const urlActualizar = `https://tu-app.firebaseio.com/tu-coleccion/${elementoId}.json`;

fetch(urlActualizar, {
  method: 'PATCH',
  body: JSON.stringify(datosActualizados)
})
.then(response => response.json())
.then(data => console.log('Elemento actualizado:', data))
.catch(error => console.error('Error al actualizar el elemento:', error));
```

# Delete

```javascript
const elementoIdAEliminar = 'ID_DEL_ELEMENTO_A_ELIMINAR';
const urlEliminar = `https://tu-app.firebaseio.com/tu-coleccion/${elementoIdAEliminar}.json`;

fetch(urlEliminar, {
  method: 'DELETE'
})
.then(() => console.log('Elemento eliminado con éxito'))
.catch(error => console.error('Error al eliminar el elemento:', error));

```