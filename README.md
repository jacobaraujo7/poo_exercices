
# POO Dart Exercices 

List exercices.

## Exercice 0

O exemplo abaixo cria uma lista de compras, porém só é possível adicionar o nome do produto:

```dart
import 'dart:io';

void main(List<String> args) {
  var products = <String>[];

  bool isRunning = true;

  while (isRunning) {
    print('\nDigite um produto(Ou print para sair):');
    //espera uma interação do usuário
    var typed = stdin.readLineSync() ?? '';
    if (typed == 'print') {
      printProducts(products);
      isRunning = false;
    } else {
      products.add(typed);
    }
  }
}

void printProducts(List<String> products) {
  //adiciona mais uma linha em branco
  print('\n');
  for (var i = 0; i < products.length; i++) {
    var product = products[i];
    print('${i + 1} - $product');
  }
}
```

Estruture o produto para que ele aceite tanto o nome quanto o valor.



## Exercice 1

Considere o exemplo a baixo:

```dart
void main(List<String> args) {
  final person = Person();
  print(person.getName()); // NoName
}

class Person {
  String getName() {
    return 'NoName';
  }
}
```

faça o método `getName()` retornar o seu nome sem alterar nada da classe `Person`.


## Exercice 2

Observer o contrato `Person`:

```dart
abstract class Person {
  double weight;
  double height;
  Person({
    required this.weight,
    required this.height,
  });

  // BMI == IMC
  double calculateBMI();
}
```

Implemente esse contrato calculando o IMC (BMI em inglês).






