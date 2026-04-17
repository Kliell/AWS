# 🌐 AWS Academy: Cloud Foundations - Módulo 3: Infraestrutura e Serviços

Este módulo detalha a espinha dorsal física da AWS e categoriza os principais serviços oferecidos para construção de aplicações escaláveis.

## 🏗️ 1. Infraestrutura Global da AWS
A infraestrutura é organizada de forma hierárquica para garantir redundância e baixa latência.

* **Regiões (Regions):** Áreas geográficas separadas no mundo que hospedam **duas ou mais** Zonas de Disponibilidade.
    * **Escolha da Região:** Baseada em conformidade legal, proximidade dos usuários (para **diminuir a latência**) e variação de custos.
* **Zonas de Disponibilidade (AZs):** Compostas por um ou mais datacenters discretos com energia e rede redundantes.
    * **Links de Baixa Latência:** As AZs dentro de uma região são conectadas por fibras ópticas de alta velocidade.
    * **Isolamento:** Cada AZ é projetada para isolamento de falhas. **Um datacenter nunca é compartilhado entre AZs diferentes**.
* **Pontos de Presença (Edge Locations):** Locais que hospedam o Amazon CloudFront para entregar conteúdo com menor latência globalmente.

## 🛠️ 2. Categorias de Serviços da AWS
A AWS oferece centenas de serviços, mas eles são agrupados em categorias fundamentais para facilitar o design da arquitetura:

| Categoria | Descrição / Exemplos |
| :--- | :--- |
| **Computação** | Processamento de dados e execução de código (ex: EC2, Lambda). |
| **Armazenamento** | Retenção de dados persistentes ou temporários (ex: S3, EBS). |
| **Bancos de Dados** | Armazenamento estruturado e consultas (ex: RDS, DynamoDB). |
| **Redes** | Isolamento e conectividade (ex: VPC, Route 53). |

## 📐 3. Conceitos de Arquitetura Resiliente
Para um programador, construir na nuvem exige pensar em falhas desde o primeiro dia:

* **Tolerância a Falhas (Fault Tolerance):** Capacidade da infraestrutura de continuar operando via redundância de componentes integrada.
* **Elasticidade e Escalabilidade:** Capacidade de os recursos se ajustarem dinamicamente conforme o aumento ou diminuição da demanda.
* **Multi-AZ:** É altamente recomendado provisionar recursos de computação em **várias** zonas de disponibilidade para evitar interrupções caso uma AZ falhe.

---

### 🔥 Notas para Fixação (Módulo 3):
* **Verdadeiro:** Redes, armazenamento, computação e bancos de dados são categorias base da AWS.
* **Verdadeiro:** AZs em uma mesma região usam links privados de alta velocidade.
* **Falso:** Um datacenter **não** pode pertencer a mais de uma Zona de Disponibilidade simultaneamente.
* **Ação Recomendada:** Provisionar em **várias** AZs para máxima disponibilidade.

---
> [!TIP]
> **Dica de Infra:** Ao escolher uma região, lembre-se que nem todos os serviços estão disponíveis em todas as regiões simultaneamente. Verifique sempre a tabela de disponibilidade regional.