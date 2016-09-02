## Formatos de instrucción 

Para que los programas escritos en el lenguaje de Q1 sean ejecutables por una computadora, deben estar escritos en **código máquina**. Entonces es necesario establecer las reglas de traducción código fuente/código máquina que debe aplicar un **ensamblador**. 

> Un ensamblador es un programa que traduce código fuente a código máquina siguiendo una determinada especificación de arquitectura

Las reglas que utiliza el ensamblador se conocen como **Formatos de instrucción**. Estos definen la organización de los bits dentro de una instrucción, en términos de las partes que la componen, pues la instrucción debe incluir información acerca de: ¿Que operación hay que hacer?¿Sobre qué datos? 

Entonces, mínimamente debe incluir el código de la operación y un mecanismo para llegar hasta el/los operando/s.
Los mecanismos que mencionamos hasta ahora son el **inmediato** (constante) y el **registro** (variable). Por ejemplo (ver operando Origen):

* ```ADD R0, R1```
* ```ADD R0, 0x0001```

Las instrucciones anteriores deben distinguirse a nivel de código máquina. Entonces la estructura podría ser:

> (Operacion)(Operando destino)(Operando origen)

Que en el ejemplo ADD RO, 0x0001 es:

> (Operacion:ADD)(Operando en modo registro)(Operando constante)


¿Faltan información? ¡SI! ¿Que registro es? ¿Que constante es?

> (Operacion:ADD)(Operando en modo registro)(Operando constante)(R0)(0x0001)

Aún falta escribir lo anterior en binario, para que pueda almacenarse en memoria y traducirse en acciones mediante circuitos.

## Especificaciones de Q1

### Formato de instrucciones de dos operandos

| codop | Modo Destino | Modo Origen | Operando Destino | Operando Origen |
|:-----:|:------------:|:-----------:|:----------------:|:---------------:|
|   4b  | 6 bits | 6 bits | 16 bits | 16 bits |

### Codigos de operaciones

| codop | operacion |
|:-----:|:---------:|
| 0000  | MUL |
| 0001  | MOV |
| 0010  | ADD |
| 0011  | SUB |
| 0111  | DIV |


### Modos de direccionamiento

| Modo | Codificacion |
|:----------:|:---------:|
| Inmediato  | 000000 |
| Registro   | 100rrr |



### Poniendo en práctica

Ensamblar (dar el codigo máquina de) la instruccion: ```ADD R0,R1```