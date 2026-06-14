# AWS

Amazon S3 (Simple Storage Service)

Serviço de armazenamento de objetos da AWS utilizado para guardar arquivos de forma segura e escalável. É amplamente empregado para backup, hospedagem de sites estáticos, armazenamento de documentos, imagens, vídeos e dados para análise.

AWS Lambda

Serviço de computação serverless que permite executar código sem a necessidade de gerenciar servidores. O código é executado automaticamente em resposta a eventos, como uploads no S3, requisições de APIs ou alterações em bancos de dados.

AWS Step Functions

Serviço de orquestração que permite criar fluxos de trabalho automatizados integrando diversos serviços da AWS. Utiliza máquinas de estado para coordenar tarefas, controlar a sequência de execução, tratar erros e monitorar processos complexos.

Amazon CloudWatch

Serviço de monitoramento e observabilidade da AWS. Permite coletar métricas, logs e eventos de aplicações e recursos da nuvem, auxiliando na identificação de problemas, análise de desempenho e configuração de alertas.

AWS IAM (Identity and Access Management)


Tutorial Básico AWS Lambda

O AWS Lambda permite executar código automaticamente sem precisar criar ou gerenciar servidores.

Passo 1: Acesse o AWS Lambda
Entre no Console da AWS.
Pesquise por AWS Lambda.
Clique em Criar função.
Passo 2: Criar uma Função
Selecione Criar do zero.
Defina um nome, por exemplo: MinhaPrimeiraLambda.
Escolha uma linguagem (Python, Node.js, Java etc.).
Clique em Criar função.
Passo 3: Escrever o Código

Exemplo em Python:

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': 'Olá, AWS Lambda!'
    }
Passo 4: Testar a Função
Clique em Test.
Crie um evento de teste.
Execute a função.
Verifique o resultado e os logs.
Passo 5: Monitorar com CloudWatch

O Lambda envia logs automaticamente para Amazon CloudWatch.

Exemplo de log:

print("Função executada com sucesso!")
Passo 6: Integrar com S3

Você pode configurar a função para ser executada quando um arquivo for enviado ao Amazon S3.

Fluxo:

Upload de Arquivo
        ↓
     Amazon S3
        ↓
    AWS Lambda
        ↓
 Processamento
Passo 7: Integrar com Step Functions

Para processos mais complexos, utilize AWS Step Functions para coordenar várias funções Lambda em sequência.

Início
  ↓
Lambda 1
  ↓
Lambda 2
  ↓
Lambda 3
  ↓
Fim
Casos de Uso Comuns
Processamento de imagens enviadas ao S3.
APIs serverless.
Automação de tarefas.
Chatbots.
Integração com IA.
Processamento de logs e eventos.
Vantagens
Não precisa gerenciar servidores.
Escalabilidade automática.
Cobrança apenas pelo uso.
Integração nativa com outros serviços AWS.

Implementando sua Primeira Stack com AWS CloudFormation
Objetivo

Aprender a utilizar o AWS CloudFormation para automatizar a criação e o gerenciamento de recursos na AWS por meio de arquivos de configuração chamados templates.

O que é AWS CloudFormation?

O AWS CloudFormation é um serviço de Infraestrutura como Código (IaC) que permite definir recursos da AWS em arquivos YAML ou JSON. Com ele, é possível criar, atualizar e excluir ambientes inteiros de forma automatizada e padronizada.

Benefícios
Automação da infraestrutura.
Padronização de ambientes.
Redução de erros manuais.
Controle de versão dos recursos.
Facilidade para replicar ambientes.
Etapas Realizadas
1. Criação do Template

Foi criado um template em formato YAML contendo a definição dos recursos necessários.

Exemplo:

Resources:
  MeuBucket:
    Type: AWS::S3::Bucket
2. Criação da Stack

O template foi enviado ao CloudFormation para criação da Stack, que representa um conjunto de recursos gerenciados como uma única unidade.

3. Validação

Após a execução, foi possível acompanhar o progresso da criação dos recursos pelo console da AWS.

4. Atualização da Stack

Foram realizadas alterações no template para compreender o processo de atualização automática dos recursos.

5. Exclusão da Stack

Ao final do laboratório, a Stack foi removida para evitar cobranças desnecessárias.

Conceitos Aprendidos
Infrastructure as Code (IaC)
Templates YAML e JSON
Stacks
Recursos AWS
Automação de infraestrutura
Gerenciamento do ciclo de vida dos recursos
Conclusão

O AWS CloudFormation simplifica a criação e o gerenciamento de infraestrutura na nuvem, permitindo implementar ambientes completos de forma consistente, repetível e segura através de código.

Serviços Utilizados
AWS CloudFormation
Amazon S3
AWS IAM (dependendo do laboratório)
Resumo em uma frase

O AWS CloudFormation permite criar e gerenciar infraestrutura na AWS através de código, automatizando a implantação de recursos e garantindo consistência entre ambientes.
O AWS Lambda é um serviço serverless que executa código sob demanda em resposta a eventos. Ele elimina a necessidade de gerenciar servidores, oferece escalabilidade automática e integra-se facilmente com serviços como Amazon S3, AWS Step Functions e Amazon CloudWatch para criar aplicações e automações na nuvem.
AWS CLI

