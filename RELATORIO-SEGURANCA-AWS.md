# RELATÓRIO DE IMPLEMENTAÇÃO DE SEGURANÇA EM SERVIÇOS AWS

Data: 06/11/2026
Empresa: Abstergo Industries
Responsável: Caio do Nascimento Bessa

## Introdução
Este relatório apresenta o processo de implementação de ferramentas de segurança na nuvem na empresa Abstergo Industries, realizado por Caio do Nascimento Bessa. O objetivo do projeto foi elencar 3 serviços e recursos da AWS, com a finalidade de proteger o acesso, os dados e o monitoramento do ambiente em nuvem da empresa.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1:
- AWS IAM (Identity and Access Management)
- Controle de identidades e permissões de acesso aos recursos da AWS
- Utilizado para garantir que cada pessoa e cada serviço acesse somente o que precisa (princípio do privilégio mínimo). Foram definidos grupos e perfis (roles) com políticas específicas, em vez de permissões amplas. Também foi ativada a autenticação multifator (MFA) para todos os usuários, principalmente para a conta root, que deixa de ser usada no dia a dia. Credenciais de longa duração são substituídas por roles temporárias, e o IAM Access Analyzer é usado para identificar acessos excessivos ou públicos.

Etapa 2:
- AWS KMS (Key Management Service) e criptografia de dados
- Proteção dos dados em repouso e em trânsito por meio de criptografia
- Utilizado para criptografar os dados da empresa com chaves gerenciadas pelo KMS. Os buckets do Amazon S3 passam a usar criptografia SSE-KMS, as instâncias do Amazon RDS e os volumes do Amazon EBS (usados pelas instâncias EC2) são criados com criptografia ativada, e a rotação automática das chaves é habilitada. Para os dados em trânsito, as conexões utilizam TLS/HTTPS. O acesso às chaves é controlado por políticas do IAM e as operações com elas são registradas para auditoria.

Etapa 3:
- Amazon CloudWatch
- Monitoramento, registro de logs e alertas do ambiente
- Utilizado para acompanhar a saúde e a segurança dos recursos. Os logs são centralizados no CloudWatch Logs e, junto com os eventos do AWS CloudTrail, são analisados por filtros de métricas que identificam situações suspeitas, como tentativas de login mal sucedidas, uso da conta root e chamadas de API não autorizadas. Alarmes do CloudWatch enviam notificações por meio do Amazon SNS, permitindo que a equipe responda rapidamente a possíveis incidentes.

## Conclusão
A implementação de ferramentas na empresa *Abstergo Industries tem como esperado o controle mais rigoroso dos acessos, a proteção dos dados contra acessos indevidos e a detecção rápida de atividades suspeitas no ambiente em nuvem*, o que aumentará a segurança e a confiabilidade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

- Documentação oficial do AWS IAM: https://docs.aws.amazon.com/iam/
- Documentação oficial do AWS KMS: https://docs.aws.amazon.com/kms/
- Documentação oficial do Amazon CloudWatch: https://docs.aws.amazon.com/cloudwatch/
- Documentação oficial do AWS CloudTrail: https://docs.aws.amazon.com/cloudtrail/

Assinatura do Responsável pelo Projeto:

Caio do Nascimento Bessa
