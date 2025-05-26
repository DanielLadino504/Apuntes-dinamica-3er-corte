# Modelamiento  de sistemas con diagrama de bloques 
## Modelos de sistemas complejos 
- Se podrian modelar sistemas como un todo hallando las funciones de transferencia de cada componente.
- Otro enfoque es utiliza modelos ya desarrollados ampliamente para construir modelos mas complejos.

# Solenoide
## Modelo del circuito electromagnetico
- Es un circuito electrico formado por un circuito electrico, un acoplamiento electromecanico y un sistema mecanico de traslacion.

![](90.jpg)

$$ L\frac{di}{dt} + Ri = v(t) $$

Trasformada de LaPlace

$$ LsI(s) + RI(s) = V(s) $$ 

$$ I(s)(L_{s}+R) = V(s) $$

$$ I(S) = V(s)\frac{1}{Ls+R} $$

Circuito 

$$ V_{L} + V_{R} = V(t) $$

Funcion de trasferencia 

$$ \frac{I(s)}{V(s)} = \frac{1}{Ls+R} $$
 
## Acople entre la parte electromagnetica y la parte mecanica 
- El electroiman produce una fuerza mecanica proporcionada a la corriente en el embobinado.

![](90.jpg)

$$ f_{s} = K_{s}i $$

Trasformada de LaPlace

$$ f_{s}(s) = K_{s}I(s) $$

Funcion de trasferencia

$$ \frac{F_{s}(s)}{I(s)} = K_{s} $$

## Sistema mecanica 

![](90.jpg)

- El electroiman atrae una masa acoplada por medio de un resorte y se considera el amortiguamiento dado por la envolvente de la bobina 

![](88.jpg)

$$ m\frac{d^{2}x}{dt^{2}} + b\frac{dx}{dt} + \kappa x = f(t) $$

Trasformada de LaPlace

$$ X(s) = F(s)\frac{1}{ms^{2}+bs+\kappa} $$

Intermedio 

$$ f(t) - KX - b\dot{x} = m\ddot{x} $$

$$ F(s) - KX(s) - bsX(s) = ms^{2}X(s) $$

$$ F(s) = X(s)ms^{2} + bsX(s) + KXs) $$

$$ F(s) = X(s)(ms^{2} + bs + K) $$

# Representacion en bloque

![](81.jpg)

![](82.jpg)

# Motor DC

![](83.jpg)

## Motor DC (Corriente de campo)
circuito elemtromagnetico

![](84.jpg)

corriente de armadula es costante 

$$ i_{a} = cte$$

$$ V_{c}(t) = V_{Rc} + V_{Lc} $$

$$ V_{c}(t) = {Rc}{Lc} + L\frac{dic}{dt} $$

$$ L_{c}\frac{di_{c}}{dt} + R_{c}i_{c} = v_{c(t)} $$

Trasformada de LaPlace

$$ L_{c}(s) = V_{c}(s)\frac{1}{(sL_{C}+R_{c})} $$

Funcion de trasferencia 

$$ \frac{I_{c}(s)}{V_{c}(s)} = \frac{l}{sL_{c} + R_{c}} $$

Parte intermedia 
Como se comviente la corriente en torque que es la que provoca el movimiento del eje

- El flujo $\phi$ en el entrehierro es proporcional a la corriente de campo

$$ \phi = K_{c}i_{c} $$

- El torque desarrollado es proporcional al $$ \phi $$ y a la corriente de armadura

$$ T_{m}=K_{a}i_{a}\Phi \Rightarrow T_{m} = K_{a}i_{a}(t)K_{c}i^{c}(t) \Rightarrow T_{m}=(K_{a}K_{c}i_{a})i_{c}(t) $$

$$ T_{m}(s) = (K_{a}K_{c}I_{a})I_{c}(s) = K_{m}I_{c}(s) \Rightarrow \frac{I_{m}(s)}{I_{c}(s)}=K_{m} $$

- El torque aplicado a la carga es el desarrollado por el motor menos la inercia de la carga

$$ T_{c}(s) = T_{m}(s)-T_{p}(s) $$

- El torque aplicado (parte mecanica) a la carga se comporta como un sistema totacional clasico que considera la inercia y la friccion mecanica
Ecuancion general

$$ J\frac{d^{2}\theta }{dt^{2}}+b\frac{d\theta }{dt}+\kappa \theta =\tau (t) $$

$$ \Theta (s) = T_{c}(s)\frac{1}{(s^{2}J+bs)} $$

Funcion de trasferencia 

$$ \frac{\theta (s)}{I_{c}(s)} = \frac{1}{s^{2}J+bs} $$ 

Se puede representar de la siguiente forma 

Escrita matematicamente funcion de trasferencia para el motor DC

$$ \Theta (s)= V_{c}(s)\frac{K_{m}}{(sL_{c}+R_{c})(Js^{2}+bs)}-T_{p}(s)\frac{1}{(Js^{2}+bs)} $$

$$ \frac{\Theta (s)}{V_{c}(s)} = \frac{K_{m}}{(sL_{c}+R_{c})(Js^{2}+bs)} $$

# Modelo del motor DC (Corriente de armadura)














