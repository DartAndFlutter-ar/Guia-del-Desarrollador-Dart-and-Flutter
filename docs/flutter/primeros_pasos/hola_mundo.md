# Hola mundo

Este código de Flutter es una aplicación básica que simplemente muestra una pantalla con un texto "Hola Mundo". A continuación, se explican las partes del código:

```Dart
import 'package:flutter/material.dart'; // (1)

void main() {
  runApp(const MainApp(123)); // (2)
}

class MainApp extends StatelessWidget { // (3)
  const MainApp({super.key}); // (4)

    final int nombre = 2+3;

  @override // (5)
  Widget build(BuildContext context) { // (6)
    return const MaterialApp( // (7)
      home: Scaffold( // (8)
        body: Center( // (9)
          child: Text('Hello World!'), // (10)
        ),
      ),
    );
  }
}
```

1. La primera línea importa el paquete flutter/material.dart, que proporciona una variedad de widgets y herramientas para construir interfaces de usuario de material design en Flutter.

2. La función main llama a la función runApp para iniciar la aplicación Flutter. runApp toma como argumento el widget raíz de la aplicación, en este caso, la clase MainApp.

3. La clase MainApp es una subclase de StatelessWidget. Un widget sin estado es aquel que no tiene mutable state, es decir, que una vez que se construye, no cambia. En este caso, MainApp es el widget raíz de la aplicación.

4. Este constructor define un parámetro opcional key y llama al constructor de la clase base (super) sin pasar ningún argumento. El modificador const indica que tanto este constructor como cualquier instancia de la clase MainApp se construirán de forma inmutable.

5. Este es el anotador override, que indica que el método que sigue a continuación (en este caso, build) reemplaza el método correspondiente de la clase base (StatelessWidget).

6. El método build de MainApp devuelve un widget que define la interfaz de usuario de la aplicación.

7. Este widget MaterialApp es un widget de nivel superior que proporciona varios servicios, como la navegación y el manejo de temas.

8. El widget Scaffold proporciona una estructura básica de pantalla para la aplicación. En este caso, solo se define el cuerpo de la pantalla.

9. El widget Center se utiliza para centrar su widget hijo, que es un widget Text.

10. El widget Text muestra el mensaje "Hola Mundo" en el centro de la pantalla.

[Abrir en DartPad](https://dartpad.dev/?id=e5dc839eda844fd6392c3cca2f864749){ .md-button .md-button--primary target=\_blank}

## Explicación

1. La primera línea importa el paquete flutter/material.dart, que proporciona una variedad de widgets y herramientas para construir interfaces de usuario de material design en Flutter.

2. La función main llama a la función runApp para iniciar la aplicación Flutter. runApp toma como argumento el widget raíz de la aplicación, en este caso, la clase MainApp.

3. La clase MainApp es una subclase de StatelessWidget. Un widget sin estado es aquel que no tiene mutable state, es decir, que una vez que se construye, no cambia. En este caso, MainApp es el widget raíz de la aplicación.

4. Este constructor define un parámetro opcional key y llama al constructor de la clase base (super) sin pasar ningún argumento. El modificador const indica que tanto este constructor como cualquier instancia de la clase MainApp se construirán de forma inmutable.

5. Este es el anotador override, que indica que el método que sigue a continuación (en este caso, build) reemplaza el método correspondiente de la clase base (StatelessWidget).

6. El método build de MainApp devuelve un widget que define la interfaz de usuario de la aplicación.

7. Este widget MaterialApp es un widget de nivel superior que proporciona varios servicios, como la navegación y el manejo de temas.

8. El widget Scaffold proporciona una estructura básica de pantalla para la aplicación. En este caso, solo se define el cuerpo de la pantalla.

9. El widget Center se utiliza para centrar su widget hijo, que es un widget Text.

10. El widget Text muestra el mensaje "Hola Mundo" en el centro de la pantalla.

## Debug Banner 

Para Remover el cartel de **Debug** agregar `debugShowCheckedModeBanner: false` dentro del Widget de `MaterialApp()`

```dart
MaterialApp( 
    debugShowCheckedModeBanner: false,
    ...
);

```

!!! Abstract "Resumiendo"

    En resumen, este código define una aplicación de Flutter simple que muestra un mensaje de "Hola Mundo" en el centro de la pantalla utilizando widgets predefinidos de Flutter.

