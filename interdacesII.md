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
<img width="1590" height="826" alt="image" src="https://github.com/user-attachments/assets/4064b4ac-5bff-405a-a1b5-defcd96f5502" />

##### Ejercicio n°2 LED Intermitente (Blink)
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
<img width="1541" height="811" alt="image" src="https://github.com/user-attachments/assets/edbaa7f5-d90a-4121-8665-378d23acd376" />


```
### Ejercicio n°3 Led con pulsador
```
void setup() {
  pinMode(2, INPUT);  // Botón como entrada
  pinMode(13, OUTPUT);
}
void loop() {
  if (digitalRead(2) == HIGH) {  // Si se presiona el botón
    digitalWrite(13, HIGH);
  } else {
    digitalWrite(13, LOW);
  }
}
<img width="1426" height="814" alt="image" src="https://github.com/user-attachments/assets/dae40f41-6f5e-4f76-b54a-45adeb1a7f3e" />
```


### Ejercicio n°4 Led con potenciometro
```
void setup() {
  pinMode(9, OUTPUT);  // Pin PWM (símbolo ~)
}
void loop() {
  int valor = analogRead(A0);           // Leer potenciómetro (0-1023)
  int brillo = map(valor, 0, 1023, 0, 255);  // Convertir a rango PWM
  analogWrite(9, brillo);               // Ajustar brillo
}
<img width="1189" height="833" alt="image" src="https://github.com/user-attachments/assets/9e32be1c-1e01-4804-88ab-c8c10252cde4" />

```

### Ejercicio n°5 Semaforo arduino
```
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
### Semaforo intermitente

/ C++ code - Semáforo Autos y Peatones

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

  //  Parte 1: Verde peatones encendido fijo
digitalWrite(LED_4, HIGH);
delay(3000); // 3 segundos fijo

  //  Parte 2: Verde peatones parpadeando
for (int i = 0; i < 5; i++) {   // Parpadea 5 veces
  digitalWrite(LED_4, LOW);     // Apagar
  delay(300);                   // 0.3s
  digitalWrite(LED_4, HIGH);    // Encender
  delay(300);                   // 0.3s
}

  // 🚦 Fase 4: Rojo autos, rojo peatones (tiempo intermedio)
  //digitalWrite(LED_4, LOW);   // Verde peatones apagado
  //digitalWrite(LED_5, HIGH);  // Rojo peatones encendido
  //delay(2000); // 2 segundos
}

<img width="1525" height="796" alt="image" src="https://github.com/user-attachments/assets/82baf371-d4a2-42fa-81c9-d64b49ca0d4e" />

```

### Ejercicio n°6 Boton+potenciometro processing
```
Arduino:
int buttonPin = 2;       // Pin del botón
int potPin = A0;         // Pin del potenciómetro
int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP); // Botón con resistencia interna
  Serial.begin(9600);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) {   // Botón presionado
    int potValue = analogRead(potPin);   // 0 - 1023
    Serial.print("BTN,");     // etiqueta para Processing
    Serial.println(potValue); // mando el valor junto con el evento
    delay(200);               // debounce simple
  }
}


Processing:

import processing.serial.*;

Serial myPort;
ArrayList<CircleData> circles; 

void setup() {
  size(1200, 720);
  background(0);
  
  // Ajusta el puerto según tu Arduino
  println(Serial.list());
  myPort = new Serial(this, "/dev/cu.usbmodem1101", 9600);
  //myPort = new Serial(this, Serial.list()[0], 9600);
  
  circles = new ArrayList<CircleData>();
}

void draw() {
  //background(0);
  
  // Dibujar todos los círculos guardados
  //fill(0, 150, 255);
  //noStroke();
  fill(0, 0, 0);
  stroke(255, 0, 0);
  for (CircleData c : circles) {
    ellipse(c.x, c.y, c.size, c.size);
  }
  
  // Leer datos de Arduino
  if (myPort.available() > 0) {
    String val = myPort.readStringUntil('\n');
    if (val != null) {
      val = trim(val);
      if (val.startsWith("BTN")) {
        // Extraer el valor del potenciómetro
        String[] parts = split(val, ',');
        if (parts.length == 2) {
          float potVal = float(parts[1]);
          float circleSize = map(potVal, 0, 1023, 10, 100); // tamaño 10-100 px
          circles.add(new CircleData(random(width), random(height), circleSize));
        }
      }
    }
  }
}

