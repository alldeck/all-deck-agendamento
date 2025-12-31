# ALL DECK - Sistema de Agendamento de Churrasqueira 🥩🍺

![ALL DECK Logo](caminho/para/seu_logo.jpg)

> **Buteco Raiz em Itajaí/SC**. O ponto de encontro perfeito com churrasqueira à disposição dos clientes.

## 📋 Sobre o Projeto

Este projeto consiste em uma aplicação web (PWA) para gerenciar o agendamento da churrasqueira do **ALL DECK**. O objetivo é facilitar a reserva para os clientes e aumentar a frequência de uso do espaço.

O cliente traz a carne, e o ALL DECK fornece todo o resto (Lenha, Carvão, Temperos e Serviço) por uma taxa fixa por pessoa.

### 📍 Localização e Contato
* **Endereço:** R. Fritz Schneider, 25, Itajaí - SC
* **WhatsApp:** (47) 9 9985-7365
* **Instagram:** [@all.deck](https://www.instagram.com/all.deck/)

---

## 🚀 Funcionalidades

* **Calendário de Disponibilidade:** Visualização em tempo real dos dias livres.
* **Agendamento Inteligente:** O sistema bloqueia datas fora do horário de funcionamento (Terça a Sexta, 17:30 - 22:30).
* **Cálculo Automático:** Estimativa de valor baseada no número de participantes (R$ 25,00/pessoa).
* **Feedback Visual:**
    * Mensagem de sucesso: *"Confirmação de envio"*
    * Status do pedido: *"Pedido de reserva aguardando confirmação"*

## 🛠️ Tecnologias Utilizadas

* **Front-end:** React.js / Vue.js (Sugerido)
* **Back-end / Database:** Google Firebase (Firestore & Cloud Functions)
* **Hospedagem:** Firebase Hosting

## 🗂️ Estrutura do Banco de Dados (Firestore)

O banco de dados segue uma estrutura NoSQL orientada a documentos:

### Collection: `agendamentos`
| Campo | Tipo | Descrição |
| :--- | :--- | :--- |
| `cliente.nome` | String | Nome do solicitante |
| `cliente.whatsapp` | String | Contato para confirmação |
| `data_reserva` | Timestamp | Data e hora do churrasco |
| `qtd_pessoas` | Number | Número de participantes |
| `status` | String | `pendente`, `confirmado`, `cancelado` |

---

## 📸 Identidade Visual e Regras de Negócio

1.  **Cores da Marca:** Utilizar as cores do logo (Laranja, Verde, Azul e Amarelo) para destacar botões e avisos.
2.  **Horários:** O sistema só permite agendamentos entre Terça e Sexta-feira.
3.  **Fluxo de Aprovação:**
    1.  Cliente solicita a data.
    2.  Sistema salva como `pendente`.
    3.  Admin recebe notificação (via App ou WhatsApp API).
    4.  Admin aprova -> Cliente recebe confirmação.

## 📦 Como Rodar este Projeto

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/seu-usuario/all-deck-agendamento.git](https://github.com/seu-usuario/all-deck-agendamento.git)
    ```
2.  Instale as dependências:
    ```bash
    npm install
    ```
3.  Configure as chaves do Firebase no arquivo `.env`.
4.  Rode o servidor local:
    ```bash
    npm run dev
    ```

---
Desenvolvido para **ALL DECK** ® - Todos os direitos reservados.
