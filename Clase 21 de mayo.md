# MODELAMIENTO DE SISTEMAS CON DIAGRAMA DE BLOQUES 
Valentina Riveros Feria, Angel David Melo, Daniel Felipe Ladino 
## MODELOS DE SISTEMAS COMPLEJOS
- Se podrian modelar sistemas como un todo hallando las funciones de transferencia de cada componente.
- Otro enfoque es utiliza modelos ya desarrollados ampliamente para construir modelos mas complejos.
# SOLENOIDE
## MODELO DEL CIRCUITO ELECTROMAGNETICO
- Es un circuito electrico formado por un circuito electrico, un acoplamiento electromecanico y un sistema mecanico de traslacion.

![](90.jpg)

$$ L\frac{di}{dt} + Ri = v(t) $$

Trasformada de LaPlace

$$ LsI(s) + RI(s) = V(s) $$ 

$$ I(s)(L_{s} + R) = V(s) $$

$$ I(S) = V(s)\frac{1}{Ls + R} $$

Circuito 

$$ V_{L} + V_{R} = V(t) $$

Funcion de trasferencia 

$$ \frac{I(s)}{V(s)} = \frac{1}{Ls + R} $$
 
# ACOPLE ENTRE LA PARTE ELECTROMAGNETICA Y LA PARTE MECANICA
- El electroiman produce una fuerza mecanica proporcionada a la corriente en el embobinado.

![](90.jpg)

$$ f_{s} = K_{s}i $$

Trasformada de LaPlace

$$ f_{s}(s) = K_{s}I(s) $$

Funcion de trasferencia

$$ \frac{F_{s}(s)}{I(s)} = K_{s} $$

# SISTEMA MECANICO

![](90.jpg)

- El electroiman atrae una masa acoplada por medio de un resorte y se considera el amortiguamiento dado por la envolvente de la bobina. 

![](88.jpg)

$$ m \frac{d^{2}x}{dt^{2}} + b \frac{dx}{dt} + \kappa x = f(t) $$

Trasformada de LaPlace

$$ X(s) = F(s) \frac{1}{ms^{2} + bs + \kappa} $$

Intermedio 

$$ f(t) - KX - b \dot{x} = m \ddot{x} $$

$$ F(s) - KX(s) - bsX(s) = ms^{2}X(s) $$

$$ F(s) = X(s)ms^{2} + bsX(s) + KXs) $$

$$ F(s) = X(s)(ms^{2} + bs + K) $$

## REPRESENTACION EN BLOQUE

![](81.jpg)

![](82.jpg)

# Motor DC

![](83.jpg)

## MOTOR DC (CORRIENTE DE CAMPO) 
circuito elemtromagnetico.

![](84.jpg)

corriente de armadula es costante. 

$$ i_{a} = cte$$

$$ V_{c}(t) = V_{Rc} + V_{Lc} $$

$$ V_{c}(t) = {Rc}{Lc} + L \frac{dic}{dt} $$

$$ L_{c} \frac{di_{c}}{dt} + R_{c}i_{c} = v_{c(t)} $$

Trasformada de LaPlace

$$ L_{c}(s) = V_{c}(s) \frac{1}{(sL_{C} + R_{c})} $$

Funcion de trasferencia 

$$ \frac{I_{c}(s)}{V_{c}(s)} = \frac{l}{sL_{c} + R_{c}} $$

Parte intermedia 
Como se convierte la corriente en torque que es la que provoca el movimiento del eje.

- El flujo $\phi$ en el entrehierro es proporcional a la corriente de campo.

$$ \phi = K_{c}i_{c} $$

- El torque desarrollado es proporcional al $\phi$ y a la corriente de armadura.

$$ T_{m} = K_{a}i_{a}\Phi \Rightarrow T_{m} = K_{a}i_{a}(t)K_{c}i^{c}(t) \Rightarrow T_{m} = (K_{a}K_{c}i_{a})i_{c}(t) $$

$$ T_{m}(s) = (K_{a}K_{c}I_{a})I_{c}(s) = K_{m}I_{c}(s) \Rightarrow \frac{I_{m}(s)}{I_{c}(s)} = K_{m} $$

- El torque aplicado a la carga es el desarrollado por el motor menos la inercia de la carga.

$$ T_{c}(s) = T_{m}(s) - T_{p}(s) $$

- El torque aplicado (parte mecanica) a la carga se comporta como un sistema totacional clasico que considera la inercia y la friccion mecanica.
Ecuancion general

$$ J \frac{d^{2} \theta }{dt^{2}} + b \frac{d\theta }{dt} + \kappa \theta = \tau (t) $$

