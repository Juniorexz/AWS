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

O AWS Lambda é um serviço serverless que executa código sob demanda em resposta a eventos. Ele elimina a necessidade de gerenciar servidores, oferece escalabilidade automática e integra-se facilmente com serviços como Amazon S3, AWS Step Functions e Amazon CloudWatch para criar aplicações e automações na nuvem

Serviço responsável pelo controle de acesso e segurança na AWS. Permite criar usuários, grupos e funções, além de definir permissões específicas para cada recurso, seguindo o princípio do menor privilégio para aumentar a proteção do ambiente.
