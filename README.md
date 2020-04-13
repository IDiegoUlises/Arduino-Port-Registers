# Arduino Ports Registers(Registro de puertos)

Los registros de puertos permiten una manipulación mas rapida y de menor nivel de los pines de I/O del microcontrolador en una placa Arduino. Los chips utilizados en la placa Arduino (ATmega8 y ATmega168) tienen tres puertos

<img src="https://github.com/IDiegoUlises/Arduino-Port-Registers/blob/master/Images/Registro-de-puertos.png" width="450" height="350" />

* **B (pin digital 8 a 13)**
* **C (pines de entrada analogica)**
* **D (pines digitales de 0 a 7)**



**PORTD se asigna a los pines digitales Arduino 0 a 7**
* DDRD El registro de direccion de datos del puerto D I/0
* PORTD El registro de datos del puerto D I/O 
* PIND El registro de pines de entrada del puerto D solo lectura 

**PORTB se asigna a  pines digitales Arduino 8 a 13 Los dos bits altos (6 y 7) se asignan a los pines de cristal y no son utilizables**
* DDRB El registro de dirección de datos del puerto B I/0
* PORTB El registro de datos del puerto B I/O
* PINB Registro de pines de entrada del puerto B solo lectura

**Los mapas PORTC a los pines analógicos Arduino 0 a 5. Los pines 6 y 7 solo son accesibles en el Arduino Mini**
* DDRC El registro de dirección de datos del puerto C I/O
* PORTC El registro de datos del puerto C I/O
* PINC Registro de pines de entrada del puerto C solo lectura

Debe tener en cuenta que los pines 0 y 1 se utilizan para las comunicaciones en serie para programar y depurar el Arduino, por lo que generalmente debe evitarse el cambio de estos pines a menos que sea necesario para las funciones de entrada o salida en serie. Tenga en cuenta que esto puede interferir con la descarga o depuracion del programa.

## Encender un led de manera habitual 
```C++
int led = 3;
pinMode(led,OUTPUT);
digitalWrite(led,HIGH);
```

**Encender un led con el puerto digital y el registro de puertos**
```C++
pinMode(3,OUTPUT);
PORTD = B00001000; //Remplaza digitalWrite y declara Pin 3 como HIGH
```

**Encender un led utilizando solo el registro de puertos**
```c++
DDRD = B00001000; //Remplaza el pinMode y declara pin 3 como OUTPUT
PORTD = B00001000; //Pin 3 como HIGH
```
