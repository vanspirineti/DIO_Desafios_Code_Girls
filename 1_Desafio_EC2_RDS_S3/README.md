# ✅ Primeiro Desafio - Descrever Uso do Amazon EC2 - RDS - EBS - Amazon S3 e AWS Lambda

Veremos abaixo a resolução do desafio "Computação na Nuvem com EC2" do Bootcamp Santander Code Girls 2025. Criei um diagrama de arquitetura com exemplo de um modelo de Loja de Departamentos utilizando serviços da **Amazon Web Services (AWS)**.  
Será demonstrado como os serviços da AWS trabalham de forma dinâmica e eficiente para melhor desempenho das necessidades de seus clientes.

---

## 🎯 Diagrama de arquitetura modelo da Loja de Departamentos


![Text](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/3e89dec79a69de6128428a0c6bdb3d91dabe7095/1_Desafio_EC2_RDS_S3/images/AWS_Diagrama_Loja_Dept.png)

---

## 🎲 Descrição detalhada da arquitetura: 

---

1️⃣ Os usuários conseguem acessar o servidor de Aplicação, conseguindo verificar informações da loja como pedidos e situação do estoque. Acessam também o WebServer da Loja de departamentos de forma indireta obviamente.

2️⃣ Servidores configurados no **Amazon EC2** ,serviço que fornece capacidade de computação escalável na nuvem.\
**Uso na loja:** Hospedar o site da loja, aplicações de gerenciamento de estoque e sistemas de ponto de venda (POS).\
**Benefícios:** Escalabilidade, flexibilidade e controle sobre a configuração do servidor.

3️⃣ Armazenamento de informações do SO e aplicativos no **Amazon EBS** , um serviço de armazenamento em bloco que fornece volumes persistentes para instâncias EC2.\
**Uso na loja:** Armazenar dados críticos, como informações de clientes, transações e inventário.\
**Benefícios:** Alta disponibilidade, backup e recuperação de dados, e desempenho consistente.Um serviço de armazenamento em bloco que fornece volumes persistentes para instâncias EC2.

4️⃣ Uso de um banco de dados para a Aplicação usando **Amazon RDS** , um serviço que facilita a configuração, operação e escalabilidade de bancos de dados relacionais na nuvem.\
**Uso na loja:** Gerenciar dados de clientes, pedidos e inventário em um banco de dados relacional.\
**Benefícios:** Redução da complexidade de gerenciamento de banco de dados, backups automáticos e escalabilidade.

5️⃣ Uso do **Amazon S3** para armazenamento de imagens e scripts do WebServer, serviço de armazenamento de objetos que oferece escalabilidade, disponibilidade e segurança.\
**Uso na loja:** Armazenar imagens de produtos, documentos e backups de dados.\
**Benefícios:** Acesso fácil e rápido aos dados, além de integração com outros serviços da AWS.

6️⃣ Temos o uso do **AWS Lambda** aplicado de diversas formas em nossa arquitetura \
 
 
 **Exemplo 1:** Processamento de Pedidos em Tempo Real: \
        - Gatilho: Um novo pedido é registrado no RDS (banco de dados de pedidos).\
        - Lambda: Uma função Lambda é acionada para processar o pedido. Ela pode:\
        - Atualizar o estoque no RDS.\
        - Enviar um e-mail de confirmação ao cliente (integrando com serviços como SES).\
        - Notificar o sistema de logística.\
       *Serviços Envolvidos:* RDS, Lambda, S3 (para logs, se necessário).
       
 **Exemplo 2:** Gerenciamento de Imagens de Produtos:\
        - Gatilho: Uma nova imagem de produto é carregada para um bucket específico no S3.\
        - Lambda: Uma função Lambda é acionada para:\
        - Redimensionar a imagem para diferentes resoluções (miniaturas, visualização principal).\
        - Otimizar a imagem para web.\
        - Salvar as versões processadas de volta no S3.\
       *Serviços Envolvidos:* S3, Lambda.
    
 **Exemplo 3:** Processamento de Eventos do Site:\
        - Gatilho: Interações do usuário no site hospedado no EC2 (ex: adições ao carrinho, visualizações de produtos).\
        - Lambda: Funções Lambda podem ser usadas para coletar dados de eventos, realizar análises em tempo real ou acionar                      notificações. \
        *Serviços Envolvidos:* EC2, Lambda, S3 (para armazenamento de dados de eventos).

---


## 💭 Resumo Geral do Fluxo

✔ EC2 (Site/Apps) -> Interage com RDS (Dados) e S3 (Imagens).\
✔ RDS (Dados) -> Aciona Lambda para processamento de pedidos e atualizações.\
✔ S3 (Imagens) -> Aciona Lambda para otimização e redimensionamento.\
✔ Lambda -> Pode escrever logs em S3, atualizar RDS, ou interagir com outros serviços AWS.\
✔ EBS -> Usado pelo EC2 para armazenamento persistente do sistema operacional e dados locais, com backups gerenciados por Lambda agendado.

---
