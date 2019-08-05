# String

### Contenido

* [Setup](#)

* [charAt(int index) char](#)
* [](#)
* [](#)
* [](#)
* [](#)
* [](#)
* [](#)
* [](#)

### Setup
```java
import java.io.PrintStream;

PrintStream out = System.out;
String msg = "Hello World";
```

### charAt(int index) char

Imprime el caracter en el indice 0 de la cadena _msg_

```java
out.println(msg.charAt(0)); //H
```
### codePointAt(int index) int

```java
out.println(msg.codePointAt(0)); //72 (Codigo Ascii del caracter 'H')
```