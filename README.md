# 🧑‍💻 Sistemas Embebidos I – mi repositorio 

📚 *Carrera:* Ingeniería Biomédica  
🏫 *Materia:* Sistemas Embebidos I  
👨‍🏫 *Docente:* Alan Cornejo 

👩‍🎓 *Integrantes:*  
- José Antonio Fernández Espíndola 

---

## 📌 Descripción
Este repositorio contiene el desarrollo del proyecto de la materia *Sistemas Embebidos I, orientado a la aplicación de técnicas de programación, hardware y software impartidos en la materia.  
El objetivo es poner en práctica el uso de *microcontroladores, sensores, comunicación y control* en un sistema embebido real.

---



// Programa: Encender 10 LEDs en secuencia

// Intervalo: 2 segundos entre cada LED

const int numLeds = 10;          // Cantidad de LEDs
int leds[numLeds] = {2,3,4,5,6,7,8,9,10,11}; // Pines digitales de Arduino donde van conectados los LEDs


void setup() {
  // Configurar cada pin como salida
  for (int i = 0; i < numLeds; i++) {
    pinMode(leds[i], OUTPUT);
  }
}


void loop() {
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(leds[i], HIGH);   // Encender LED
    delay(2000);                   // Esperar 2 segundos
    // Si quieres que quede encendido, comenta la siguiente línea
    digitalWrite(leds[i], LOW);    // Apagar LED
  }
}