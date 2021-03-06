# Building Calc Engine with Java

## Java Notes

Reverse domian name notation in Java packages.
Type name are qualified by their Package name
Package name affect source code organisation

IDE - Integrated Development Enviroment
JRE - Java Runtime enviroment
JDK - Java Development Kit

Primitive Data types
Integer types
Byte 8 bits -128 - 128
Short 16 bits -32768 - 32768
int 32 bits -2147483648 - 2147483647
long 64bits -9223372036854775808 - 9223372036854775807 0L

Floating points type
float
double

Character Data Type
Boolean type

Operators
Basic + - _ / %
++ Prefix and Postfix ++
comound operator += -+ /= _/ %/

Operator precedence
Postfix -> Prefix -> multiplicative -> additive

Type conversion and Casting
Narrowing and widening

###### String Formating

%[argument index][flags][width][precision] conversion
Conversion types
d - integer
xX - Hex
f - Decimal
eE - Scientific Notation
s String

Flags
\# - radix
0 Zero padding
\- - left justified
, - include grouping seperators
space - Leading space with positive number
\+ - Always show sign

Argument Index
index\$ - index of arguments to use (1 based not like the array)
< - corresponds to the same arguments as the previous specifier

###### Time

- Time Stamping Events
- Local date, time amd sate time
- Global - ZonedDateTime

DateTimeFormatter

##### Access Modifiers

Encapsulations and access modifiers
| Modifiers | Visibility | usable on class | usable on members |
| :--------------: | :-------------------: | :-------------: | :---------------: |
| None | only withiin its own package (aka package private) | Y | Y |
| public | Everywhere | Y | Y |
| Private| only withn the declaring class | N\* | Y|

Field Encapsulation using accessor(getter) and mutator(setters) patterns

Establishing Initial state

- Fleid initializers: Give field a value
- Initialization Blocks
- Constructors
  The above also follows initialization and construction order.

Constructors, constructors chaining, constructor visibility and initialization block.

Static members

- Including keyword static
- Static fields and importing static methods ( Actions tied to the class itself ) without having to qualify by the class name
- Static initialization block

```
private static int <VariableName>;
Static {
 // Add your static methods here
}
```

Making changes to object (in this case an instace of a class) passed to methods requires using the getter and setter methods

Method Overloading

- Multiple number of parameters can be passed in by uinf the ... which is similar to the spread operator in JS. methodName(dataType... variableName) varialbleName is passed in as an array

There is a difference between refrence types and instance type.
`instanceOf` operator to check that if its an instance of the object in question.

super refrence allows us call the base class.

Enums

```
public enum FlightCrewJOB(){
    FLIGHT_ATTENDANT("Flight Attendant),
    COPILOT("First Officer"),
    PILOT("Captain);

    private String title;
    private String getTitle(){return title;}
    private FlightCrewJob(String title) {
        this.title = title;
    }
}
```

Interfaces: It allows is to define a contract for behavoir


//TODO Review inner class


Data Strtuctures are diverse
- Ordering
- Pairs
- Uniqueness

String::compareTo - Method refrence syntax
item -> System.out.println(item * item) - lambda expressions