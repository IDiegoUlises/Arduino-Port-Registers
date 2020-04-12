# Arduino Port Registers 

Los registros de puertos permiten una manipulación más rápida y de menor nivel de los pines de E / S del microcontrolador en una placa Arduino. Los chips utilizados en la placa Arduino ( ATmega8 y ATmega168 ) tienen tres puertos:

B (pin digital 8 a 13)
C (pines de entrada analógica)
D (pines digitales de 0 a 7)
Cada puerto está controlado por tres registros, que también son variables definidas en el idioma arduino. El registro DDR determina si el pin es una ENTRADA o SALIDA. El registro PORT controla si el pin es ALTO o BAJO, y el registro PIN lee el estado de los pines INPUT configurados para ingresar con pinMode (). Los mapas de los chips ATmega8 y ATmega168 muestran los puertos. El nuevo chip Atmega328p sigue exactamente el pinout del Atmega168.

* B (pin digital 8 a 13)
* C (pines de entrada analógica)
* D (pines digitales de 0 a 7)
