# 💰 AWS Academy: Cloud Foundations - Módulo 2: Economia e Faturamento

Este módulo foca em como a AWS cobra pelos serviços, como estimar custos e as ferramentas disponíveis para governança financeira de múltiplas contas.

## 💳 1. Fundamentos de Precificação
A AWS segue o modelo **Pay-as-you-go** (Pague pelo que usar). Os três principais geradores de custo (Cost Drivers) são:

1.  **Computação:** Cobrança por segundo ou hora.
2.  **Armazenamento:** Cobrança por GB/mês.
3.  **Transferência de Dados:** * **Inbound (Entrada):** Gratuita na maioria dos casos.
    * **Outbound (Saída):** Cobrada por GB (dados saindo da AWS para a internet).

## 📉 2. TCO (Total Cost of Ownership)
O TCO é a métrica usada para comparar o custo de manter uma infraestrutura **On-premises** vs. **Nuvem AWS**. 
* **On-premises:** Custos altos de CAPEX (servidores, imóveis, eletricidade, pessoal de manutenção física).
* **Nuvem:** Transforma custos fixos em custos variáveis (OPEX) e elimina gastos com a "manutenção pesada" do data center.

## 🏢 3. AWS Organizations
Ferramenta de gerenciamento de conta que permite consolidar várias contas da AWS em uma estrutura centralizada.

* **Consolidated Billing:** Agrega o consumo de todas as contas para atingir níveis de desconto por volume mais rápido.
* **SCPs (Service Control Policies):** Políticas que definem os limites de permissão para o que os usuários (inclusive o root) podem fazer nas contas membro.
* **Hierarquia:** Organização de contas em **UOs (Unidades Organizacionais)**.

## 🛠️ 4. Ferramentas de Gestão Financeira

| Ferramenta | Objetivo | Quando usar? |
| :--- | :--- | :--- |
| **AWS Pricing Calculator** | **Estimativa** | Antes de implantar a solução. |
| **AWS Budgets** | **Alertas** | Para receber e-mails quando o gasto real ou previsto exceder um limite. |
| **AWS Cost Explorer** | **Análise** | Para visualizar gráficos e tendências de gastos passados. |
| **AWS Cost and Usage Report** | **Detalhamento** | Para obter o conjunto de dados de faturamento mais granular possível. |

## 🆘 5. Planos de Suporte AWS
Existem 4 níveis de suporte, dependendo da criticidade do negócio:

1.  **Basic:** Gratuito (Acesso a fóruns, documentação e suporte para faturamento).
2.  **Developer:** Recomendado para ambientes de teste.
3.  **Business:** Suporte 24x7 por e-mail, chat e telefone (para produção).
4.  **Enterprise:** Inclui um **TAM (Technical Account Manager)** dedicado.

## 💎 6. Serviços Gratuitos (Core Services)
Alguns serviços não possuem custo por si só, mas você paga pelos recursos que eles criam:
* **IAM** (Identity and Access Management)
* **Amazon VPC** (Rede Virtual)
* **AWS CloudFormation** (Infraestrutura como Código)
* **AWS Organizations**
* **AWS Beanstalk**

---
> [!TIP]
> **Dica para a prova:** Lembre-se que as **Instâncias Reservadas** oferecem desconto pelo compromisso de tempo (1 ou 3 anos), e não necessariamente exigem pagamento antecipado (opção *No Upfront*).