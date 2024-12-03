# Microcontrolador Universal de Controles para o Console Nintendo Switch

Este projeto tem como objetivo criar um dispositivo baseado no microcontrolador ESP32 que funcione como um intermediário universal entre diferentes controles Bluetooth e o console Nintendo Switch. O foco principal é permitir que controles de outros dispositivos, como o DualShock 4 (PS4), sejam usados no Switch, simulando perfeitamente o comportamento de um Controle Nintendo Switch Pro.

## Estrutura do Projeto

O projeto é dividido em etapas fundamentais:

1. **Microcontrolador**  
   O ESP32 foi escolhido por sua versatilidade e suporte nativo a Bluetooth, tornando-o ideal para a tarefa. Embora uma versão com suporte a USB HID pudesse ser mais eficiente, este projeto se concentra exclusivamente em conexões Bluetooth para simplificar e intensificar o desafio técnico.

2. **Conexões e Tradução de Comandos**  
   - **Primeira conexão Bluetooth**: O ESP32 atua como receptor, conectando-se ao controle original, como o DualShock 4.  
   - **Tradução de comandos**: Os sinais recebidos do controle são interpretados e traduzidos para o formato compatível com o protocolo do Controle Nintendo Switch Pro.  
   - **Segunda conexão Bluetooth**: O ESP32 emula um Controle Nintendo Switch Pro, conectando-se ao console como se fosse um controle oficial.  

## Fluxo de Funcionamento

1. **Conexão Inicial**: O controle original (por exemplo, PS4 DualShock) conecta-se ao ESP32 via Bluetooth.  
2. **Processamento**: O ESP32 mapeia e converte os comandos recebidos no padrão do Switch.  
3. **Emulação**: O ESP32 estabelece uma segunda conexão Bluetooth com o Nintendo Switch, comportando-se como um controle oficial Pro.

---

# Diagrama...

Primeira conexão de Bluetooth: PS4Controller -> ESP32 (Sucess) <br>
Tradução dos comandos: PS4Controller -> Controle Nintendo Switch Pro (...) <br>
Segunda conexão Bluetooh: ESP32 como um Controle Nintendo Switch Pro -> Nintendo Switch