// Clase para guardar datos de cada círculo
class CircleData {
  float x, y, size;
  CircleData(float x, float y, float size) {
    this.x = x;
    this.y = y;
    this.size = size;
  }
}
<img width="1195" height="755" alt="Captura de pantalla 2025-09-01 105539" src="https://github.com/user-attachments/assets/d22598e7-9e5f-45cd-a6bc-5b98a8e22fef" />

```

### Ejercicio n°7 Pulsador + arduino + processing
```
Codigo arduino: int buttonPin = 2;  // Pin del botón
int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP); // Botón con resistencia interna
  Serial.begin(9600);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) {   // Botón presionado
    Serial.println(1);        // Enviar un "1" a Processing
    delay(200);               // Evitar rebotes
  }
}

Processing: 
import processing.serial.*;

Serial myPort;
ArrayList<PVector> circles; 

void setup() {
  size(1920, 1080);
  background(0);
  
  // Ajusta el nombre del puerto según tu Arduino
  println(Serial.list());
  //myPort = new Serial(this, "/dev/cu.usbmodem1101", 9600);
  myPort = new Serial(this, Serial.list()[0], 9600);
  
  circles = new ArrayList<PVector>();
}

void draw() {
  //background(0);
  
  // Dibujar círculos almacenados
  fill(#2A890E);
  //noStroke();
  stroke(0, 0, 0);
  for (PVector c : circles) {
    ellipse(c.x, c.y, 200, 200);
  }
  
  // Revisar si llega algo de Arduino
  if (myPort.available() > 0) {
    String val = myPort.readStringUntil('\n');
    if (val != null) {
      val = trim(val);
      if (val.equals("1")) {
        // Cada vez que se aprieta el botón, agregar un círculo en posición aleatoria
        circles.add(new PVector(random(width), random(height)));
      }
    }
  }
}

```
### Ejercicio n°8 Arduino + pulsador + potenciometro + processing
```
Codigo Arduino:
int buttonPin = 2;       // Pin del botón
int potPin = A0;         // Pin del potenciómetro
int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP); // Botón con resistencia interna
  Serial.begin(9600);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) {   // Botón presionado
    int potValue = analogRead(potPin);   // 0 - 1023
    Serial.print("BTN,");     // etiqueta para Processing
    Serial.println(potValue); // mando el valor junto con el evento
    delay(200);               // debounce simple
  }
}

Codigo Processing:
import processing.serial.*;

Serial myPort;
ArrayList<CircleData> circles; 

void setup() {
  size(1200, 720);
  background(0);
  
  // Ajusta el puerto según tu Arduino
  println(Serial.list());
  myPort = new Serial(this, "/dev/cu.usbmodem1101", 9600);
  //myPort = new Serial(this, Serial.list()[0], 9600);
  
  circles = new ArrayList<CircleData>();
}

