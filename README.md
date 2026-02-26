# 💡 LED Piscante com ESP32

## 📌 Informações do Projeto

**Autora:** Isabelle dos Santos de Abreu  
**Turma:** DS3B  
**Disciplina:** Internet das Coisas (IoT)

---

## 📖 Descrição

Este projeto foi desenvolvido durante as aulas de Internet das Coisas (IoT) com o objetivo de aprofundar os conhecimentos práticos na utilização de protoboard e componentes eletrônicos.

A implementação foi realizada utilizando a **ESP32**, um microcontrolador de baixo custo que se destaca por integrar conectividade **Wi-Fi** e **Bluetooth**, além de apresentar maior capacidade de processamento em comparação a outras plataformas amplamente utilizadas no ensino.

O projeto consiste na refatoração de uma atividade desenvolvida anteriormente no segundo semestre, na disciplina de Arquitetura de Redes, na qual foi utilizada a plataforma Arduino. Nesta versão, a solução foi adaptada para a ESP32, explorando seus recursos avançados e ampliando a compreensão sobre sistemas embarcados e comunicação em IoT.

---

## 🎯 Objetivos

- Compreender o funcionamento da ESP32  
- Aprender a utilizar a protoboard corretamente  
- Realizar a montagem de circuitos eletrônicos básicos  
- Desenvolver lógica de programação para controle de GPIO  
- Aplicar conceitos introdutórios de sistemas embarcados  

---

## 🛠️ Tecnologias e Componentes Utilizados

### Hardware
- ESP32  
- Protoboard  
- LED  
- Resistor
- Jumpers  
- Cabo USB  

### Software
- Arduino IDE  
- Linguagem C/C++  
- Driver da ESP32 instalado na IDE  

---

## ⚙️ Funcionamento do Projeto

O sistema realiza o acionamento intermitente de um LED conectado a um dos pinos digitais da ESP32.

A lógica implementada:
1. Configura o pino do LED como saída.
2. Define o estado HIGH (ligado).
3. Aguarda um intervalo de tempo.
4. Define o estado LOW (desligado).
5. Repete o ciclo continuamente.

Esse comportamento caracteriza o efeito de **LED piscante**, amplamente utilizado como exemplo introdutório em sistemas embarcados.

---

## 🔌 Esquema de Ligação

- Terminal positivo do LED → Pino digital da ESP32  
- Terminal negativo do LED → Resistor → GND  

---

## 💻 Código Utilizado

```cpp
int ledPin = 21;

void setup()
{
  pinMode(ledPin, OUTPUT);
}

void loop()
{
  digitalWrite(ledPin, HIGH); //acende o led
  delay(2000); //por 2 segundos
  digitalWrite(ledPin, LOW); //apaga o led
  delay(2000); //por 2 segundos
}
