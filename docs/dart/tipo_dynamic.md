# Variable Tipo Dynamic

En Dart, `dynamic` es un tipo de variable especial que permite la asignación de cualquier tipo de valor en tiempo de **ejecución**.

Las variables declaradas como `dynamic` no se comprueban en tiempo de **compilación** para verificar que sean del tipo correcto. En lugar de eso, se permiten todas las operaciones en las variables `dynamic` y se comprueba su tipo en tiempo de **ejecución**.

Algunos de los casos de uso comunes de `dynamic` son:

- Cuando se trabaja con una API externa que puede devolver diferentes tipos de datos según el contexto.
- Cuando se trabaja con datos que pueden cambiar su tipo de manera dinámica, como en el ejemplo del código anterior.
- Cuando se necesita almacenar objetos de diferentes tipos en una lista o mapa.

Sin embargo, el uso excesivo de `dynamic` puede dificultar la comprensión del código y aumentar la posibilidad de errores en tiempo de **ejecución**. Además, las variables `dynamic` no tienen los beneficios de comprobación de tipo que proporcionan los otros tipos de variables en Dart, lo que puede hacer que el código sea más difícil de mantener y depurar.

!!! tip

    En general, se recomienda evitar el uso excesivo de `dynamic` y utilizar los tipos de datos estáticos siempre que sea posible para beneficiarse de la comprobación de tipos en tiempo de **compilación**.

Un ejemplo común de error que puede ocurrir debido al uso indebido de `dynamic` es la invocación de un método que no existe en tiempo de **ejecución**.

Por ejemplo, considera el siguiente código:

```dart
void main() {
  dynamic value = 'Hola mundo';
  value.toUpperCase(); // (1)
}
```


1. `toUpperCase` es un método que devuelve un `string` en mayúsculas.

En este ejemplo, la variable value se declara como `dynamic` y se le asigna una cadena de caracteres "Hola mundo". Luego, se llama al método `toUpperCase()` en la variable `value`.

El problema aquí es que, como la variable value se declara como `dynamic`, Dart no verifica en tiempo de compilación si el método `toUpperCase()` existe en el objeto al que se hace referencia. En este caso, como el objeto es una cadena de caracteres, el método `toUpperCase()` sí existe y el programa se ejecutará sin problemas.

Sin embargo, si cambiamos el valor de la variable value a un tipo de objeto diferente que no tenga un método `toUpperCase()`, el programa fallará en tiempo de **ejecución**. Por ejemplo:

```dart
void main() {
  dynamic value = 123;
  value.toUpperCase();
}
// Como notaras Dart no nos brinda ningún error. 
// Sin embargo si corremos el código el programa crasheara. 
// Y si cambiamos el tipo de dato de la variable `value`
// Por un entero Dart nos advertirá del error. 
```

[Abrir en DartPad](https://dartpad.dev/?id=0d7100d7ead4007f6fb888f4b36950a3){ .md-button .md-button--primary target=_blank}

En este caso, la variable `value` se le asigna un valor entero en lugar de una cadena de caracteres. Como los enteros no tienen un método `toUpperCase()`, el programa arrojará un error en tiempo de **ejecución** que indicará que el método no existe.

El uso indebido de dynamic puede hacer que el código sea más difícil de entender y mantener, y puede provocar errores en tiempo de **ejecución**. Por lo tanto, se recomienda utilizar `dynamic` solo cuando sea necesario y siempre que sea posible utilizar tipos estáticos para beneficiarse de la comprobación de tipos en tiempo de **compilación**.

!!! Abstract "Resumiendo"

    El uso indebido de dynamic puede hacer que el código sea más difícil de entender y mantener, y puede provocar errores en tiempo de ejecución. Por lo tanto, se recomienda utilizar dynamic solo cuando sea necesario y siempre que sea posible utilizar tipos estáticos para beneficiarse de la comprobación de tipos en tiempo de compilación.
