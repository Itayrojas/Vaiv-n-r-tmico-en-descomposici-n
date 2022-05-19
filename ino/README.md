# ino
## Codigo Luces y potenciometro

- const int LEDRojo =3;  // indicando que el led se encuentra en el pin3
- const int LEDAzul =8;
- const int potenciometro =0; // el potenciometro esta conectado al pin A0
- int intensidad;  //variable para la intensidad de brillo
- void setup() {
- // No se necesitan declaran los pines analogicos
- //ya que se realiza automáticamente
- pinMode (LEDRojo, OUTPUT); 
- pinMode (LEDAzul, OUTPUT);// declaramos el led como salida
- }
- void loop() {
- //los valores analogicos se usan entre 0 y 255
- //asi que el valor del potenciometro lo dividos en 4
- intensidad = analogRead (potenciometro) / 4; //analogWrite recibe los valores analogicos del pin
- analogWrite(LEDRojo, intensidad);
- analogWrite(LEDAzul, intensidad);
- }

## Cableado

![Ejemplo cableado arduino y luces](https://wiki.ead.pucv.cl/images/f/f0/Arduinodixentrega3DiVaI_%281%29.png)

## Codigo Motor Servo/ Sensor ultrasonico

- #include <Servo.h>
- Servo myservo;  // crea el objeto servo
- int pos = 0;    // posicion del servo
- void setup() {
- myservo.attach(9);  // vincula el servo al pin digital 9
- }
- void loop() {
- //varia la posicion de 0 a 180, con esperas de 15ms
- for (pos = 0; pos <= 90; pos += 1) 
- {
- myservo.write(pos);              
- delay(30);                       
- }
- //varia la posicion de 180 a 0, con esperas de 15ms
- for (pos = 90; pos >= 0; pos -= 1) 
- {
- myservo.write(pos);              
- delay(30);                       
- }
- }

## Cableado
![Ejemplo cableado arduino y motor](https://wiki.ead.pucv.cl/images/thumb/e/ef/Arduinodixentrega3DiVaI_%282%29.jpg/400px-Arduinodixentrega3DiVaI_%282%29.jpg)
