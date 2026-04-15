# AWS Lab: Introdução ao AWS Identity and Access Management (IAM)

Este repositório contém a documentação e os detalhes do laboratório prático sobre **AWS IAM**, focado na gestão centralizada de utilizadores, grupos e permissões.

## 📝 Descrição do Laboratório
O **AWS Identity and Access Management (IAM)** é um serviço web que permite aos clientes da AWS gerir utilizadores e as suas permissões de forma segura. Com o IAM, é possível controlar quem pode autenticar-se (iniciar sessão) e quem tem autorização (permissões) para utilizar os recursos.

## 🎯 Objetivos de Aprendizagem
* Explorar utilizadores e grupos IAM pré-criados.
* Inspecionar políticas IAM aplicadas a grupos.
* Implementar um cenário real: adicionar utilizadores a grupos com capacidades específicas.
* Localizar e utilizar o URL de início de sessão do IAM.
* Testar na prática os efeitos das políticas no acesso aos serviços.

---

## 🏢 Cenário de Negócio
Uma empresa em crescimento utiliza instâncias Amazon EC2 e armazenamento Amazon S3. Foram contratados três novos funcionários com funções distintas, exigindo a configuração de permissões baseada no princípio do **menor privilégio**:

| Utilizador | Grupo Destino | Permissões |
| :--- | :--- | :--- |
| **user-1** | `S3-Support` | Acesso de leitura (Read-Only) ao Amazon S3. |
| **user-2** | `EC2-Support` | Acesso de leitura (Read-Only) ao Amazon EC2. |
| **user-3** | `EC2-Admin` | Visualizar, Iniciar e Parar instâncias Amazon EC2. |

---

## 🚀 Passo a Passo da Execução

### 1. Auditoria de Recursos
No início do laboratório, foram identificados:
* **Utilizadores:** `user-1`, `user-2`, `user-3` (inicialmente sem permissões).
* **Grupos e Políticas:**
    * `EC2-Support`: Associado à Managed Policy `AmazonEC2ReadOnlyAccess`.
    * `S3-Support`: Associado à Managed Policy `AmazonS3ReadOnlyAccess`.
    * `EC2-Admin`: Associado a uma **Inline Policy** que permite `DescribeInstances`, `StartInstances` e `StopInstances`.

### 2. Atribuição de Permissões
Os utilizadores foram adicionados aos grupos para herdarem as permissões necessárias:
1.  Adicionado **user-1** ao grupo `S3-Support`.
2.  Adicionado **user-2** ao grupo `EC2-Support`.
3.  Adicionado **user-3** ao grupo `EC2-Admin`.

### 3. Testes de Validação (Acesso Multi-Utilizador)
Através de sessões em janelas anónimas, validou-se o acesso de cada perfil:

* **Teste user-1 (S3 Support):** Conseguiu visualizar os buckets S3, mas recebeu erro `Not Authorized` ao tentar aceder ao EC2.
* **Teste user-2 (EC2 Support):** Conseguiu listar instâncias EC2, mas recebeu erro de autorização ao tentar parar a instância `LabHost`. Não teve acesso ao S3.
* **Teste user-3 (EC2 Admin):** Conseguiu visualizar a instância e teve sucesso ao executar o comando **Stop Instance**, validando as permissões administrativas.

---

## 🛠️ Estrutura de uma Política IAM (JSON)
Durante o lab, analisámos que as políticas seguem esta estrutura base:
* **Effect:** Define se permite (`Allow`) ou nega (`Deny`).
* **Action:** Especifica a chamada de API (ex: `s3:Get*`, `ec2:StopInstances`).
* **Resource:** Define a que recursos a regra se aplica (ex: `*` para todos os recursos).

---

## ✅ Conclusão
Este laboratório demonstrou como o IAM permite a governação segura de um ambiente AWS. O uso de grupos facilita a gestão de permissões à medida que a organização cresce, garantindo que cada colaborador aceda apenas ao que é estritamente necessário para a sua função.

---
> **Nota:** Este laboratório faz parte do currículo oficial de aprendizagem da AWS.