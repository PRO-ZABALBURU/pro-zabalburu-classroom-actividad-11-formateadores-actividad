# Instrucciones
Se pide diseñar una clase que nos permita **gestionar los pagos de un préstamo hipotecario**. En un préstamo hipotecario se emplea el sistema francés que calcula un `pago` constante para todos los `periodos` (meses) del préstamo. Dicho pago incluye los intereses del capital pendiente de devolver y una cantidad a descontar (amortizar) de dicho capital. Para el siguiente mes la cantidad a pagar de intereses es menor (dado que el capital ha disminuido) con lo que la cantidad a amortizar será mayor (dado que el pago, como ya se ha dicho es siempre el mismo)

 

La clase `Prestamo` dispondrá de los siguientes campos:

 

- `capital` : la cantidad de dinero prestada

- `interés` : el tipo de interés (un % anual). Por ejemplo 0,015 → 1,5%)

- `años` : el número de años a los que se ha concedido el préstamo

- `fecha` : la fecha de formalización del préstamo. 

 

La clase dispondrá de los métodos set/get habituales y de un constructor sin argumentos y otro que reciba toda la información.

 

Además en la clase se deberá definir el siguiente método:

 

pago() : Esta función retornará el pago mensual de la hipoteca. Este pago es el mismo todos los meses y se calcula según la siguiente fórmula (emplear la función pow de la clase Math):

 

pago = (Co * i) / (1 - (1 + i)-n)

C0 es el capital
i es el interés mensual (el interés que tenemos dividido entre 12)
n es el número de periodos (meses), por tanto años multiplicado por 12
 

Se pide diseñar un programa que nos permita mostrar la tabla de amortización de un préstamo. Es decir cuánto se debe pagar cada periodo, cuanto se amortiza (qué parte del préstamo se paga) y cuánto se paga de intereses.

 

El programa solicitará los datos de un préstamo. Para ello se empleará un formateador de números decimales para el capital, un formateador de tipo porcentaje (con dos decimales) para el interés anual y un formateador de fecha corta para la fecha de formalización del préstamo. Con esos datos se creará un objeto de tipo Prestamo.

 

Al final del proceso deberá mostrarse el siguiente cuadro de amortización :

 

Periodo    Fecha       Capital     Pago        Amortización           Intereses

1          fecha       capital     pago        amortización           intereses

…

 

Total Pagado : sumaPagos

Intereses Pagados : sumaIntereses

 

El proceso a realizar será el siguiente

Guardamos en una variable llamada capital el capital inicial y en otra llamada fecha la fecha de formalización del préstamo

Dado que el pago es fijo, conviene guardarlo en una variable

Repetimos el siguiente proceso tantas veces como periodos tenga el préstamo (empezando desde 1)

Calculamos los intereses a pagar en el periodo (el capital multiplicado por el tipo de interés mensual (recordar dividirlo entre 12) )

Obtenemos la amortización (el pago menos los intereses)

Mostramos los datos por pantalla correctamente formateados

Restamos la amortización del capital

Sumamos un mes más a la fecha
