# Arduino Ports Registers(Registro de puertos)

Los registros de puertos permiten una manipulación más rápida y de menor nivel de los pines de E/S del microcontrolador en una placa Arduino. Los chips utilizados en la placa Arduino (ATmega8 y ATmega168) tienen tres puertos

* B (pin digital 8 a 13)
* C (pines de entrada analógica)
* D (pines digitales de 0 a 7)

PORTD se asigna a los pines digitales Arduino 0 a 7

DDRD - El registro de dirección de datos del puerto D - lectura / escritura
PORTD - El registro de datos del puerto D - lectura / escritura
PIND - El registro de pines de entrada del puerto D - solo lectura

PORTB se asigna a los pines digitales Arduino 8 a 13 Los dos bits altos (6 y 7) se asignan a los pines de cristal y no son utilizables

DDRB - El registro de dirección de datos del puerto B - lectura / escritura
PORTB - El registro de datos del puerto B - lectura / escritura
PINB - Registro de pines de entrada del puerto B - solo lectura

Los mapas PORTC a los pines analógicos Arduino 0 a 5. Los pines 6 y 7 solo son accesibles en el Arduino Mini

DDRC - El registro de dirección de datos del puerto C - lectura / escritura
PORTC - El registro de datos del puerto C - lectura / escritura
PINC - Registro de pines de entrada del puerto C - solo lectura

Sin embargo, debe tener en cuenta que los pines 0 y 1 se utilizan para las comunicaciones en serie para programar y depurar el Arduino, por lo que generalmente debe evitarse el cambio de estos pines a menos que sea necesario para las funciones de entrada o salida en serie. Tenga en cuenta que esto puede interferir con la descarga o depuración del programa.

**Ejemplo con codigo**
PORTD = B10101000; // sets digital pins 7,5,3 HIGH

