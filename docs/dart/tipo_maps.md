# Tipo Maps

En Dart, un `Map` es una estructura de datos que almacena pares de valores **clave-valor**. Cada elemento del mapa tiene una **clave** única que se utiliza para acceder al valor asociado.

Los `Map` en Dart son similares a los `diccionarios` en otros lenguajes de programación. Los elementos de un Map se pueden acceder y modificar mediante la **clave**. Las **claves** pueden ser de cualquier tipo, siempre y cuando el tipo sea compatible con el operador de igualdad `==`. Los valores también pueden ser de cualquier tipo.

Para crear un Map en Dart, se puede utilizar la siguiente sintaxis:

```dart
var mapa = {
  'clave1': valor1,
  'clave2': valor2,
  // ...
};

```

También se puede crear un Map vacío y luego agregar elementos:

```dart
var mapa = Map<String, int>();
mapa['clave1'] = 1;
mapa['clave2'] = 2;

```

Para acceder a un valor en un Map, se utiliza la clave correspondiente:

```dart
print(mapa['clave1']); // Imprime 1
```

Si se intenta acceder a una clave que no existe en el Map, se devuelve `null`.

También se pueden recorrer todos los elementos de un Map utilizando un ciclo `for`:

```dart
for (var clave in mapa.keys) {
  print('$clave: ${mapa[clave]}');
}

```

## Métodos Útiles

Además, Dart proporciona muchos métodos útiles para trabajar con Mapas, como:

- **[]**: Accede al valor asociado con la clave especificada.
- **[]=**: Asigna un valor a una clave específica.
- **length**: Devuelve el número de elementos en el Map.
- **keys**: Devuelve una lista que contiene todas las claves en el Map.
- **values**: Devuelve una lista que contiene todos los valores en el Map.
- **isEmpty**: Devuelve true si el Map está vacío.
- **isNotEmpty**: Devuelve true si el Map no está vacío.
- **containsKey**: Devuelve true si el Map contiene la clave especificada.
- **containsValue**: Devuelve true si el Map contiene el valor especificado.
- **forEach**: Ejecuta una función para cada clave-valor en el Map.
- **putIfAbsent**: Asigna un valor a una clave solo si la clave no existe en el Map.
- **remove**: Elimina la entrada correspondiente a una clave del Map.
- **clear**: Elimina todas las entradas del Map.
- **update**: Actualiza el valor correspondiente a una clave en el Map.
- **updateAll**: Actualiza todos los valores del Map utilizando una función proporcionada.
- **map**: Crea un nuevo Map aplicando una función a cada entrada del Map original.
- **toString**: Devuelve una cadena que representa el Map.

Hay muchos más métodos disponibles en la clase Map de Dart, pero estos son algunos de los más comunes y útiles.

[https://dart.dev/language/collections#maps](https://dart.dev/language/collections#maps){target=_blank}

``` dart
// Crear un Map vacío
Map<String, int> miMapa = {};

// Agregar elementos al Map
miMapa['Manzanas'] = 10;
miMapa['Naranjas'] = 5;
miMapa['Plátanos'] = 7;

// Acceder a un valor en particular
print(miMapa['Manzanas']); // 10

// Obtener una lista de todas las claves
List<String> claves = miMapa.keys.toList();
print(claves); // ['Manzanas', 'Naranjas', 'Plátanos']

// Obtener una lista de todos los valores
List<int> valores = miMapa.values.toList();
print(valores); // [10, 5, 7]

// Comprobar si el Map está vacío
print(miMapa.isEmpty); // false

// Comprobar si el Map no está vacío
print(miMapa.isNotEmpty); // true

// Comprobar si el Map contiene una clave específica
print(miMapa.containsKey('Manzanas')); // true

// Comprobar si el Map contiene un valor específico
print(miMapa.containsValue(5)); // true

// Iterar sobre cada clave-valor en el Map
miMapa.forEach((clave, valor) {
  print('$clave = $valor');
});

// Asignar un valor a una clave solo si la clave no existe en el Map
miMapa.putIfAbsent('Uvas', () => 3);

// Eliminar una entrada del Map
miMapa.remove('Naranjas');

// Eliminar todas las entradas del Map
miMapa.clear();

// Actualizar el valor correspondiente a una clave en el Map
miMapa.update('Manzanas', (valor) => valor + 2);

// Actualizar todos los valores del Map utilizando una función proporcionada
miMapa.updateAll((clave, valor) => valor * 2);

// Crear un nuevo Map aplicando una función a cada entrada del Map original
Map<String, int> nuevoMapa = miMapa.map((clave, valor) {
  return MapEntry(clave.toUpperCase(), valor + 1);
});

// Convertir el Map a una cadena
print(miMapa.toString()); // {Manzanas: 12, Plátanos: 14, Uvas: 3}
```

!!! Abstract "Resumiendo"

    Los Map en Dart son una estructura de datos muy útil para almacenar y manipular pares de valores clave-valor. Los elementos de un Map se pueden acceder y modificar mediante la clave correspondiente, y Dart proporciona una gran cantidad de métodos útiles para trabajar con Mapas.
