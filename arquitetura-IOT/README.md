# markdown# 🤖 Aula: Hardware e Programação em IoT

## 1. O Ecossistema Arduino na IoT
O Arduino atua na **Camada de Percepção**. Ele é responsável por ler o mundo físico (sensores) e executar ações (atuadores).

### Componentes Principais:
*   **Microcontrolador:** O "cérebro" (ATmega328P no Uno, ESP32 para projetos com Wi-Fi).
*   **Entradas/Saídas (I/O):** Pinos digitais e analógicos.
*   **Comunicação:** Serial (UART), I2C e SPI.

---

## 2. Programação C++ (O Padrão Arduino)
A linguagem padrão do Arduino é um framework baseado em C++. É ideal para performance e controle direto do hardware.

### Estrutura Básica:
```cpp
// Definição de pinos
const int LED_PIN = 13;

void setup() {
  // Executa uma vez ao iniciar
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  // Executa em loop infinito
  digitalWrite(LED_PIN, HIGH);
  Serial.println("LED Aceso");
  delay(1000); 
  digitalWrite(LED_PIN, LOW);
  delay(1000);
}
```

---

## 3. Python na Arquitetura IoT
O Python entra em cena em dois cenários principais:

### A. Python no Host (PC/Servidor)
Usado para ler dados da porta serial do Arduino e enviar para a nuvem ou banco de dados.
*   **Biblioteca:** `pySerial`

```python
import serial

# Configura a conexão serial
arduino = serial.Serial('COM3', 9600)

while True:
    data = arduino.readline().decode('utf-8').strip()
    print(f"Dados do Sensor: {data}")
```

### B. MicroPython (No Hardware)
Para placas mais potentes (como ESP32 ou Raspberry Pi Pico), o Python roda diretamente no microcontrolador.
*   **Vantagem:** Desenvolvimento rápido e prototipagem ágil.

---

## 4. Comparativo: C++ vs Python em IoT


| Característica | C++ (Arduino) | Python / MicroPython |
| :--- | :--- | :--- |
| **Performance** | Alta (Compilado) | Média (Interpretado) |
| **Consumo de Memória** | Baixíssimo | Alto |
| **Curva de Aprendizado** | Moderada | Fácil |
| **Uso Ideal** | Dispositivos de baixo poder | Gateways e análise de dados |

---

## 🛠️ Atividade Prática
1.  **C++:** Programar o Arduino para ler um sensor LDR (Luz).
2.  **Python:** Criar um script que recebe o valor do LDR via Serial e salva em um arquivo `.csv`.