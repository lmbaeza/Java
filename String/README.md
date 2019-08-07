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

### compareToIgnoreCase()