void draw() {
  //background(0);
  
  // Dibujar todos los círculos guardados
  fill(#F77AC3);
  //noStroke();
  fill(#F77AC3);
  stroke(0, 0, 0);
  for (CircleData c : circles) {
    ellipse(c.x, c.y, c.size, c.size);
  }
  
  // Leer datos de Arduino
  if (myPort.available() > 0) {
    String val = myPort.readStringUntil('\n');
    if (val != null) {
      val = trim(val);
      if (val.startsWith("BTN")) {
        // Extraer el valor del potenciómetro
        String[] parts = split(val, ',');
        if (parts.length == 2) {
          float potVal = float(parts[1]);
          float circleSize = map(potVal, 0, 1023, 10, 100); // tamaño 10-100 px
          circles.add(new CircleData(random(width), random(height), circleSize));
        }
      }
    }
  }
}

// Clase para guardar datos de cada círculo
class CircleData {
  float x, y, size;
  CircleData(float x, float y, float size) {
    this.x = x;
    this.y = y;
    this.size = size;
  }
}
```
### Ejercicio n°9 Botonera con sonidos/ funciones if + else
```
Codigo arduino:
// --- Configuración de botones ---
const int numButtons = 3;
const int buttonPins[numButtons] = {2, 4, 7};
const int ledButtonPins[numButtons] = {9, 10, 11}; // LEDs botones

// --- Configuración de potenciómetros ---
const int numPots = 2;
const int potPins[numPots] = {A0, A1};
const int ledPotPins[numPots] = {3, 5}; // LEDs PWM

// Variables de estados previos
int lastButtonState[numButtons];
int lastPotValue[numPots];

void setup() {
  Serial.begin(9600);

  // Configurar botones y LEDs
  for (int i = 0; i < numButtons; i++) {
    pinMode(buttonPins[i], INPUT_PULLUP);
    pinMode(ledButtonPins[i], OUTPUT);
    lastButtonState[i] = digitalRead(buttonPins[i]);
  }

  // Configurar LEDs de potenciómetros
  for (int i = 0; i < numPots; i++) {
    pinMode(ledPotPins[i], OUTPUT);
    lastPotValue[i] = analogRead(potPins[i]);
  }
}

void loop() {
  // Leer y enviar botones
  for (int i = 0; i < numButtons; i++) {
    int buttonState = digitalRead(buttonPins[i]);

    // LED se enciende cuando botón está presionado
    digitalWrite(ledButtonPins[i], buttonState == LOW ? HIGH : LOW);

    if (buttonState != lastButtonState[i]) {  // enviar cambios
      Serial.print("B");
      Serial.print(i); 
      Serial.print(":");
      Serial.println(buttonState);
      lastButtonState[i] = buttonState;
    }
  }

  // Leer y enviar potenciómetros
  for (int i = 0; i < numPots; i++) {
    int potValue = analogRead(potPins[i]); // 0–1023
    int pwmValue = potValue / 4;           // 0–255

    // Ajustar LED según valor
    analogWrite(ledPotPins[i], pwmValue);

    if (abs(pwmValue - lastPotValue[i]) > 2) { // evitar ruido
      Serial.print("P");
      Serial.print(i);
      Serial.print(":");
      Serial.println(pwmValue);
      lastPotValue[i] = pwmValue;
    }
  }

  delay(10);
}

Codigo processing: 
// Importamos librería para comunicación serial
import processing.serial.*;
// Importamos librería Minim para manejar audio
import ddf.minim.*;

// Declaramos el objeto serial para comunicarnos con Arduino
Serial myPort;
// Objeto principal de Minim
Minim minim;
// Array de reproductores de audio (3 pistas)
AudioPlayer[] players;
// Variable para guardar el índice de la pista que está sonando
int currentTrack = -1;  // -1 significa que no hay pista activa al inicio

void setup() {
  size(400, 200); // Ventana de 400x200 píxeles
  
  // --- Configuración del puerto serial ---
  printArray(Serial.list()); // Muestra en consola la lista de puertos disponibles
  myPort = new Serial(this, Serial.list()[0], 9600); // Abrimos el primer puerto de la lista a 9600 baudios
  
  // --- Configuración de audio ---
  minim = new Minim(this); // Inicializamos Minim
  players = new AudioPlayer[3]; // Creamos un array de 3 reproductores
  
  // Cargamos los 3 archivos de audio desde la carpeta "data"
  players[0] = minim.loadFile("Gyaru-1.mp3", 2048); 
  players[1] = minim.loadFile("shaw.mp3", 2048); 
  players[2] = minim.loadFile("gato.mp3", 2048); 
}

void draw() {
  background(0); // Fondo negro
  fill(255);     // Color blanco para el texto
  textSize(16);  // Tamaño del texto
  
  // Mostramos en pantalla qué botón está activo
  text("Botón actual: " + (currentTrack == -1 ? "ninguno" : currentTrack), 20, 40);
}

void serialEvent(Serial myPort) {
  // Leemos la cadena que llega desde Arduino hasta el salto de línea
  String inString = trim(myPort.readStringUntil('\n'));
  
  // Si no llega nada, salimos
  if (inString == null) return;

  // --- Si el mensaje recibido empieza con "B" significa que es un botón ---
  if (inString.startsWith("B")) {
    // Quitamos la letra "B" y separamos el mensaje en partes (ejemplo "0:0")
    String[] parts = split(inString.substring(1), ':');
    
    // Si realmente recibimos dos partes (índice y estado)
    if (parts.length == 2) {
      int buttonIndex = int(parts[0]); // Número del botón (0,1,2)
      int state = int(parts[1]);       // Estado del botón (0 = presionado, 1 = suelto)
      
      // Si el botón fue presionado (LOW = 0 en Arduino)
      if (state == 0) { 
        playTrack(buttonIndex); // Llamamos a la función para reproducir la pista correspondiente
      }
    }
  }
}

// --- Función que reproduce una pista según el botón ---
void playTrack(int index) {
  // Si ya había una pista sonando, la pausamos y la rebobinamos al inicio
  if (currentTrack != -1 && players[currentTrack].isPlaying()) {
    players[currentTrack].pause();
    players[currentTrack].rewind();
  }
  
  // Reproducimos en bucle la pista seleccionada
  players[index].loop();
  
  // Actualizamos la variable para saber cuál es la pista activa
  currentTrack = index;
}
<img width="1346" height="806" alt="image" src="https://github.com/user-attachments/assets/d6a79f3a-37e8-4abb-8bed-670e114af7f1" />


```


Ejercicio n°10 ejercicio a eleccion:
Semaforo mas musica (se utilizo la ayuda de chatGPT para los codigos)
```
codigo arduino:
int ledsArriba[] = {6, 7, 8}; // 3 LEDs arriba (volumen)
int ledsAbajo[] = {9, 10};    // 2 LEDs abajo (beat)

void setup() {
  Serial.begin(9600);
  for (int i = 0; i < 3; i++) pinMode(ledsArriba[i], OUTPUT);
  for (int i = 0; i < 2; i++) pinMode(ledsAbajo[i], OUTPUT);
}

void loop() {
  if (Serial.available() > 0) {
    String data = Serial.readStringUntil('\n'); // leer línea completa
    data.trim();
    
    if (data.length() > 0 && data.indexOf(',') != -1) {
      int commaIndex = data.indexOf(',');
      int volume = data.substring(0, commaIndex).toInt();
      int beat = data.substring(commaIndex + 1).toInt();

      // --- LEDs de arriba (volumen) ---
      for (int i = 0; i < 3; i++) {
        if (i < volume) digitalWrite(ledsArriba[i], HIGH);
        else digitalWrite(ledsArriba[i], LOW);
      }

      // --- LEDs de abajo (beat) ---
      for (int i = 0; i < 2; i++) {
        digitalWrite(ledsAbajo[i], beat == 1 ? HIGH : LOW);
      }
    }
  }
}

Codigo Processing:

import processing.serial.*;
import ddf.minim.*;
import ddf.minim.analysis.*;

Minim minim;
AudioPlayer song;
BeatDetect beat;
Serial myPort;

// --- Lista de canciones disponibles ---
String[] canciones = {
  "ado.mp3",
  "canary.mp3",
  "charles.mp3",
  "cuchito.mp3"
};

String nombreActual = ""; // nombre de la canción actual

void setup() {
  size(400, 200);
  
  minim = new Minim(this);
  reproducirNuevaCancion(); // arranca con una canción al azar
  
  beat = new BeatDetect();
  
  // --- Configurar Serial ---
  printArray(Serial.list());
  myPort = new Serial(this, Serial.list()[0], 9600);
}

void draw() {
  background(0);
  fill(255);
  
  // --- Detectar nivel de volumen ---
  float level = song.mix.level();
  int volumeLevel = (int)map(level, 0, 0.5, 0, 3);
  
  // --- Detectar beats ---
  beat.detect(song.mix);
  int beatActive = beat.isOnset() ? 1 : 0;
  
  // --- Mostrar información ---
  text("Volumen LEDs: " + volumeLevel, 20, 40);
  text("Beat: " + beatActive, 20, 70);
  text("Pista actual: " + nombreActual, 20, 100);
  text("Presiona ESPACIO para cambiar de canción", 20, 140);
  
  // --- Enviar datos a Arduino ---
  String data = volumeLevel + "," + beatActive + "\n";
  myPort.write(data);
  
  // --- Si la canción termina sola, pasar a otra ---
  if (!song.isPlaying()) {
    reproducirNuevaCancion();
  }
}

// --- Reproducir una canción aleatoria ---
void reproducirNuevaCancion() {
  if (song != null) {
    song.close();
  }
  
  int indice = (int)random(canciones.length);
  nombreActual = canciones[indice];
  println("🎵 Reproduciendo: " + nombreActual);
  
  song = minim.loadFile(nombreActual, 2048);
  song.play();
  beat = new BeatDetect();
}

// --- Detectar tecla presionada ---
void keyPressed() {
  if (key == ' ') {
    println("⏭ Cambio manual de canción");
    reproducirNuevaCancion();
  }
}
}
```
