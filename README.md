# Projeto: Comunicação Serial e Controle de LEDs com RP2040

## 📌 Descrição
Este projeto tem como objetivo a implementação de comunicação serial no **RP2040** utilizando a placa **BitDogLab**, explorando os protocolos **UART** e **I2C**. O sistema permite interação via **Serial Monitor**, controle de **LEDs WS2812** e **LED RGB**, além do uso de **botões físicos** com tratamento de **interrupções (IRQ) e debounce**.

## 🎯 Funcionalidades
- Exibição de caracteres digitados no **Serial Monitor** no **display SSD1306**.
- Exibição de símbolos correspondentes a números (0-9) na **matriz de LEDs WS2812**.
- Controle do **LED RGB** por meio de **botões físicos**:
  - **Botão A (GPIO 5)** alterna o estado do **LED verde**.
  - **Botão B (GPIO 6)** alterna o estado do **LED azul**.
- Mensagens informativas sobre o estado dos LEDs são enviadas para:
  - **Display SSD1306**.
  - **Serial Monitor** via UART.

## 🛠 Requisitos
### Hardware
- Placa **BitDogLab (RP2040)**
- **Matriz de LEDs WS2812 (5x5)** (GPIO 7)
- **LED RGB** (GPIOs 11, 12 e 13)
- **Botão A** (GPIO 5)
- **Botão B** (GPIO 6)
- **Display SSD1306 via I2C** (GPIO 14 e 15)

### Software
- **SDK do Raspberry Pi Pico**
- **CMake** e **Ninja**
- **Editor de Código VS Code**
- **Ferramentas de build do RP2040**

## 🚀 Como Executar

### **1️⃣ Clonar o Repositório**
```bash
git clone https://github.com/Anamacario/led-project.git
cd led-project
```

### **2️⃣ Compilar e Carregar no Raspberry Pi Pico**
- Conecte a placa **BitDogLab** ao computador.
- Compile o código e copie o arquivo `.uf2` para a unidade do Pico.

### **3️⃣ Testar o Projeto**
- **Abrir o Serial Monitor** e enviar caracteres.
- **Verificar a exibição no display SSD1306**.
- **Pressionar os botões físicos** para testar a alternância dos LEDs RGB.

## ⚙ Implementação Técnica
- **Uso de Interrupções (IRQ)**: Os botões são gerenciados por interrupções para evitar polling constante.
- **Debounce via Software**: Para garantir leituras confiáveis dos botões.
- **Controle de LEDs**: Utiliza a biblioteca para manipular WS2812 e LED RGB.
- **Protocolo I2C**: Comunicação entre o RP2040 e o display SSD1306.
- **Protocolo UART**: Comunicação entre o RP2040 e o computador via Serial Monitor.

## 🔍 Testes Realizados
✅ Digitação de caracteres no Serial Monitor e exibição correta no display SSD1306.  
✅ Exibição de números com símbolos correspondentes na matriz WS2812.  
✅ Alternância dos LEDs RGB ao pressionar os botões.  
✅ Saída correta de mensagens no Serial Monitor via UART.  
✅ Testes de estabilidade com debounce ativo nos botões.  

## 🎥 Entrega
- **Código-fonte**: Disponibilizado em repositório.
- **Vídeo de demonstração** 
- Click [AQUI](https://drive.google.com/file/d/1JZNorVrXtVoAesfkzNKsN-8GPesO7b2g/view?usp=sharing) para acessar o link do vídeo de apresentação.


