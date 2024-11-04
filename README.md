# Desafio Arquiteto de Soluções

## Olá!👋Bem vindo a página do Desafio de Arquitetura de Soluções

<div>
<a href = "mailto:edsonhenriques@yaho.com"><img src="https://img.shields.io/badge/-eMail-%23333?style=for-the-badge&logo=mail.ru&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/edsonhenriquesantos" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
</div><p></p>
O objetivo deste repositório é apresentar uma solução arquitetural em resposta ao desafio proposto para avaliar a capacidade de conhecimento empírico do arquiteto de soluçõe, além de avaliar a capacidade de tomada de decisão, aplicação de boas práticas, decomposição dos domínios e componentes, etc.

<h1>Descritivo da solução</h1>
Desenhar uma solução que controle o fluxo de caixa diário com os lançamentos de débitos e créditos e que disponibilize o saldo diário consolidado. 

<h3>Requisitos de negócio:</h3>

- Controle financeiro de lançamentos (débitos e créditos).
- Geração de relatórios de saldo diário.
- Segurança e privacidade dos dados financeiros.
- Escalabilidade para atender a picos de demanda.
- Alta disponibilidade para garantir a continuidade do serviço.



<h3> Requisitos funcionais: </h3>

- Controle de lançamentos financeiros (débitos e créditos).
- Cálculo e consulta de saldos diários.
- Geração de relatórios financeiros personalizados.
- Cadastro e autenticação de usuários.
- Integração com sistemas de pagamento.
- Notificações de eventos relevantes (ex: transações, alertas).
- Armazenamento de dados financeiros em banco de dados transacional.

<h3> Requisitos não funcionais: </h3>

- Alta disponibilidade: O sistema deve estar disponível 24/7.
- Escalabilidade: O sistema deve ser capaz de lidar com um aumento significativo no volume de transações.
- Segurança: Os dados financeiros dos usuários devem ser protegidos.
- Desempenho: As transações devem ser processadas rapidamente.
- Confiabilidade: Os dados devem ser consistentes e precisos.
- Monitoramento e observabilidade: O sistema deve ser monitorado de forma contínua para identificar problemas e gerar alertas.

<h3>Entregáveis de Arquitetura: </h3><p>

- Mapeamento de domínios funcionais e capacidade de negócio
- Diagrama de contexto
- Diagrama de arquitetura de solução
- Justificativas arquiteturais


<h3>Domínios funcionais e capacidades: </h3>

- Domínio Financeiro: Realizar lançamentos, consultar saldos, gerar relatórios. 
- Domínio Pessoa: Cadastrar, alterar e excluir usuários.
- Domínio Segurança: Autenticar e autorizar acessos.
- Domínio Integração: Integrar sistemas (controle de lançamento, controle de saldo, notificações).
- Domínio de Dados: Armazenar dados financeiros, logs e métricas.


<h3> Diagrama de Contexto: </h3> 
<p align="center">
<img src="https://drive.google.com/uc?export=view&id=1Uw-42S8ZjqAI2xMrYVGRTlqXXRHOiyY6">
</p>


<h3>Arquitetura de Solução: </h3> 
<p align="center">
<img src="https://drive.google.com/uc?export=view&id=1tCheOMtxalmjevg53mpAMzdWZar9ppnR">
</p>


<h3> Tecnologias Sugeridas: </h3>

- Frontend: Angular para uma aplicação web reativa e moderna.
- API Gateway: AWS API Gateway para gerenciar as APIs, autenticação e roteamento.
- Autenticação: AWS AKS Kafka para notificações de eventos e CDC para distribuição de dados.
- Microsserviços: Node.js com Express.js para os serviços de lançamento e saldo.
- Banco de Dados: PostgreSQL para armazenar os dados de forma transacional.
- Mensageria/CDC: AWS MSK para comunicação assíncrona entre os microsserviços.
- Armazenamento: Amazon S3 para data lake.
- ETL: AWS Glcue para consolidar as informações financeiras.
- E-mail: AWS SNE para enviar e-mails de alertas e notificações.
- Relatórios: AWS Quicksight para gerar paineis e relatórios consolidados diários.
- Monitoramento: Prometheus e Grafana para coletar métricas e gerar gráficos.
