# ✅ Terceiro Desafio - Criando uma Stack no AWS Cloud Formation

_Detalharemos abaixo a resolução do desafio 3 do Bootcamp Santander Code Girls 2025._ 
_Será explorado alguns conceitos do uso do Cloud Formation_

---

## 🎯 Conceitos de Uso do AWS Cloud Formation:

_O AWS CloudFormation é um serviço que permite modelar, provisionar e gerenciar recursos da AWS e de terceiros utilizando o conceito de Infraestrutura como Código (IaC)._ 

_🥇 O CloudFormation oferece diversos benefícios, como:_

* _Automação: Provisiona e configura recursos automaticamente com base nos modelos._
* _Reutilização: Permite replicar a infraestrutura em várias regiões ou contas reutilizando os mesmos modelos._
* _Controle de Alterações: Facilita o rastreamento de mudanças na infraestrutura, semelhante ao controle de versão de código._
* _Escalabilidade: Suporta desde configurações simples até arquiteturas complexas e multirregionais._

### _Há pelo menos duas formas básicas de criar uma Stack com o AWS Cloud Formation:_ ###


1️⃣ Infrastructure Composer: Ferramenta de design visual que permite criar e configurar aplicativos de forma dinâmica.

>> Dica: Voce pode criar no Infrastructure Composer uma base modelo para seu Stack , após validar,
>> você pode salvar o arquivo YAML e editá-lo posteriormente conforme a necessidade.


2️⃣ Selecionar Modelo Existente: Você pode criar seu stack através de um modelo existente da AWS, ou fazer o upload de um arquivo com as configurações, e ainda temos a opção de selecionar diretamente de um repositório do GitHub nosso arquivo de configurações.

>> Modelo Padrão: Mesmo depois de selecionar um modelo padrão você pode acessar o Infrastructure Composer para visualizá-lo \
>> IAM: Embora você possa criar um stack sem uma função de serviço IAM, é recomendável usar uma para gerenciar permissões de forma mais segura e eficiente. Isso ajuda a evitar problemas de segurança e facilita a gestão de recursos.
   
---

## 🎲 Integrações: 




 ✔ AWS CLI - Você pode usar a AWS CLI para interagir com o CloudFormation para criar, atualizar e excluir pilhas, entre outras operações. \
 ✔ AWS Management Console - Para criar um stack, você pode usar a interface do AWS Management Console. \
 ✔ AWS SDK -  O AWS SDK permite que você trabalhe com templates do CloudFormation. Você pode criar, atualizar ou excluir stacks usando os métodos disponíveis no SDK, que variam conforme a linguagem de programação que você está utilizando (como Python, Java, .NET, etc.).

---
## 🎲 Conteúdos:


![Criando Modelo](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5de8b780346729078e5a4f12aae5a82f57b9c3b3/3_Desafio_CloudFormation/images/Modelo_Criacao_Composer.PNG)

![Salvando Modelo](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5de8b780346729078e5a4f12aae5a82f57b9c3b3/3_Desafio_CloudFormation/images/Salvando_Modelo.png)

![YUML](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5daae0f2f90d27f6695398f85c94d40e1b248733/3_Desafio_CloudFormation/template.yaml)


