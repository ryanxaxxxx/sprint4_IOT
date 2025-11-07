# 🚨 Projeto IoT – Moto Security System

Este projeto implementa um **sistema embarcado de monitoramento e alerta para motos**, utilizando **ESP 32** e diversos sensores/atuadores.
A lógica foi desenvolvida em **C++ (Wokwi)**, com dashboard para histórico de eventos e configuração do sistema.

O sistema exibe estados da moto em um **LCD 16x2 I2C**, controla **LEDs de status**,  registra dados ambientais via **DHT22**, e localização real das motos com latitude e longitude.
Foi pensado como um protótipo de **segurança IoT para motocicletas**.

---

Link para o vídeo:  

## 📦 Tecnologias e Componentes Utilizados

* **ESP 32**
* **4 LEDs + 4 resistores**
* **Botão de entrada**
* **LCD 16x2 com interface I2C (0x27)**
* **Sensor de temperatura e umidade DHT22**
* **Dashboard** para histórico persistente

---

## 📂 Estrutura do Projeto

```
/MotoSecurityIoT
 ├── sketch.ino         # Código-fonte principal
 ├── Json 
```

---

## 🚀 Funcionalidades Implementadas

* 📋 Alternância de estados a cada clique no botão:

  * **Moto Localizada**
  * **Moto OK**
  * **Moto liberada**
  * **em uso**

* ⏱️ **Pressão longa (>1s):** desliga todos os LEDs.

* 💾 **Dashboard:**

  * Histórico de até **20 registros** (temperatura, umidade, estado do sistema, LEDs, localização ).
  * Contador de boots do sistema.
  * Restauração do último estado após reinício.

* 🔍 **Monitor Serial:** impressão periódica de registros e histórico.

---

## ⚙️ Como Executar o Projeto

### 1. Montagem

Monte os componentes conforme descrito:

* LEDs nos pinos **2–5**
* Botão no pino **7** (com `INPUT_PULLUP`)
* DHT22 no pino **6**
* LCD 16x2 via I2C (endereço `0x27`)

### 2. Upload

1. Abra o `sketch.ino` no **Wokwi** ou **VS Code + PlatformIO**
2. Instale as bibliotecas necessárias (via *Library Manager*).
3. Compile e faça upload para o **ESP 32**.

### 3. Uso

* Pressione rapidamente o botão para alternar estados.
* Segure o botão >1s para desligar tudo e salvar histórico.
* Veja dados salvos no **Serial Monitor (9600 baud)**.

---

## 📊 Resultados Parciais

* ✅ Controle de estados funcionando com LEDs e LCD.
* ✅ Buzzer ativado no estado de alerta.
* ✅ Medição de temperatura/umidade e exibição no LCD.
* ✅ DAshboard (histórico e último estado).
* ✅ Localização da moto.

### Próximos Passos/ concluidos

* 🔗 Integração com módulo **ESP8266/ESP32** para envio dos dados via Wi-Fi.✅
* 📡 Dashboard web/mobile para monitoramento remoto.✅


---


## 👨‍💻 Autores:

Ryan Fernando Lucio da Silva - 555924
Lucas Henrique de Souza Santos - 558241
Mariana Roberti Neri - 556284

