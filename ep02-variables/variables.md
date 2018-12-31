# Variables en Go

Una varibale es un espacio en la memoria que tiene un tipo de dato específico y <br>
que almacena un valor de ese tipo. Por ejemplo, una variable de tipo int puede <br>
almacenar un valor de tip int (0, 1, 2, 3). En la mayoría de los casos, las variables<br>
tienen nombres que le asignamos al declararlas.

## Ejemplos de declaraciones de variables

Al usar la palabra clave var, se puede declarar una variable en cualquier lugar <br>
del programa.

```
var x int = 1		// Declaración con nombre, tipo de dato y valor.
var x = 1		// Declaración sin tipo de dato.
var x			// Declaración sin tipo de dato ni valor asignado. 
var x, y int = 1, 2	// Se pueden declarar múltiples variables a la vez.
var x, y = 1, 3.14	// Se omite el tipo de dato si son tipos distintos por variable.
```

Las siguientes declaraciones no usan var, sino que usan el operador de declaración <br>
corta := y solo pueden ocurrir dentro de una función.

```
x := 1			// Nunca se incluye el tipo de dato.
x, y := 1, 3.14		// Aquí, solo y es declarada ya que x ya existe en este bloque.
```

## Tipos de datos en Go

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

## Alcance (Scope) de variables en Go

En Go, cada archivo de código pertenece a un paquete (package). Un paquete es una <br>
unidad de codigo que sirve una función específica, como por ejemplo servir como punto <br>
de entrada a un programa por ejecutar (package main) o como una librería de varables y <br>
funciones para uso en otros programas (fmt, os, net/http).

Cualquier variable declarada fuera de una función es global y visible en todo el paquete <br>
que la contiene. Una variable declarada dentro de una función es local y visible solo <br>
dentro de esa función. Una variable local con el mismo nombre que una global, solapa <br>
y oculta a la variable global (shadowing), lo cual puede resultar en código confuso y <br>
errores difíciles de encontrar.

```
package main

import (
	"fmt"
)

var global = "soy global"

func saluda() {
	global := "soy local" // global se declara nuevamente como local!
	fmt.Println(global)
}

func main() {
	saluda()
	fmt.Println(global)
}
```
