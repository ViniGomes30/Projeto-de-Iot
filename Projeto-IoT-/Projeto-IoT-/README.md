# Projeto IoT: Monitoramento Energético

**Participantes**  
- Diego Estevão Lopes de Queiroz  
- Erik Salomão Almeida  
- Iago Leite Chain   
- Vinicius Gutierrez Gomes

---

## Visão Geral

Este projeto implementa um sistema de monitoramento de consumo de energia elétrica utilizando tecnologias de IoT.

O ESP32 realiza a leitura de corrente por meio do sensor SCT-013-030 e envia os dados via MQTT para o Node-RED, que processa as informações e as armazena no InfluxDB. Os dados são visualizados em tempo real através de dashboards no Grafana e, quando há consumo elevado, o sistema envia alertas automáticos via WhatsApp usando a API CallMeBot. O projeto busca promover o uso consciente de energia, alinhado aos objetivos de sustentabilidade, com foco na eficiência energética e na redução do desperdício.

---

## Tecnologias Utilizadas

- **ESP32** (C++ / Arduino)  
- **MQTT** (Mosquitto ou outro broker compatível)  
- **Node-RED** (JavaScript / JSON para fluxos)  
- **InfluxDB 2.x**  
- **Grafana**  
- **API CallMeBot** (WhatsApp)

## Como Executar

Para testar o projeto sem hardware físico, utilize o simulador Wokwi:

### Rodar o Código no Wokwi

1. Acesse [Wokwi](https://wokwi.com/) e importe o sketch `firmware/monitoramento.ino`.  
2. Configure o ESP32 virtualmente, incluindo o sensor SCT-013-030 simulado.  
3. Inicie a simulação e verifique a publicação MQTT no console do Wokwi (tópico `iot/energia/consumo`).  

### Implementar o Node-RED

1. Instale e inicie o Node-RED localmente:
   ```bash
   npm install -g --unsafe-perm node-red
   node-red
