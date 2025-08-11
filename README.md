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
