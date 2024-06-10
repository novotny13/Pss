# Pss<br>
Dokumentace <br>
<h1> Úvod </h1><br>
Tento projekt popisuje konstrukci a použití dávkovací krabičky, která využívá Arduino Nano R3 a servomotory pro přesné dávkování různých látek.<br>
 <h1> Použité komponenty </h1> <br>
1.Arduino Nano R3: Mikrokontrolér pro řízení celého systému.<br>
2.Servomotor: Používají se k ovládání mechanizmů pro dávkování.<br>
3.Napájecí zdroj: 5V zdroj pro napájení Arduino Nano a servomotorů.<br>
4.Dávkovací mechanismus: Konstrukce, která umožňuje přesné dávkování.<br>
5.Spojovací materiál: Kabely, konektory a případně prototypová deska.<br>
 <h1> Ukázka kódu </h1> <br>

 
 ```
 #include <Servo.h>

Servo myservo;

void setup() {
  myservo.attach(9);
  myservo.write(80);
}

void loop() {
  myservo.write(105);  // vydání cigarety/tužky
  delay(70);    

  myservo.write(80); 
  delay(3600000);      // čekání 1 hodiny (3600000 milisekund)
}
```
