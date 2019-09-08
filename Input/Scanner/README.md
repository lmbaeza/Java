# Scanner

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
```