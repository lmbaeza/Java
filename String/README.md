# String

### Contenido

* [Setup](#)
* [charAt(int index) char](#)
* [codePointAt(int index) int](#)
* [codePoints() IntStream](#)
* [chars() IntStream](#)
* [compareTo(String anotherString) int](#)
* [](#)
* [](#)
* [](#)

### Setup
```java
String msg = "Hello World";
```

### charAt(int index) char

Retorna el caracter en la posición _index_ de la cadena _msg_

```java
msg.charAt(0); //H
```
### codePointAt(int index) int

Retorna el numero del codigo ascii correspondiente al caracter en la posición _index_ de la cadena de string _msg_

```java
msg.codePointAt(0); //72 (Codigo Ascii del caracter 'H')
```
### codePoints() IntStream

Este metodo retorna un Objeto _IntStream_ que contiene una lista con el codigo ascii de cada uno de los caracteres de la cadena. 

```java
IntStream streamCP = msg.codePoints();

streamCP.forEach(out::println);
//Out:
// 72
// ... ...
//100

// Array con los digitos de codigo ascii del string
int[] arrCP = streamCP.toArray();

Arrays.toString(arrCP);
// [72, 101, 108, 108, 111, 32, 87, 111, 114, 108, 100]
```

### chars() IntStream

Este metodo retorna un Objeto _IntStream_ que contiene una lista con el codigo ascii de cada uno de los caracteres de la cadena. 

```java
IntStream chars = msg.chars();
Arrays.toString(chars.toArray());
// [72, 101, 108, 108, 111, 32, 87, 111, 114, 108, 100]
```

### compareTo(String anotherString) int

Compara 2 cadena y retorna:

* `0` : si las cadena son iguales
* `±length` : Si las cadenas son diferentes

**Nota:** Discrimina minusculas y mayusculas
```java
msg.compareTo("Hola Mundo");  // -10
msg.compareTo("Hello World"); // 0
```

### compareToIgnoreCase(String anotherString) int

Compara 2 cadena y retorna:

* `0` : si las cadena son iguales
* `±length` : Si las cadenas son diferentes

**Nota:** No discrimina minusculas y mayusculas

```java
msg.compareToIgnoreCase("hello world"); // true
```

### concat(String str) String

Concatena al final del string `msg` la cadena `str`.

```java
msg.concat(" English"); // Hello World English
```

### contains(String str) boolean

Saber si una subcadena esta dentro de una cadena
_retorna:_ true o false segun sea la respuesta

```java
msg.contains("He"); //true
```

### endsWith(String str) boolean

Verifica si la subcadena en la que termina en una subcadena en particular.

```java
msg.endsWith("World"); // true
```

### equals(String str) boolean

Verificar si 2 cadenas son iguales:
Retorna: true, false

```java
msg.equals("Hello World"); // true
```

### equalsIgnoreCase(String str) String

Verifica si 2 cadenas son iguales sin tener en cuenta minuscula de mayuscula

```java
msg.equalsIgnoreCase("hello world"); // true
```

### getBytes() byte []

Imprime los digitos del codigo ascii de la cadena

```java
Arrays.toString(msg.getBytes())
// [72, 101, 108, 108, 111, 32, 87, 111, 114, 108, 100]
```

### hashCode() int
Retorna el codigo hash de la cadena, es unico por cada cadena diferente

```java
msg.hashCode(); // //-862545276
```

### indexOf(String str) int

Retorna el indice donde comienza la subcadena en caso de que no exista la subacadena retorna -1

```java
msg.indexOf("World"); // 6
```

### indexOf(char character) int

Retorna el indice donde comienza la subcadena en caso de que no exista la subacadena retorna -1

```java
msg.indexOf('W'); // 6
```

### isBlank() boolean

Saber si un string esta en blanco

```java
StringUtils.isBlank(null); // true
"".isBlank();              // true  
" ".isBlank();             // true  
"bob".isBlank();           // false  
"  bob  ".isBlank();       // false
```

### isEmpty() boolean

Saber si un string esta vacio

```java
StringUtils.isEmpty(null); // true
"".isEmpty();              // true  
" ".isEmpty();             // false  
"bob".isEmpty();           // false  
"  bob  ".isEmpty();       // false
```

### lastIndexOf(String str) int

Retorna el ultimo indice de la subcadena ingresada

```java
String msg1 = "Hello World Hello World";
msg1.lastIndexOf("World"); // 18
```

### lastIndexOf(char character) int

Retorna el ultimo indice del caracter ingresada

```java
String msg1 = "Hello World Hello World";
msg1.lastIndexOf('W'); // 18
```

       
### lines() Stream<String>

retorna un array partido en los saltos de linea

```java
String msg2 = "Hello \nWorld \nHello \nWorld";
Stream<String> streamLines = msg2.lines();

Object[] streamLinesArr =  streamLines.toArray();

for(Object x: streamLinesArr) {
    out.print(x.toString() +" <-> ");
}
out.println();
// Hello  <-> World  <-> Hello  <-> World <->
```

### matches(String regex) boolean

Saber si una subcadena esta en una cadena

```java
msg.matches(".*\\bHello\\b.*"); // true
```

### replace(String oldStr, String newStr) String

Reemplazar la subcadena 'Hello' por 'Hola'

```java
msg.replace("Hello", "Hola"); // Hola World
```

### replace(char oldChar, char newChar) String

Reemplazar el caracter 'H' por 'h'

```java
msg.replace('H', 'h'); // hello World
```
        
        