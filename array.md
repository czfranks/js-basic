# Arrays

**Recordar:**
La funcion de _callback_ que produce un nuevo array de **Filter()**, **map()**, **forEach()**, **find()**, **every()**, etc, recibe 3 argumentos en el siguiente orden:

1. _currentValue_ : El elemento actual del array que se está procesando.
2. _index_: El índice del elemento actual dentro del array.
3. _array_: El array sobre el que se llama ++filter, map, find, etc.++

Ahora con estos conceptos veamos algunos ejercicios sobre el siguiente array:
```javascript
let articles = [
    { name: 'bike', price: 1600},
    { name: 'book', price: 14},
    { name: 'laptop', price: 5000},
    { name: 'keyboard', price: 400}
];
```
//

- **FILTER()**: retorna un nuevo array con los elementos que cumplen alguna condición, los elementos no son modificados.

> Escoger un número aleatorio de artículos del array.
```javascript
articles.filter(function(){ return Math.round( Math.random() )} );
```
> Escoger artículos que cumplen alguna restricción en algunos de sus atributos:
```javascript
articles.filter(function(article){ return article.price > 2000; } );
```
> Escoger artículos en posiciones pares, con respecto a las posiciones del array: 0_based:
```javascript
articles.filter(function(_, i){ return i%2 == 0; });
```
- **MAP()**:  retorna un nuevo array con los resultados de la función que le pasamos  y que es aplicada a cada uno de los elementos del array.

> Devolver en array solo el atributo **name** por cada elemento de **articles**:
```javascript
articles.map(function(value, index){return {name: value.name}; });

//si solo quisiéramos el contenido de -> name
articles.map(function(value, index){return value.name; });
```

> Devolver en array la concatenación de los valores de name y price en un string separado por un espacio.
```javascript
articles.map(function(value){return `${value.name} ${value.price}`; });
```
