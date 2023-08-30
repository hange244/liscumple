void main() {
  final String pokemon = 'Ditto';
  final int hp = 100;
  final bool isAlice = true;
  final List<String> abilities = ['impostor'];
  final sprites = <String>['ditto/front.png', 'ditto/back.png'];

  dynamic errorMessage = 'Hola';
  errorMessage = true;
  errorMessage = [1, 2, 3, 4, 5, 6];
  errorMessage = {1, 2, 3, 4, 5, 6};
  errorMessage = () => true;
  errorMessage = null;

  print("""
$pokemon
$hp
$isAlice
$abilities
$sprites
$errorMessage

""");
}

void main() {
  print(greetEveryone());
  print("suma: ${addTwoNumbers(10, 20)}");
}

String greetEveryone() => "Hello everyone";

int addTwoNumbersOptional(int a, int b) => a + b;

int addTwoNumbers(int a, [int b = 0]) {
  return a + b;
}

String greetPerson({name, message}) {
  return "hola ,Fernando";
}

void main() {
  final Map<String, dynamic> pokemon = {
    'name': 'Ditto',
    'hp': 100,
    'isAlive': true,
    'abilites': <String>['impostor'],
    'sprites': <int, String>{1: 'ditto/front.png', 2: 'ditto/back.png'}
  };

  print(pokemon);
  print('Name: ${pokemon['name']} ');
  print('Name: ${pokemon['sprites']} ');

  print('Back: ${pokemon['sprites'][2]} ');
  print('Front: ${pokemon['sprites'][1]} ');
}

void main() {
  final numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 13, 14];

  print('List original $numbers');
  print('Length ${numbers.length}');
  print('Index 0: ${numbers[3]}');
  print('First: ${numbers.first}');
  print('Last: ${numbers.last}');
  print('Reversed: ${numbers.reversed}');

  final reversedNumbers = numbers.reversed;
  print('Iterable: $reversedNumbers');
  print('List: ${reversedNumbers.toList()}');
  print('Set: ${reversedNumbers.toSet()}');

  final reversedNumber = numbers.where((num) {
    return num > 5;
  });

  print('>5 iterable: $numbersGreaterThan5');
  print('>5 Set: ${}')
}

void main() {

print(greetEveryone() );

print( 'suma: ${ addTwoNumbers( 10, 20)}');

print( greetPerson( name: 'Fernando' , message: 'Hi,' ));

}

String greetEveryone() => 'Hola mundo';

int addTwoNumbers( int a, int b ) => a + b;

int addTwoNumbersOptional( int a, [int b = 0 ]) {

//b ??= 0;

return a + b;
}


String greetPerson({ required String name, String message = 'Hola,'}) {

  return '$message Fernando';

}


void main() {
  for (int i = 0; i < 5; i++) {
    print('hello ${i + 1}');
  }
}

void main() {
  
  final Hero wolverine = Hero('Logan','Regeneracion');
  
  print( wolverine );
  print( wolverine.name );
  print( wolverine.power );
  
  
}

class Hero{
  
  String name;
  String power;
  
  Hero( String pName, String pPower )
    : name = pName,
     power = pPower;
  
}
void main() {
  
  final Hero wolverine = Hero('Logan','Regeneracion');
  
  print( wolverine );
  print( wolverine.name );
  print( wolverine.power );
  
  
}

class Hero{
  
  String name;
  String power;
  
  Hero( this.name , this.power );
  
}


void main() {
  
  final Hero wolverine = Hero(name: 'Logan',power: 'Regeneracion');
  
  print( wolverine );
  print( wolverine.name );
  print( wolverine.power );
  
  
}

class Hero{
  
  String name;
  String power;
  
  Hero({ 
       required this.name ,
       required this.power
    } );
  
}

void main() {
  
  final Hero wolverine = Hero(name: 'Logan',power: 'Regeneracion');
  
  print( wolverine.toString() );
  print( wolverine.name );
  print( wolverine.power );
  
  
}

class Hero{
  
  String name;
  String power;
  
  Hero({ 
       required this.name ,
        this.power = 'sin poder'
    } );
  
  
  @override  
  String toString() {
    return '$name - $power';
  }
  
}

