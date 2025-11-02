 # ✅ Quarto Desafio - Projeto de Automação no AWS Cloud Formation

_Veremos abaixo a resolução do desafio 4 do Bootcamp Santander Code Girls 2025._ \
_Será resumido a criação de uma stack com AWS Cloud Formation onde criaremos um ambiente de testes contendo: Uma VPC, uma sub-rede e uma instâmcia EC2._ \
_Este ambiente pode ser usado para testes fora de seu ambiente de produção. O ambiente pode ser destruído após seu uso e realização de testes necessários._ \
_Com nosso template de código YAML o ambiente pode ser criado, usado e destruído sempre que necessário._ 

---

## ⚙️ Passo a passo da implantação.

_A criação de uma stack é relativamente simples, se tiver todos os parâmetros de sua criação pré-definidos, é sempre aconselhável fazer um mapeamento detalhado de sua stack para análise de uso, e redução de custos na criação de recursos dentro da AWS._ 

🧭 _Vamos acompanhar os passos a seguir para criação de nosso ambiente de testes._ 

1️⃣ Primeiro vamos acessar nossa conta AWS com um usuário que tenha as devidas permissões para elaboração de uma Stack e de recursos, assim podemos acessar o AWS Cloud Formation, sempre se certifique de estar na região correta para criação da stack e dos recursos.

2️⃣ Selecionaremos a opção de criação de Stack, teremos a opção de criação a partir de um modelo, e faremos o upload do nosso arquivo YAML.

3️⃣ Após carregamento do arquivo podemos visualizar no Infrastructure Composer nossa stack, e lá mesmo, também temos acesso a edição de nosso código YAML, caso necessário faça as devidas alterações e, em seguida, clique em validar.

![Infrastructure Composer](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/3c366093b97d338461080dac578cddfbb376f225/4_Desafio_Automacao_CloudFormation/images/Modelo_Infraestructure_Composer.PNG)

4️⃣ Após todas as alterações necessárias, podemos seguir com a criação da Stack, será solicitado o nome que daremos a Stack que está sendo criada, e seus parâmetros.

![Detalhes Stack](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/3c366093b97d338461080dac578cddfbb376f225/4_Desafio_Automacao_CloudFormation/images/Detalhes_da_Stack.PNG)

5️⃣ Em seguida podemos selecionar Tags, opções da stack no caso de falhas, configurações de segurança e de notificações da Stack. Todas essas configurações podem ser importantes caso seu ambiente necessite ficar ativo por um tempo maior que o esperado.

6️⃣ O último passo é revisar todas as informações confirmar a criação da Stack.

7️⃣ Nesse momento todos os recursos serão criados automaticamente e poderão ser visualizados posteriormente no painel de gerenciamento.

---
### 🎲 Detalhes importantes pós criação da Stack: 

☑️ _Destruição do Ambiente: Podemos excluir todos os recursos criados excluindo essa stack_
☑️ _Reutilização: Com nosso código elaborado podemos recriar essa Stack sempre que necessário._ \
☑️ _Controle de Alterações: Facilita o rastreamento de mudanças na infraestrutura, semelhante ao controle de versão de código._

### 🥇 Dicas:

>> 🔖 Temos a opção de criar no Infrastructure Composer uma base modelo para seu Stack , após validar,você pode salvar o arquivo YAML e editá-lo posteriormente conforme a necessidade. \
>> 🔖 IAM: Embora você possa criar um stack sem uma função de serviço IAM, é recomendável usar uma para gerenciar permissões de forma mais segura e eficiente. Isso ajuda a evitar problemas de segurança e facilita a gestão de recursos. \
>> 🔖 Para garantir que nada seja acidentalmente retido, evite usar a política de exclusão Retain para recursos de teste. Se você precisar reter dados (como logs ou resultados de testes), armazene-os em um bucket S3 ou outro serviço de armazenamento de longo prazo que não seja gerenciado pela stack de teste em si, ou use uma função Lambda para fazer backup antes da exclusão'  \
>> 🔖 _Você também pode configurar o agendamento automático da exclusão da stack usando uma combinação de Lambda e Amazon EventBridge, conforme sugerido em práticas da AWS, para impor um ciclo de vida efêmero para a infraestrutura de teste._
   
---

### 🎲 Integrações: 

 ✔ AWS CLI - Você pode usar a AWS CLI para interagir com o CloudFormation para criar, atualizar e excluir pilhas, entre outras operações. \
 ✔ AWS Management Console - Para criar um stack, você pode usar a interface do AWS Management Console. \
 ✔ AWS SDK -  O AWS SDK permite que você trabalhe com templates do CloudFormation. Você pode criar, atualizar ou excluir stacks usando os métodos disponíveis no SDK, que variam conforme a linguagem de programação que você está utilizando (como Python, Java, .NET, etc.).

---
### 🔮 Modelo YUML:

![YUML](https://github.com/vanspirineti/DIO_Desafios_Code_Girls/blob/5daae0f2f90d27f6695398f85c94d40e1b248733/3_Desafio_CloudFormation/template.yaml)


