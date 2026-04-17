# ☁️ AWS Academy: Cloud Foundations - Resumo de Estudo

Este repositório contém anotações estratégicas das seções iniciais do curso AWS Academy, focadas em arquitetura, infraestrutura global e modelos de adoção de nuvem.

## 📌 1. Conceitos Fundamentais de Nuvem
A computação em nuvem é a entrega de recursos de TI sob demanda via Internet com uma política de **pagamento conforme o uso**.

* **Propriedade:** O provedor (AWS) detém e mantém o hardware físico. O usuário aluga a capacidade.
* **Capacidade:** Elimina a necessidade de "adivinhar" a infraestrutura necessária (Scalability).

## 🚀 2. As 6 Vantagens da Computação em Nuvem
Para fins de certificação, entenda estes pilares:

1.  **Trade Capital Expense for Variable Expense:** Troca de CAPEX (investimento pesado em hardware) por OPEX (despesas operacionais baseadas no uso).
2.  **Economies of Scale:** Redução de custos unitários devido ao volume massivo de clientes da AWS.
3.  **Stop Guessing Capacity:** Uso de *Auto Scaling* para ajustar recursos conforme a demanda real.
4.  **Increase Speed and Agility:** Recursos disponíveis para desenvolvedores em minutos.
5.  **Stop Spending Money on Data Centers:** Foco no código e no cliente, não na manutenção física (energia, refrigeração).
6.  **Go Global in Minutes:** Deploy mundial rápido usando a infraestrutura global da AWS.

## 🏗️ 3. Infraestrutura Global da AWS

| Componente | Descrição | Importância para o Dev |
| :--- | :--- | :--- |
| **Região (Region)** | Local físico geográfico (ex: `sa-east-1`). | Latência, soberania de dados e custos. |
| **Zona de Disponibilidade (AZ)** | Um ou mais data centers isolados dentro de uma região. | Alta Disponibilidade (Multi-AZ). |
| **Edge Locations** | Pontos de presença para cache de conteúdo. | Usado pelo CloudFront para reduzir latência. |

> [!IMPORTANT]
> **Alta Disponibilidade:** Sempre provisione recursos em **várias (várias)** Zonas de Disponibilidade para evitar pontos únicos de falha.

## 📂 4. Cloud Adoption Framework (AWS CAF)
Estrutura para organizar a jornada de migração para a nuvem através de 6 perspectivas:

### Perspectivas de Negócio (Foco em Pessoas/Processos)
* **Negócios:** Foco em ROI e valor comercial.
* **Pessoas:** Gestão de mudanças e treinamento.
* **Governança:** Gerenciamento de portfólio e conformidade.

### Perspectivas Técnicas (Foco em Tecnologia/Plataforma)
* **Plataforma:** Design de arquitetura e padrões de nuvem.
* **Segurança:** Proteção de dados e conformidade.
* **Operações:** Monitoramento e manutenção do ambiente.

## 💰 5. Precificação e Gerenciamento Financeiro
* **Instâncias Reservadas:** Desconto baseado no compromisso de 1 ou 3 anos.
* **Transferência de Dados:** Entrada (*Inbound*) é **gratuita**; Saída (*Outbound*) para a internet é **paga**.
* **AWS Organizations:** Centraliza o faturamento e permite o uso de **SCPs** (Service Control Policies) para governança.
* **AWS Pricing Calculator:** Ferramenta para criar **estimativas** de custo antes do deploy.

---
**Nota:** Este guia foi elaborado como material de apoio para a certificação *AWS Certified Cloud Practitioner*.