$$ \Theta (s) = T_{c}(s) \frac{1}{(s^{2}J + bs)} $$

Funcion de trasferencia 

$$ \frac{\theta (s)}{I_{c}(s)} = \frac{1}{s^{2}J + bs} $$ 

Se puede representar de la siguiente forma.

![](70.jpg)

Escrita matematicamente funcion de trasferencia para el motor DC.

$$ \Theta (s) = V_{c}(s)\frac{K_{m}}{(sL_{c} + R_{c})(Js^{2} + bs)} - T_{p}(s)\frac{1}{(Js^{2} + bs)} $$

$$ \frac{\Theta (s)}{V_{c}(s)} = \frac{K_{m}}{(sL_{c} + R_{c})(Js^{2} + bs)} $$

# MODELO DEL MOTOR DC (CORRIENTE DE ARMADURA) 

![](84.jpg)

- La corriebte de campo se asume constate por lo tanto el torque es: Parte electromecanica.

$$ T_{m}(s) = (K_{a}K_{c}I_{c})I_{a}(s) = K_{m}I_{a}(s) $$

- La corriente de armadura se relaciona con el volteje aplicando a la armadura por: Parte electrica
Transformada de LaPlace de la ecuacion Diferencial.

$$ V_{a}(t) = R_{a}i_{a}(t) + L_{a}\frac{di_{a}}{dt} + V_{b}(t) $$

$$ V_{a}(s) = (sL_{a} + R_{a}) I_{a}(s) + V_{b}(s) $$

Parte electrica y la parte electromecanica.
- El voltaje inducido en la armadura es proporcional a la velocidad angular del eje: 

$$ V_{b}(s) = K_{b}\omega (s) $$

Se reemplaza 

$$ V_{a}(s) = (sL_{a} + R_{a})I_{a}(s) + V_{b}(s) $$

Obtenemos, ecuacion 

$$ I_{a}(s) = \frac{V_{a}(s) - K_{b}\omega (s)}{sL_{a} + R_{a}} $$

Parte mecanica
- Se comporta de la misma manera que en el caso anterior:

$$ T_{c}(s) = T_{m}(s) - T_{p}(s) $$

$$ \Theta (s) = T_{c}(s)\frac{1}{(s^{2}J + bs)} $$

## DIAGRAMA DE BLOQUES RESULTANTE   

$$ I_{a} = \frac{V_{a} - K_{b}\omega }{L_{s} + R_{a}} $$

$$  L(\int f(t)dt) = \frac{F(s)}{s}$$

![](71.jpg)

# ELEMENTOS TRANSMISORES DE ENERGIA 
## ENGRANAJES Y POLEAS  
- Son dispositivos mecanicos que transmiten la energia desde una parte del sistema a otra.
- Los podemos usar ya sea para aumentar la cantidad de torque que se genera sobre una carga o la cantidad de velocidad.

![](60.jpg)


$$ \frac{T_{2}}{T_{1}}\Rightarrow \frac{N_{2}}{N_{1}} $$
 
$$ \frac{N_{2}}{N_{1}} = - \frac{\theta_{1} }{\theta_{2}} $$

## DIAGRAMA DE BLOQUES  

![](72.jpg)

## TRANSMISION ROTACIONAL A LINEAL 

![](73.jpg)

# PALANCAS

![](74.jpg)

Fuerzas y distacion son constantes.

$$ -\frac{f_{2}}{f_{1}} = \frac{d_{1}}{d_{2}} $$

Distacias y desplazamiento constantes. 

$$ \frac{d_{1}}{d_{2}} = \frac{x_{1}}{x_{2}} $$

# POTENCIOMETRO
## POTENCIOMETRO DE ROTACION  

![](75.jpg)

![](61.jpg)

## POTENCIOMETRO LINEAL 

$$ V_{0} = \frac{\theta }{\theta_{max}}V\propto $$

## POTENCIOMETRO LOGARITMICOS 

$$ V_{o} = Log_{10}\left ( \frac{\theta }{\theta Max} V_{cc} \right ) $$

## POTENCIOMETRO DE TRANSLACION  

![](62.jpg)

Funcion de transferencia todo va a estar a terminos de desplazamiento lineal.

$$ V_{0} = \frac{x}{x_{Max}}V_{\propto} $$

# TACOMETROS
- Son dispositivos que convierte la velocidad angular a voltaje.

![](63.jpg)

$$ v(t) = k \frac{d\theta (t)}{dt} $$

Funcion de transferencia 

$$ G(s) = \frac{V(s)}{\Theta (s)} = ks $$

# SENSORES TRANSMISORES  

