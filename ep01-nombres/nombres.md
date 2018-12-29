Un nombre en Go tiene que comenzar con letra [a-z_A-Z] y luego puede tener
cualquier combinación de letras y números. El guión bajo se considera una letra.

# Ejemplos de nombres válidos

```
x
x_1
_a
a1
procesarHTML
new
_
```


# Ejemplos de nombres inválidos

```
0a									// No comienza con letra.
$total							// No comienza con letra.
precio*cantidad			// No consiste solo de letras y números.
precio por unidad		// No consiste solo de letras y números.
func								// Palabra reservada.
```


# Ejemplos de nombres válidos pero NO idiomáticos en Go

```
indice_del_ciclo	// en Go, se prefiere: i
fabricadeobjetos	// en Go, se prefiere: fabricaDeObjetos
UNA_CONSTANTE			// en Go, se prefiere: UnaConstante
```


# Estos nombres NO son iguales (mayúsculas y minúsculas importa)

```
procesarHTML
procesarHtml
ProcesarHtml
```


# Go Keywords (palabras claves, reservadas)

```
break        default      func         interface    select
case         defer        go           map          struct
chan         else         goto         package      switch
const        fallthrough  if           range        type
continue     for          import       return       var
```


# Go Pre-defined names (nombres pre-declarados, no reservados)

```
Types:
	bool byte complex64 complex128 error float32 float64
	int int8 int16 int32 int64 rune string
	uint uint8 uint16 uint32 uint64 uintptr

Constants:
	true false iota

Zero value:
	nil

Functions:
	append cap close complex copy delete imag len
	make new panic print println real recover

```

