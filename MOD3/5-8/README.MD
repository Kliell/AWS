## 📂 Resumo das Seções (5 a 8)

### Seção 5: Otimização de Custos do Amazon EC2
O EC2 é a base da computação, mas requer estratégia para não estourar o orçamento. O foco aqui é o **Right Sizing** (redimensionamento).

* **Modelos de Compra:**
    * **On-Demand:** Sem compromisso, pagamento por segundo.
    * **Instâncias Reservadas (RI):** Compromisso de 1-3 anos (descontos de até 75%).
    * **Savings Plans:** Flexibilidade em troca de um compromisso de gasto ($/hora).
    * **Instâncias Spot:** Instâncias ociosas da AWS com até 90% de desconto. Ótimas para workloads tolerantes a falhas.
* **Dica de Aluno:** Sempre monitorar o *AWS Compute Optimizer* para ver se não estamos pagando por CPU que não usamos.

### Seção 6: Serviços de Contêiner
Contêineres permitem consistência entre ambientes de dev e prod. Na AWS, temos opções robustas:

* **Amazon ECS:** Orquestrador de contêineres nativo e altamente escalável.
* **Amazon EKS:** Kubernetes gerenciado (padrão de mercado).
* **AWS Fargate:** O "Serverless para contêineres". Você não gerencia instâncias EC2; a AWS cuida da infraestrutura subjacente.

### Seção 7: Introdução ao AWS Lambda
Entrando no mundo **Serverless**. Aqui o foco é apenas o código.

* **Execução por Eventos:** O código roda em resposta a gatilhos (S3, DynamoDB, API Gateway).
* **Vantagens:** Escalabilidade automática e custo zero quando não está em execução.
* **Limitação:** Ideal para tarefas curtas (timeout de até 15 min).

### Seção 8: Introdução ao AWS Elastic Beanstalk
O caminho mais rápido para colocar uma aplicação web no ar.

* **PaaS (Plataforma como Serviço):** Você faz o upload do código (Node.js, Python, Java, etc.) e a AWS cuida do resto: Load Balancer, Auto Scaling e Provisionamento.
* **Controle:** Mesmo sendo automatizado, você mantém o controle total sobre as instâncias EC2 criadas.

## 💡 Reflexão de Estudante
Para um dev, a escolha depende do nível de controle vs. agilidade:
- **EC2:** Controle total (IaaS).
- **Beanstalk:** Agilidade no deploy (PaaS).
- **Lambda:** Foco total na lógica (FaaS).
- **Fargate:** O equilíbrio para microsserviços.
