 # ✅ Quarto Desafio - Projeto de Automação no AWS Cloud Formation

_Veremos abaixo a resolução do desafio 4 do Bootcamp Santander Code Girls 2025._ \
_Será resumido a criação de uma stack com AWS Cloud Formation onde criaremos um ambiente de testes contendo: Uma VPC, uma sub-rede e uma instâmcia EC2._ \
_Este ambiente pode ser usado para testes fora de seu ambiente de produção. O ambiente pode ser destruído após seu uso e realização de testes necessários._ \
_Com nosso template de código YAML o ambiente pode ser criado, usado e destruído sempre que necessário_ \

---

## ⚙️ Passo a passo da implantação.

_A criação de uma stack é relativamente simples, se tiver todos os parâmetros de sua criação pré-definidos, é sempre aconselhável fazer uma mapeamento detalhado de sua stack. Para análise de uso e redução de custos na criação de recursos dentro da AWS._ 

_Vamos acompanhar os passos a seguir para criação de nosso ambiente de testes._ 

1️⃣ Primeiro vamos acessar nossa conta AWS com um usuário que tenha as devidas permissões para elaboração de uma Stack e de recursos, assim podemos acessar o AWS Cloud Formation, sempre se certifique de estar na região correta para criação da stack e dos recursos.

2️⃣ Selecionaremos a opção de criação de Stack, teremos a opção de criação a partir de um modelo, e faremos o upload do nosso arquivo YAML.

3️⃣ Após carregamento do arquivo podemos visualizar no Infrastructure Composer seu stack, e lá mesmo podemos também editar nosso arquivo YAML caso necessário e validá-lo

![Infrastructure Composer](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5de8b780346729078e5a4f12aae5a82f57b9c3b3/3_Desafio_CloudFormation/images/Modelo.PNG)

4️⃣ Após todas as alterações necessárias, podemos seguir com a criação da Stack, será solicitado o nome que daremos a Stack que está sendo criada, e seus parâmetros.

![Cracao Stack](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5de8b780346729078e5a4f12aae5a82f57b9c3b3/3_Desafio_CloudFormation/images/Modelo.PNG)

5️⃣ Em seguida podemos selecionar Tags, opções da stack no caso de falhas, configurações de segurança e de notificações da Stack.

6️⃣ O úlitmo passo é revisar todas as informações conffirmar a criação da Stack.

7️⃣ Nesse momento todos os recursos serão criados e poderão ser visualizados posteriormente no painel de gerenciamento


* _Automação: Provisiona e configura recursos automaticamente com base nos modelos._
* _Reutilização: Permite replicar a infraestrutura em várias regiões ou contas reutilizando os mesmos modelos._
* _Controle de Alterações: Facilita o rastreamento de mudanças na infraestrutura, semelhante ao controle de versão de código._
* _Escalabilidade: Suporta desde configurações simples até arquiteturas complexas e multirregionais._

>> Dica: Voce pode criar no Infrastructure Composer uma base modelo para seu Stack , após validar,
>> você pode salvar o arquivo YAML e editá-lo posteriormente conforme a necessidade.


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


