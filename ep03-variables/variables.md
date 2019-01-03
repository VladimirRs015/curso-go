# Variables en Go

Una varibale es un espacio en la memoria que tiene un tipo de dato específico y <br>
que almacena un valor de ese tipo. Por ejemplo, una variable de tipo int puede <br>
almacenar un valor de tip int (0, 1, 2, 3). En la mayoría de los casos, las variables<br>
tienen nombres que le asignamos al declararlas.

## Ejemplos de declaraciones de variables

Al usar la palabra clave var, se puede declarar una variable en cualquier lugar <br>
del programa.

```
var x int = 1		    // Declaración con nombre, tipo de dato y valor.
var x = 1		        // Declaración sin tipo de dato.
var x int			      // Declaración sin valor asignado.
var x, y int = 1, 2	// Se pueden declarar múltiples variables a la vez.
var x, y = 1, 3.14	// Se omite el tipo de dato si son tipos distintos por variable.
```

Las siguientes declaraciones no usan var, sino que usan el operador de declaración <br>
corta, (:=), y solo pueden ocurrir dentro de una función.

```
x := 1			// Nunca se incluye el tipo de dato.
x, y := 1, 3.14		// Aquí, solo y es declarada ya que x ya existe en este bloque.
```

Este tipo de declaración corta no permite especificar el tipo de dato, por lo que en casos<br>
donde el tipo de dato es ambiguo, hay que usar var:

```
i := 100		// Un int (entero)
var i float64 = 100	// Un float64 (punto flotante 100.0)

## Valor zero (Zero Value) en Go

Si una variable es declarada pero no se le asigna un valor, recibe lo que se conoce en Go como el<br>
valor zero (zero value) automáticamente. Los valores zero para cada tipo de dato son:

- Número: 0
- String: ""
- Booleano: false
- Slice, function, channel, map, pointer: nil

## Tipos de datos básicos en Go

Estos son los tipos de datos básicos de Go. Existen otros tipos de datos más complejos<br>
como array, map, slice, struct, function, pointer, y channel. Esos los veremos luego en el curso.

```
bool
int int8 int16 int32 int64 
uint uint8 uint16 uint32 uint64 uintptr
float32 float64
complex64 complex128 
byte (uint8)
rune (int32)
error
string
```

