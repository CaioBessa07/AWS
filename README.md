# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 02/11/2026
Empresa: Abstergo Industries
Responsável: Caio do Nascimento Bessa

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Caio do Nascimento Bessa. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1:
- Amazon S3 (Simple Storage Service)
- Armazenamento de objetos escalável, durável e de baixo custo
- Utilizado para armazenar backups, logs, arquivos estáticos e documentos da empresa. Com as classes de armazenamento (como S3 Intelligent-Tiering e S3 Glacier) e as políticas de ciclo de vida, os dados menos acessados são movidos automaticamente para camadas mais baratas, eliminando a necessidade de servidores de arquivos físicos e reduzindo o custo de armazenamento.

Etapa 2:
- Amazon RDS (Relational Database Service)
- Banco de dados relacional gerenciado
- Utilizado para hospedar os bancos de dados das aplicações da empresa sem a necessidade de administrar servidores, instalar patches ou configurar backups manualmente. O RDS automatiza backups, atualizações e monitoramento, reduzindo o esforço operacional e os custos com infraestrutura e manutenção. O uso de instâncias dimensionadas corretamente e de instâncias reservadas gera economia adicional.

Etapa 3:
- Amazon EC2 (Elastic Compute Cloud)
- Servidores virtuais sob demanda (capacidade computacional)
- Utilizado para executar as aplicações da empresa com o tamanho de instância ideal para cada carga de trabalho, pagando apenas pelo tempo de uso. Com o dimensionamento correto das instâncias (right-sizing), o desligamento de ambientes fora do horário de uso e opções como Savings Plans, Instâncias Reservadas ou Spot, é possível diminuir significativamente os gastos com computação.

## Conclusão
A implementação de ferramentas na empresa *Abstergo Industries tem como esperado a redução imediata de custos com infraestrutura, maior escalabilidade, segurança e disponibilidade dos dados e aplicações, além da diminuição do esforço operacional das equipes*, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

- Documentação oficial do Amazon S3: https://docs.aws.amazon.com/s3/
- Documentação oficial do Amazon RDS: https://docs.aws.amazon.com/rds/
- Documentação oficial do Amazon EC2: https://docs.aws.amazon.com/ec2/
- Calculadora de preços da AWS: https://calculator.aws/

Assinatura do Responsável pelo Projeto:

Caio do Nascimento Bessa
