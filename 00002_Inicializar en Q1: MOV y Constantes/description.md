Muchos programas necesitan dar un determinado valor a una determinada variable. Esto se denomina muchas veces **inicializar la variable**.

Supongamos que la variable que usaremos es R5 y necesitamos que sea un contador. Entonces necesitamos **inicializarla en 0**.

¿Como se escribe eso en Q1?


### Instrucción MOV
No lo dijimos antes, pero Q1 cuenta también con una instrucción para **copiar** el valor de un operando en otro operando. Esta instrucción se denomina **MOV** y similarmente a las instrucciones ADD y SUB, tiene dos operandos (destino y origen). Por ejemplo ```MOV R5, R6```copia el contenido de R6 en R5. El único operando que se modifica es R5.

Pero todavía no podemos inicializar R5, porque nos hace falta poder expresar un valor determinado.

### Constantes

La escritura de constantes en Q1 se hace usando el **sistema hexadecimal** y anteponiendo el texto```0x```. En la instrucción MOV como la que vimos arriba, podríamos reemplazar el operando origen con una constante, escribiendo: 
```
MOV R5, 0x0000
```

> Escribí un programa que inicialice R0 con una cadena hexadecimal que represente el valor 3 en BSS(16)