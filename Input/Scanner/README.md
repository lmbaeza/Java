# Scanner

### Contenido

* [Input mediante Scanner](#)
* [Has Next](#)

### Input mediante Scanner

Permite ingresar datos por la consola


```java
// LIBRARY
import java.util.Scanner;

// INPUT
Scanner in = new Scanner(System.in);

// INPUT
String a  = in.next();        // Hello World  -> Hello
String b  = in.nextLine();    // Hello World  -> Hello World
byte c    = in.nextByte();    // 8 Bites
short d   = in.nextShort();   // 16 Bites
int e     = in.nextInt();     // 32 Bites
long f    = in.nextLong();    // 64 Bites
float g   = in.nextFloat();
double h  = in.nextDouble();
boolean i = in.nextBoolean();
BigInteger j = in.nextBigInteger();
BigDecimal k = in.nextBigDecimal();
```

### HasNext

Retorna `true` si hay mas datos y `false` en caso contrario

```java
in.hasNext();         // boolean
in.hasNextLine();     // boolean
in.hasNextByte();     // boolean
in.hasNextShort();    // boolean
in.hasNextInt();      // boolean
in.hasNextLong();     // boolean
in.hasNextFloat();    // boolean
in.hasNextDouble();   // boolean
in.hasNextBoolean();  // boolean
in.hasNextBigInteger(); // boolean
in.hasNextBigDecimal(); // boolean
```

### HasNext con Base

Retorna `true` si hay un numero de una `base` dada y `false` en caso contrario

```java
int base = 10;
in.hasNextByte(base);
in.hasNextShort(base);
in.hasNextInt(base);
in.hasNextLong(base);
in.hasNextBigInteger(base);
```