# 🦯 Bastão Inteligente: Sistema Embarcado de Auxílio à Mobilidade

Este projeto consiste no desenvolvimento de um dispositivo assistivo para deficientes visuais, utilizando a fusão de sensores ultrassônicos e laser para detecção de obstáculos em tempo real. Desenvolvido como parte do Trabalho Interdisciplinar da **PUC Minas**.

---

## 🌍 Impacto Social e ODS (Agenda 2030)
O projeto foi concebido sob as diretrizes das **Objetivos de Desenvolvimento Sustentável (2025)**, focando em:
* **ODS 3 (Saúde e Bem-Estar):** Redução de acidentes e promoção da segurança física do usuário.
* **ODS 9 (Indústria, Inovação e Infraestrutura):** Fomento à tecnologia assistiva nacional com hardware de baixo custo.
* **ODS 10 (Redução das Desigualdades):** Promoção da autonomia e inclusão social de pessoas com deficiência visual.

---

## 🛠️ Especificações Técnicas

### Hardware
* **Microcontrolador:** ESP-32 (Arquitetura 32 bits).
* **Sensores de Distância:** * 1x HC-SR04 (Ultrassônico) para detecção frontal de longo alcance.
    * 2x VL53L0X (Laser Time-of-Flight) para cobertura lateral e precisão.
* **Atuadores:** * 2x Motores Vibracall 1027 (Feedback tátil).
    * 1x Buzzer (Feedback sonoro variável).
      
---

## 📋 Pinagem (Mapeamento de Hardware)

| Componente | Pino ESP32 | Descrição |
| :--- | :--- | :--- |
| **HC-SR04 TRIG** | 27 | Gatilho Ultrassônico |
| **HC-SR04 ECHO** | 14 | Eco Ultrassônico |
| **XSHUT ESQ** | 17 | Reset/Endereçamento Laser Esq |
| **XSHUT DIR** | 16 | Reset/Endereçamento Laser Dir |
| **VIBRACALL ESQ**| 25 | Motor de Vibração Esquerdo |
| **VIBRACALL DIR**| 26 | Motor de Vibração Direito |
| **BUZZER** | 32 | Alerta Sonoro |

---

## 🚀 Lógica de Alerta

* **Obstáculos Laterais:** Ativam os motores de vibração correspondentes se a distância for $\leq 300\text{ mm}$.
* **Obstáculos Frontais:** O buzzer emite bips cuja frequência aumenta conforme o objeto se aproxima (limite de 1 metro). A modulação é feita via função `map()` no código.

---

## 👥 Integrantes
* **Alunas:** Ana Késia e Gabriela Adriana.
* **Orientador:** Prof. Mário Buratto.
* **Instituição:** Pontifícia Universidade Católica de Minas Gerais (PUC Minas).
* **Ano:** 2025
