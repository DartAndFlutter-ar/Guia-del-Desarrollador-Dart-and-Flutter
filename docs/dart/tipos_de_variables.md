# Tipos de Variables en Dart

En Dart, existen varios tipos de variables que se utilizan para almacenar diferentes tipos de datos. A continuación, se describen los tipos de variables más comunes en Dart y para qué se utilizan:

1. **int**: El tipo int se utiliza para almacenar números enteros. Este tipo de variable se utiliza para representar valores numéricos sin decimales, como 1, 2, 3, etc.

2. **double**: El tipo double se utiliza para almacenar números decimales o de punto flotante. Este tipo de variable se utiliza para representar valores numéricos con decimales, como 3.14, 2.5, etc.

3. **String**: El tipo String se utiliza para almacenar texto. Este tipo de variable se utiliza para representar cadenas de caracteres, como "Hola", "Mundo", etc.

4. **bool**: El tipo bool se utiliza para almacenar valores booleanos, que son valores que solo pueden ser verdaderos o falsos. Este tipo de variable se utiliza para representar valores booleanos como true o false.

5. **List**: El tipo List se utiliza para almacenar una colección de elementos. Este tipo de variable se utiliza para representar una lista de valores, como una lista de números o una lista de cadenas.

6. **Map**: El tipo Map se utiliza para almacenar una colección de pares clave-valor. Este tipo de variable se utiliza para representar una colección de valores que se pueden acceder utilizando una clave única, como un diccionario.

7. **dynamic**: El tipo dynamic se utiliza para declarar una variable que puede contener cualquier tipo de valor. Este tipo de variable se utiliza cuando no se sabe de antemano el tipo de dato que se va a almacenar en la variable.

Los diferentes tipos de variables en Dart se utilizan para almacenar diferentes tipos de datos, como números enteros, números decimales, texto, valores booleanos, colecciones de elementos, etc. La elección del tipo de variable adecuado dependerá del tipo de dato que se va a almacenar en la variable y del uso que se le va a dar a dicha variable en el programa.

```dart

void main() { // (1)
  
  final String pokemon = 'Ditto'; //(2)
  final int hp = 100; // (3)
  final bool isAlive = true;
  final List<String> abilities = ['impostor'];
  final sprites = <String>['ditto/front.png','ditto/back.png'];
  
  // dynamic == null
  dynamic errorMessage = 'Hola'; // (4)
  errorMessage = true;
  errorMessage = [1,2,3,4,5,6];
  errorMessage = { 1,2,3,4,5,6 };
  errorMessage = () => true;
  errorMessage = null;

  
  print("""  
  $pokemon
  $hp
  $isAlive
  $abilities
  $sprites
  $errorMessage
  """); // (5)
}
```

1. La primera línea define la función principal main() que se ejecutará cuando se inicie el programa.

2. Las siguientes líneas del código definen varias variables usando la palabra clave final. La palabra clave final se utiliza para declarar variables que no cambiarán de valor una vez que se les haya asignado un valor.

3. La variable pokemon es de tipo String y contiene el valor 'Ditto'. La variable hp es de tipo int y contiene el valor 100. La variable isAlive es de tipo bool y contiene el valor true. La variable abilities es de tipo List<String> y contiene una lista con un único elemento: 'impostor'. La variable sprites es de tipo List<String> y contiene una lista con dos elementos: 'ditto/front.png' y 'ditto/back.png'.

4. La sección siguiente del código utiliza la variable errorMessage de tipo dynamic para demostrar que su tipo puede cambiar dinamicamente. La variable errorMessage se inicializa con el valor 'Hola' y luego se le asignan varios valores diferentes, incluidos un valor booleano, una lista, un conjunto, una función y el valor null.

5. Finalmente, la última línea del código utiliza la función print() para imprimir todas las variables declaradas anteriormente en la consola en un formato de cadena de varias líneas utilizando una sintaxis especial que permite insertar variables en la cadena utilizando $ y los corchetes {}.

[Abrir en DartPad](https://dartpad.dev/?id=53ea3c03a30143a8d995ee8dc5c98cc8){ .md-button .md-button--primary target=_blank}
