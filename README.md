# 💡 Monitoramento Residencial de Consumo de Energia com IoT (ODS 7)

[![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)](link_para_o_artigo_ou_video)
[![Tecnologias](https://img.shields.io/badge/Tecnologias-IoT%20%7C%20MQTT%20%7C%20Grafana-blue)](estrutura_do_projeto)
[![Alinhamento](https://img.shields.io/badge/ODS-7%20(Eficiência%20Energética)-yellowgreen)](https://brasil.un.org/pt-br/sdgs/7)

Este projeto implementa um sistema de **Monitoramento de Consumo de Energia Elétrica** utilizando a Internet das Coisas (IoT), com o objetivo de promover o **uso consciente** e auxiliar residências e empresas na adoção de práticas mais sustentáveis.

---

## 🎯 Contexto e Motivação

O projeto está totalmente alinhado com o **Objetivo de Desenvolvimento Sustentável (ODS) 7 da ONU** – *Energia Acessível e Limpa* –, que foca em dobrar a taxa global de melhoria da eficiência energética até 2030.

### ⚠️ O Problema da Energia no Brasil

| Motivação Principal | Dados Chave do Artigo |
| :--- | :--- |
| **Combate ao Desperdício** | O Brasil desperdiça cerca de **43 TWh por ano**, o equivalente ao consumo de 20 milhões de residências. |
| **Mitigação Climática** | O aumento do uso de ar-condicionado (devido ao aquecimento global) gera mais consumo, criando um ciclo vicioso (*retroalimentação positiva*). |
| **Objetivo** | Desenvolver uma solução de baixo custo para fornecer dados em tempo real, incentivando a **redução do desperdício** e promovendo **economia financeira**. |

---

## ⚙️ Arquitetura e Fluxo de Dados

O sistema foi concebido como uma solução modular, capaz de monitorar, processar e alertar o usuário sobre o consumo elétrico em tempo real.

### 📊 Componentes e Funcionamento

| Etapa | Componentes Principais | Função |
| :--- | :--- | :--- |
| **1. Sensoriamento** | **ESP32** + Sensor **SCT-013-030** | Realiza a leitura da corrente elétrica e envia os dados. |
| **2. Comunicação** | Protocolo **MQTT** (Broker Mosquitto) | Envio de dados leve e eficiente do dispositivo para o sistema central. |
| **3. Processamento** | **Node-RED** | Trata os dados recebidos via MQTT e os direciona para o armazenamento e alertas. |
| **4. Armazenamento** | **InfluxDB 2.x** | Banco de dados otimizado para séries temporais (histórico de consumo). |
| **5. Visualização** | **Grafana** | Criação de Dashboards interativos (padrão diário, partição por dispositivo, comparativo mensal). |
| **6. Alertas** | **API CallMeBot** (WhatsApp) | Dispara alertas automatizados e sugestões de consumo consciente em tempo real. |

---

## 💻 Tecnologias Utilizadas

| Categoria | Tecnologia | Versão (Se aplicável) |
| :--- | :--- | :--- |
| **Firmware** | ESP32 | C++ / Arduino |
| **Protocolo** | MQTT | Mosquitto (ou broker compatível) |
| **Flow Editor** | Node-RED | JavaScript / JSON |
| **Database** | InfluxDB | 2.x |
| **Visualização** | Grafana | - |
| **Comunicação** | API CallMeBot | WhatsApp |

---

## ✅ Resultados e Conclusões

O projeto demonstrou a viabilidade de uma solução de monitoramento de energia de **baixo custo, modular e confiável**, capaz de impactar diretamente na economia de energia e detecção de falhas.

### ✨ Vantagens do Projeto
* **Monitoramento em Tempo Real** e análise histórica detalhada.
* **Custo Acessível** dos componentes (acessibilidade à solução).
* **Sistema Modular** e escalável, pronto para receber mais sensores (tensão, temperatura).
* Potencial para **Integração com Automação Residencial**.

---

## 👥 Contribuições

**Universidade Presbiteriana Mackenzie (UPM)**

* Diego Estevão Lopes de Queiroz
* Erik Salomão Almeida
* Iago Leite Chain
* Vinícius Gutierrez Gomes
* Wallace Rodrigues de Santana (Professor/Orientador)

## 📎 Links de Apoio e Referências
* **Link do Vídeo Demonstrativo:** [https://youtu.be/cs6IxYoTQsk](https://youtu.be/cs6IxYoTQsk)
* **Link do Artigo Científico Completo:** [https://docs.google.com/document/d/1HQKtHN72CtHaNvR1a_5E-f9LxjKznq807X5FiDnqqSU/edit?usp=sharing](https://docs.google.com/document/d/1HQKtHN72CtHaNvR1a_5E-f9LxjKznq807X5FiDnqqSU/edit?usp=sharing)
