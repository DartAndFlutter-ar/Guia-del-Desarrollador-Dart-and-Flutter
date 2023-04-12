# Tipo List 

En Dart, una Li``st es una colección ordenada de objetos que puede contener cero o más elementos. Cada elemento en la lista se identifica por un índice entero que comienza en cero para el primer elemento y se incrementa en uno para cada elemento subsiguiente.

La sintaxis básica para crear una lista es la siguiente:

```dart
List<int> numeros = [1, 2, 3, 4, 5];
```

En este ejemplo, se crea una lista llamada `números` que contiene cinco enteros. La sintaxis utiliza corchetes [] para indicar que se trata de una lista y se separan los elementos por comas.

## Métodos Útiles

Entre las principales características de las listas en Dart se incluyen:

- **add(E elemento)**: Agrega el elemento especificado al final de la lista.
- **addAll(Iterable<E> elementos)**: Agrega todos los elementos especificados al final de la lista.
- **insert(int indice, E elemento)**: Inserta el elemento especificado en el índice especificado en la lista.
- **remove(Object elemento)**: Elimina la primera ocurrencia del elemento especificado de la lista.
- **removeAt(int indice)**: Elimina el elemento en el índice especificado de la lista.
- **clear()**: Elimina todos los elementos de la lista.
- **contains(Object elemento)**: Devuelve true si la lista contiene el elemento especificado.
- **indexOf(Object elemento, [int desde = 0])**: Devuelve el índice de la primera ocurrencia del elemento especificado en la lista, o -1 si no se encuentra.
- **lastIndexOf(Object elemento, [int desde])**: Devuelve el índice de la última ocurrencia del elemento especificado en la lista, o -1 si no se encuentra.
- **sublist(int desde, [int hasta])**: Devuelve una vista de la lista que contiene los elementos desde el índice especificado hasta el índice especificado (no inclusivo).
- **forEach(void f(E elemento))**: Ejecuta la función especificada para cada elemento de la lista.
- **map<R>(R f(E elemento))**: Devuelve una nueva lista que contiene los resultados de aplicar la función especificada a cada elemento de la lista.
- **where(bool f(E elemento))**: Devuelve una nueva lista que contiene solo los elementos de la lista para los que la función especificada devuelve true.
- **reduce(E combine(E valorPrevio, E elemento))**: Combina los elementos de la lista utilizando la función especificada y devuelve el resultado final.
- **sort([int f(E a, E b)])**: Ordena los elementos de la lista según el orden especificado por la función de comparación opcional.

```dart
// Ejemplo para el método add()
List<int> numeros = [1, 2, 3];
numeros.add(4);
print(numeros); // salida: [1, 2, 3, 4]

// Ejemplo para el método addAll()
List<int> numeros = [1, 2, 3];
numeros.addAll([4, 5, 6]);
print(numeros); // salida: [1, 2, 3, 4, 5, 6]

// Ejemplo para el método insert()
List<String> palabras = ['hola', 'mundo'];
palabras.insert(1, '!');
print(palabras); // salida: [hola, !, mundo]

// Ejemplo para el método remove()
List<int> numeros = [1, 2, 3, 4];
numeros.remove(3);
print(numeros); // salida: [1, 2, 4]

// Ejemplo para el método removeAt()
List<String> palabras = ['hola', 'mundo', '!'];
palabras.removeAt(2);
print(palabras); // salida: [hola, mundo]

// Ejemplo para el método clear()
List<int> numeros = [1, 2, 3];
numeros.clear();
print(numeros); // salida: []

// Ejemplo para el método contains()
List<String> palabras = ['hola', 'mundo'];
bool contieneHola = palabras.contains('hola');
print(contieneHola); // salida: true

// Ejemplo para el método indexOf()
List<int> numeros = [1, 2, 3, 4];
int indice = numeros.indexOf(3);
print(indice); // salida: 2

// Ejemplo para el método lastIndexOf()
List<int> numeros = [1, 2, 3, 4, 3];
int ultimoIndice = numeros.lastIndexOf(3);
print(ultimoIndice); // salida: 4

// Ejemplo para el método sublist()
List<int> numeros = [1, 2, 3, 4, 5];
List<int> sublista = numeros.sublist(1, 4);
print(sublista); // salida: [2, 3, 4]

// Ejemplo para el método forEach()
List<String> palabras = ['hola', 'mundo'];
palabras.forEach((palabra) => print(palabra)); // salida: hola, mundo

// Ejemplo para el método map()
List<int> numeros = [1, 2, 3];
List<String> numerosComoCadenas = numeros.map((numero) => numero.toString()).toList();
print(numerosComoCadenas); // salida: ['1', '2', '3']

// Ejemplo para el método where()
List<int> numeros = [1, 2, 3, 4, 5];
List<int> pares = numeros.where((numero) => numero % 2 == 0).toList();
print(pares); // salida: [2, 4]

// Ejemplo para el método reduce()
List<int> numeros = [1, 2, 3, 4];
int suma = numeros.reduce((valorPrevio, numero) => valorPrevio + numero);
print(suma); // salida: 10

// Ejemplo para el método sort()
List<int> numeros = [3, 1, 4, 2];
numeros.sort();
print(numeros); // salida: [1, 2,

```
!!! Abstract "Resumiendo"

    Las listas en Dart son una herramienta muy útil para almacenar y manipular colecciones de objetos en un orden específico.