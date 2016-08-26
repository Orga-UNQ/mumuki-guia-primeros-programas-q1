## Variables
La arquitectura Q1 tiene 8 registros de 16 bits. Esas son las variables con las que el programador puede contar.

## Repertorio de instrucciones
Además, tiene el siguiente repertorio de instrucciones, es decir que los programas son una secuencia de ellas.

Las instrucciones aritméticas son ADD, SUB, MUL y DIV. Cada una tiene dos operandos, y almacena el resultado en el primero de ellos, que es denominado ***operando destino*** mientras que el otro se denomina ***operando origen***. 

Por ejemplo, un ADD se escribe ```ADD R0, R1 ``` y luego de sumar los contenidos de los registros R0 y R1, almacena el resultado en R0.

Análogamente, si nuestro programa es ```SUB R0, R1``` y los valores de los registros R0 y R1 son 5 y 4 respectivamente, ¿Que variable se modifica y cual es su nuevo valor? 

Exacto! El **efecto de la ejecución** de esa instrucción es ```R0=0x0004```

## Ahora trabajás vos

Si antes de ejecutar la instrucción ```ADD R5, R6 ``` el R5 tenía almacendo ```0x0004```  y R6 tenía ```0x00AA```

> ¿Cual es el efecto de la ejecución de esa instrucción? (Ayuda: debés escribir algo como R?=0x????)
