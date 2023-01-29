# JsNotes

- [Variables](#variables)
- [Arrays](#arrays)
  * [Metodos de los arrays](#metodos-de-los-arrays)
    + [Quitar y agregar valores](#quitar-y-agregar-valores)
    + [Juntar con otro array o lista](#juntar-con-otro-array-o-lista)
    + [Para iterar por sus elementos](#para-iterar-por-sus-elementos)
    + [Para generar un nuevo array de forma iterativa](#para-generar-un-nuevo-array-de-forma-iterativa)
    + [Filtrar elementos](#filtrar-elementos)
- [Entrada y salida de datos](#entrada-y-salida-de-datos)
- [Bucles](#bucles)
  * [For](#for)
  * [For... in](#for-in)
  * [While](#while)


# Variables
Para almacenar valores individuales se utilizan variables y constantes. Js determina automaticamente de que tipo es el dato que almacena.
```js
let x = 35        // Number
const y = "Hola"  // String
```

Se puede comprobar el tipo de la variable almacenada con la palabra clave `typeof`
```js
console.log(typeof x)   // Number
console.log(typeof y)   // String
```

# Arrays
Para almacenar conjuntos de datos se suelen usar los arrays, que son listas de datos. Para crear un array
```js
let arr = []
let arr = new Array()  // Son equivalentes excepto si metemos un numero en los parentesis
let arr = [1, 2, 3, 4] // Se pueden inicializaral crearlos

alert(arr[0])          // Se accede a los valores con el oerador [n], donde n es el indice del dato deseado (empezando en 0)
```

## Metodos de los arrays
Suponemos que la variable `arr` es un array.

### Quitar y agregar valores
- push()
- pop()
- shift()
- unshift()

### Juntar con otro array o lista
```js
arr.concat(lista1, lista2...)
```

### Para iterar por sus elementos
Se usa `arr.forEach()`
```js
arr.forEach((item, index, array) => {
  // Funcion a aplicar en cada elemento
});
```

### Para generar un nuevo array de forma iterativa
Se usa `arr.map()`
```js
arr.map((item, index, array) => {
  // Se escriben las operaciones deseadas para cada valor del array y se hace un array nuevo con el valor de retorno
  return item+2     // Por ejemplo en este caso se generaria un array nuevo con los elementos de arr sumados a 2.
})
```

### Filtrar elementos
Se usa `arr.filter()`
```js
arr.filter((item, index, array) => {
  // Se mantienen en el array los elementos que cumplan la condicion logica que se especifique aqui
  return item > 3   // Por ejemplo aquii se mantendrian los elementos mayores que 3
})
```

# Entrada y salida de datos

```js
console.log(variable)               // Salida por consola
alert(variable)                     // Salida en notificacion del navegador
let input = prompt(variable)        // Entrada en notificacion del navegador. Siempre coge el dato como String.
```
# Bucles
## For
Bucle fundamental clasico. Se itera un numero especifico de veces y en cada iteracion aumenta un contador
```js
for (let i = 0; i < 10; i++) {
  // Se itera desde 0 hasta 9
  // En la variable i tenemos el numero de iteracion
}
```

## For... in
Si tenemos un array `let arr = [1,2,3,4]`, podemos iterar por sus elementos de la siguiente manera
```js
for (let elemento in arr) {
  // Cada iteracion tenemos el valor correspondiente en la variable elemento
}
```

## While
