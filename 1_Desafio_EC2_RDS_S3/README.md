# ✅ Primeiro Desafio - Descrever Uso do Amazon EC2 - RDS - EBS - Amazon S3 e AWS Lambda

Veremos abaixo a resolução do desafio "Computação na Nuvem com EC2" do Bootcamp Santander Code Girls 2025. Criei um diagrama de arquitetura com exemplo de um modelo de Loja de Departamentos utilizando serviços da **Amazon Web Services (AWS)**.  
Será demonstrado como os serviços da AWS trabalham de forma dinâmica e eficiente para melhor desempenho das necessidades de seus clientes.

---

## 🔷 Diagrama de arquitetura modelo da Loja de Departamentos 
![alt text](./images/loja_departamentos_EC2.jpg)

## ⏭ Descrição detalhada da arquitetura:

1 - Os usuários conseguem acessar o servidor de Aplicação, conseguindo verificar informações da loja como pedidos e situação do estoque. Acessam também o WebServer da Loja de departamentos de forma indireta obviamente.

2. Servidores configurados no *Amazon EC2* ,serviço que fornece capacidade de computação escalável na nuvem.
*Uso na loja:* Hospedar o site da loja, aplicações de gerenciamento de estoque e sistemas de ponto de venda (POS).
*Benefícios:* Escalabilidade, flexibilidade e controle sobre a configuração do servidor.

3. Armazenamento de informações do SO e aplicativos no *Amazon EBS* , um serviço de armazenamento em bloco que fornece volumes persistentes para instâncias EC2.
*Uso na loja:* Armazenar dados críticos, como informações de clientes, transações e inventário.
*Benefícios:* Alta disponibilidade, backup e recuperação de dados, e desempenho consistente.Um serviço de armazenamento em bloco que fornece volumes persistentes para instâncias EC2.



---

## 📌 Resumo Visual do Fluxo

1. Usuário acessa o blog.  
2. Conteúdo dinâmico vem do **EC2 + RDS**.  
3. Conteúdo estático vem direto do **S3**.  
4. Uploads no **S3** disparam **Lambda** para processamento.  

---