![](64.jpg)

- Si son lineales

$$ H(s) = \frac{TO}{PV} = K $$

- si no son lineales, funcion de transferencia de primer grado

$$ H(s) = \frac{TO(s)}{PV(s)} = \frac{K_{T}}{\tau _{T}S+1} $$

# MODELOS DE OTROS PROCESOS  
## MEZCLA DE SUSTANCIAS  

![](65.jpg)

Funcion de transferencia 

$$G_{s} = \frac{Q(s)}{Q_{i}(s)} = \frac{\rho _ {inicial} s + \rho _ {in} v _ {in}}{s + v _ {out}} $$

## EJEMPLO DE CLASE 
- Sea un tanque lleno con ocho litros de agua salada en el cual estan disueltos dos kg de sal. Una solucion de salmuera ( agua salada) con tres kg de sal por litro entra al tanque a una velocidad de 4l/min, mientras la mezcla bien agitada sale a la misma velocidad con la que entra.

$$ G(s) = \frac{Q(s)}{Q_{i}(s)} = \frac{2s + 3 * 4}{s + 4} $$

## EJEMPLO DE TEMA
1. Sea un tanque lleno con 10 litros de agua salada en el cual están disueltos 1.5 kg de sal. Una solución de salmuera con 4 kg de sal por litro entra al tanque a una velocidad de 5 l/min, mientras la mezcla bien agitada sale a la misma velocidad con la que entra.
Funcion de transferencia

$$ G_{s} = \frac{Q(s)}{Q_{i}(s)} = \frac{1.5s+4*5}{s+5} = \frac{1.5s+20}{s+5} $$

2. Un tanque contiene 12 litros de agua salada con 3 kg de sal disueltos. Se agrega salmuera con una concentración de 2 kg por litro a una velocidad de 3 l/min, y al mismo tiempo, la mezcla agitada sale del tanque a la misma velocidad.
Funcion de transferencia 

$$ G_{s} = \frac{Q(s)}{Q_{i}(s)} = \frac{3s+2*3}{s+3} = \frac{3s+6}{s+3} $$

## SISTEMAS TERMICOS

![](66.jpg)

$$ G(s) = \frac{T(s)}{Q_{in}(s)} = \frac{1/C}{s+1/RC} $$

## EJEMPLO DE CLASE 

![](67.jpg)

Diagrama de bloques 

![](68.jpg)

# EJEMPLO DE TEMA 
1. Tenemos el siguiente sistema hidraulico:

![](40.jpeg)

Teniendo esto presente nos disponemos a realizar el modelamiento de este sistema:

$$ Q_{1}(t) - Q_{2}(t) = \frac{\mathrm{d} V}{\mathrm{d} t} $$

$$ V = A\cdot h(t) $$

Reemplazamos

$$ Q_{1}(t) - f(P_{T} - P_{atm}) = A\cdot\frac{\mathrm{d} h(t)}{\mathrm{d} t} $$

Donde

$$ Q_{1}(t) - f(P_{T} - P_{atm}) = A\cdot\frac{\mathrm{d} h(t)}{\mathrm{d} t} $$

Entonces obtenemos

$$ Q_{1} - f(pgh(t)) = A\frac{\mathrm{d} h(t)}{\mathrm{d} t} $$

Despejamos y obtenemos la funcion de transferencia

$$ (Q_{1} - f(pgh(t))) \frac{1}{A} = \frac{\mathrm{d} h(t)}{\mathrm{d} t} $$

Una vez obtenemos la funcion de transferencia el diagrama de bloques que obtenemos es

![](41.jpeg)

2.Tenemos el siguiente sistema mecanico:

![](42.jpeg)

Teniendo esto en cuenta se dispone a realizar el modelamiento del sistema:

$$ F(t) - kx(t) - b( \frac{\mathrm{d} x(t)}{\mathrm{d} t}) = M \frac{\mathrm{d^{2}} x(t)}{\mathrm{d} t^{2}} $$

Despejamos la ecuacion

$$ F(t) - b(\frac{\mathrm{d} x(t)}{\mathrm{d} t}) - M \frac{\mathrm{d^{2}} x(t)}{\mathrm{d} t^{2}} = kx(t) $$

Finalmente obtenemos la funcion de transferencia del sistema

$$ (F(t) - b ( \frac{\mathrm{d} x(t)}{\mathrm{d} t}) - M\frac{\mathrm{d^{2}} x(t)}{\mathrm{d} t^{2}}) \frac{1}{k} = x(t) $$

Habiendo hecho el modelamiento el diagrama de bloques que obtenemos es

![](43.jpeg)
