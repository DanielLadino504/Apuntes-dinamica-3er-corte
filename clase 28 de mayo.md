# Algebra de bloques
Diagrama de bloques
- Una herramienta que puede ayudar a entender un poc la interaccion entre varios sistemas son los diagramas de bloques.
- Primer sistema de control J.Watt.
- Para explicar su sistemas empezo a desarrollar los diagramas de bloques.
## Maquina de vapor

![](31.jpeg)

# Elementos de un diagrama de bloques 
- Bloque funcional: Es un simbolo para representar la operacion matematica que sobre la señal de entrada hace el bloque para producir una salida.

![](32.jpeg)

- Flechas: Representa las señales que se estan moviendo dentro del proceso, la señal solo puede pasar en la direccion de las flechas y son magnitudes fisicas. La punta de la flecha quie señala el bloque indica una entrada, la punta de la flecha que se aleja del bloque indica salida.

![](33.jpeg)

-Punto suma: Realiza operaciones (Suma o resta) entre señales unicamente. el signo mas o el signo menos en cada punta de la flecha, indica si la señal debe sumarse o restarse.

![](34.jpeg)

-Ramificacion: Un punto de ramificacion es aquel que apartir del cual la señal de un bloque va de modo concurrente a otros bloques o puntos de suma.

![](35.jpeg)

## Interpretacion del diagrama
- La salida de un bloque funcional corresponde a la señal de entrada (Dominios) multiplicada por la funcion de transferencia del bloque 

![](36.jpeg)

Y(s) = U(s) * G(s)

Funcion de transfetencia

\frac{Y(s)}{U(s)} = G(s)

## Aplicacion de una diagrama de bloques 
CSTR = Continuos Stirred Tank Reactor = Tanque Reactor de Agitacion Continua, tanque donde se juntan varias sustancias y sale sola una sustancia 

![](37.jpeg)

![](38.jpeg)

## Ejemplo de clase
bloques en cascada
- si se tienen 2 sistemas interconectadas
- 










