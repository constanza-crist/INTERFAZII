# INTERFAZII

#### Ejercicio n°1: Hola mundo!" en Arduino

```
void setup () {
  Serial.begin(9600);
  Serial.println("I am selfish, I am broken, I am cruel, I am all the things they might have said to you");
}

void loop() {

}
```

##### LED Intermitente (Blink)
```js

#### Ejercicio n°2: Semaforo
void setup () {
   pinMode (13, OUTPUT);
  pinMode (8, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH) ;
  delay(1000);
    digitalWrite(13, LOW);
  delay(3000);
  
  void loop () ;
  digitalWrite(8, HIGH) ;
  delay(100);
    digitalWrite(8, LOW);
  delay(500);
}




```
void setup(){ 
  pinMode(2, INPUT) ;
  pinMode(13, OUTPUT);
}
void loop() { 
  if (digitalRead (2) == HIGH);
 else { 
  digitalWrite(13, LOW);
   }
}
```
###Semaforo arduino

// C++ code - Semáforo Autos y Peatones

// Definición de pines
int LED_1 = 6;  // Luz roja autos
int LED_2 = 7;  // Luz amarilla autos
int LED_3 = 8;  // Luz verde autos
int LED_4 = 9;  // Luz verde peatones
int LED_5 = 10; // Luz roja peatones

void setup() {
  // Configuramos todos los pines como salida
  pinMode(LED_1, OUTPUT);
  pinMode(LED_2, OUTPUT);
  pinMode(LED_3, OUTPUT);
  pinMode(LED_4, OUTPUT);
  pinMode(LED_5, OUTPUT);
}

void loop() {
  // 🚦 Fase 1: Autos en verde, peatones en rojo
  digitalWrite(LED_1, LOW);   // Rojo autos apagado
  digitalWrite(LED_2, LOW);   // Amarillo autos apagado
  digitalWrite(LED_3, HIGH);  // Verde autos encendido
  digitalWrite(LED_4, LOW);   // Verde peatones apagado
  digitalWrite(LED_5, HIGH);  // Rojo peatones encendido
  delay(5000); // 5 segundos

  // 🚦 Fase 2: Amarillo autos, peatones siguen en rojo
  digitalWrite(LED_3, LOW);   // Verde autos apagado
  digitalWrite(LED_2, HIGH);  // Amarillo autos encendido
  delay(2000); // 2 segundos
  digitalWrite(LED_2, LOW);   // Amarillo autos apagado

  // 🚦 Fase 3: Rojo autos, verde peatones
  digitalWrite(LED_1, HIGH);  // Rojo autos encendido
  digitalWrite(LED_5, LOW);   // Rojo peatones apagado
  digitalWrite(LED_4, HIGH);  // Verde peatones encendido
  delay(5000); // 5 segundos

  // 🚦 Fase 4: Rojo autos, rojo peatones (tiempo intermedio)
  //digitalWrite(LED_4, LOW);   // Verde peatones apagado
  //digitalWrite(LED_5, HIGH);  // Rojo peatones encendido
  //delay(2000); // 2 segundos


<img width="1562" height="818" alt="Captura de pantalla 2025-08-25 101355" src="https://github.com/user-attachments/assets/b9235a09-4ce0-4c8d-850e-81d14a56b18e" />

}