A AWS Command Line Interface é uma ferramenta de linha de comando que permite gerenciar serviços da AWS diretamente pelo terminal. Com ela, é possível criar, configurar e monitorar recursos sem acessar o console web.

Exemplos de uso:

Criar buckets S3.
Gerenciar instâncias EC2.
Configurar usuários IAM.
Automatizar tarefas administrativas.
AWS SDKs

Os SDKs da AWS são bibliotecas disponíveis para diversas linguagens de programação, como Python, Java, JavaScript e C#. Eles permitem que aplicações se comuniquem diretamente com os serviços da AWS por meio de código.

Exemplos de uso:

Upload de arquivos para o S3.
Envio de mensagens para filas.
Integração com serviços de IA.
Gerenciamento automático de infraestrutura.
Benefícios
Automação de processos.
Maior produtividade.
Integração com aplicações.
Redução de tarefas manuais.
Escalabilidade e padronização.
Conclusão

A AWS CLI e os SDKs são ferramentas fundamentais para automatizar operações e desenvolver aplicações integradas à AWS. Enquanto a CLI é ideal para administração e scripts, os SDKs permitem incorporar recursos da nuvem diretamente ao código das aplicações.

Resumo em uma frase

A AWS CLI permite gerenciar serviços da AWS via terminal, enquanto os SDKs possibilitam integrar e controlar esses serviços por meio de código em diferentes linguagens de programação.
Implementando Infraestrutura Automatizada com AWS CloudFormation
Objetivo

Aprender a automatizar a criação e o gerenciamento de recursos na AWS utilizando o AWS CloudFormation, aplicando o conceito de Infraestrutura como Código (IaC).

O que é AWS CloudFormation?

O AWS CloudFormation é um serviço que permite definir recursos da AWS por meio de arquivos de configuração (templates) em YAML ou JSON. Esses templates descrevem toda a infraestrutura necessária, possibilitando sua criação, atualização e remoção de forma automatizada.

Principais Benefícios
Automação da infraestrutura.
Padronização de ambientes.
Redução de erros manuais.
Facilidade de replicação.
Controle de versão da infraestrutura.
Gerenciamento centralizado dos recursos.
Etapas Realizadas
Criação de um template CloudFormation.
Definição dos recursos AWS necessários.
Criação da Stack através do template.
Monitoramento da implantação.
Atualização dos recursos por meio do template.
Exclusão da Stack ao término do laboratório.
Conceitos Aprendidos
Infrastructure as Code (IaC).
Templates YAML e JSON.
Stacks e recursos.
Automação de provisionamento.
Gerenciamento do ciclo de vida da infraestrutura.
Reprodutibilidade de ambientes.
Serviços Relacionados
AWS CloudFormation
Amazon EC2
Amazon S3
AWS IAM
Conclusão

O AWS CloudFormation permite criar e gerenciar infraestruturas completas por meio de código, tornando o provisionamento mais rápido, seguro, escalável e consistente entre diferentes ambientes.

Resumo em uma frase

O AWS CloudFormation automatiza a criação e o gerenciamento da infraestrutura na AWS através de templates, garantindo consistência, escalabilidade e redução de erros operacionais.

Serviço responsável pelo controle de acesso e segurança na AWS. Permite criar usuários, grupos e funções, além de definir permissões específicas para cada recurso, seguindo o princípio do menor privilégio para aumentar a proteção do ambiente.
Arquitetura Utilizada

Fluxo básico da solução:

O AWS Step Functions inicia a execução do workflow.
O workflow chama uma função AWS Lambda.
A função processa os dados recebidos.
O resultado é retornado ao Step Functions.
O fluxo segue para o próximo estado ou é finalizado.
Criação da Função Lambda

Foi criada uma função Lambda utilizando o runtime Node.js.

Exemplo de código:

exports.handler = async (event) => {
    return {
        statusCode: 200,
        message: "Execução realizada com sucesso!"
    };
};
Criação da State Machine

Foi criada uma State Machine utilizando o tipo Standard.

Exemplo de definição:

{
  "Comment": "Exemplo de execução Lambda",
  "StartAt": "ExecutarLambda",
  "States": {
    "ExecutarLambda": {
      "Type": "Task",
      "Resource": "arn:aws:states:::lambda:invoke",
      "End": true
    }
  }
}
Testes Realizados
Entrada
{
  "nome": "Teste"
}
Saída
{
  "statusCode": 200,
  "message": "Execução realizada com sucesso!"
}
Aprendizados
Resumo

Como criar funções AWS Lambda.
Como configurar permissões IAM para integração.
Como criar State Machines no AWS Step Functions.
Como executar workflows serverless.
Como monitorar execuções utilizando o histórico do Step Functions.
Como visualizar logs através do Amazon CloudWatch.
Benefícios da Integração
Eliminação do gerenciamento de servidores.
Escalabilidade automática.
Menor complexidade operacional.
Integração nativa entre serviços AWS.
Facilidade de monitoramento e rastreamento das execuções.
