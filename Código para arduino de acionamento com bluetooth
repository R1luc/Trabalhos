#include <SoftwareSerial.h>


// Defina os pinos do HC-06
SoftwareSerial BTSerial(10, 11); // RX, TX (pino 10 para RX e pino 11 para TX)


// Defina o pino do circuito a ser controlado (por exemplo, um LED ou relé)
const int circuitoPin = 7;


void setup() {
// Inicia a comunicação com o módulo Bluetooth HC-06
  BTSerial.begin(9600); // A taxa padrão de comunicação do HC-06 é 9600 bps


  // Configura o pino do circuito como saída
  pinMode(circuitoPin, OUTPUT);
  digitalWrite(circuitoPin, LOW); // Começa com o circuito desligado
}


void loop() {
  // Se houver dados disponíveis do Bluetooth
  if (BTSerial.available()) {
    char comando = BTSerial.read(); // Lê o comando do Bluetooth


    // Verifica o comando recebido
    if (comando == '1') {
      // Liga o circuito (por exemplo, acende o LED ou aciona o relé)
      digitalWrite(circuitoPin, HIGH);
    }
    else if (comando == '0') {
      // Desliga o circuito (por exemplo, apaga o LED ou desativa o relé)
      digitalWrite(circuitoPin, LOW);
    }
  }
}
