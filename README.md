<div align="center">

# Olá, eu sou o Victor Hugo 👋

### Desenvolvedor Backend | Go | Sistemas Distribuídos

</div>

Construo APIs, microsserviços e ferramentas CLI em **Go**, com foco em arquiteturas orientadas a eventos, resiliência (retry, DLQ, idempotência) e observabilidade. Gosto de entender o sistema de ponta a ponta: do design da infraestrutura (Kafka, AWS, Terraform) até os detalhes de concorrência e performance no código.

---

## 🛠️ Stack Tecnológica

**Linguagem & Frameworks**

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Gin](https://img.shields.io/badge/Gin-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Fiber](https://img.shields.io/badge/Fiber-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-4285F4?style=for-the-badge&logo=google&logoColor=white)

**Dados & Mensageria**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=for-the-badge&logo=amazondynamodb&logoColor=white)

**Cloud & Infraestrutura**

![AWS](https://img.shields.io/badge/AWS_Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

**Observabilidade**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

---

## 🚀 Projetos em Destaque

### 📊 [FlowMetrics](https://github.com/vhgomes/flowmetrics) — Plataforma de Analytics em Tempo Real
Clone de infraestrutura nos moldes de Segment/Mixpanel, organizado como monorepo com **seis microsserviços** independentes (ingest, enricher, processor, storage, query, api-gateway).
- Pipeline orientado a eventos com **Kafka** ligando todas as etapas de ingestão e enriquecimento.
- Comunicação interna via **gRPC** e exposição externa via **API Gateway REST**.
- Agregações em janelas de tempo, cache de consultas em **Redis** e persistência em **PostgreSQL**.
- Observabilidade completa com **Prometheus + Grafana** e dashboards provisionados via código.
- `Stack:` Go (Fiber, gRPC, sqlc) · Kafka · PostgreSQL · Redis · Prometheus · Grafana · Docker

### 🔔 [Notifier](https://github.com/vhgomes/notifier) — Plataforma de Notificações Assíncronas
Serviço de envio de notificações multi-canal (e-mail e webhook) desacoplado via mensageria.
- Worker pool em goroutines consumindo continuamente um tópico **Kafka**, com **retry automático** e **Dead Letter Queue** para falhas persistentes.
- Rastreamento de entregas via `delivery_log` em **PostgreSQL**, com queries geradas por **sqlc**.
- Métricas customizadas (latência de entrega, mensagens em voo, retries, DLQ) expostas via **Prometheus** e visualizadas em **Grafana**.
- `Stack:` Go (Fiber) · Kafka · PostgreSQL · Redis · Prometheus · Grafana

### 🔗 [LambdaLink](https://github.com/vhgomes/lambdalink) — Encurtador de URLs Serverless
Encurtador de links com rastreamento de cliques em tempo real, construído 100% serverless na AWS.
- Três funções **Lambda** em Go (criação, redirecionamento e processamento de cliques), com infraestrutura inteiramente definida em **Terraform**.
- Cliques são publicados de forma assíncrona em uma fila **SQS** (com DLQ), processados em lotes sem impactar a latência do redirecionamento.
- Persistência em **DynamoDB** com TTL nativo e GSI para consultas de analytics.
- Ambiente local replicado com LocalStack, sem custos de infraestrutura durante o desenvolvimento.
- `Stack:` Go · AWS Lambda · API Gateway · DynamoDB · SQS · Terraform

### 🌐 [Go Checker](https://github.com/vhgomes/go-checker) — Monitoramento de Status de Sites
API REST para monitoramento de disponibilidade e tempo de resposta de sites, com dashboards por usuário.
- Autenticação stateless com **JWT** e middleware de proteção de rotas.
- **Cron jobs** para atualização periódica do histórico de status e cache de dashboards em **Redis**.
- Persistência relacional com **GORM + SQLite** e histórico filtrável por data e status.
- `Stack:` Go (Gin, GORM) · SQLite · Redis · JWT · Cron

### 📰 [LudensNews](https://github.com/vhgomes/ludensnews) — Coletor Automatizado de Notícias (RSS)
Serviço que monitora múltiplas fontes RSS de forma concorrente e mantém um catálogo de artigos sem duplicatas.
- Uma goroutine independente por fonte, cada uma com seu próprio `ticker` de coleta.
- Deduplicação eficiente via **Redis** antes de qualquer escrita em banco.
- Persistência contínua em **MongoDB**, com ambiente de dependências (Mongo, Mongo Express, Redis) via Docker Compose.
- `Stack:` Go · MongoDB · Redis · Docker

### 💼 [JobTracker](https://github.com/vhgomes/job-tracker) — Rastreamento de Vagas de Emprego
API para organizar candidaturas a vagas, acompanhando empresas, status e comentários de cada etapa do processo.
- Modelagem 100% **NoSQL** em **MongoDB**, com tratamento explícito de relacionamentos via driver oficial.
- Camadas bem definidas de handlers, services e repositórios, com testes para a camada de banco e rotas.
- Containerizado com Docker para deploy simplificado.
- `Stack:` Go (Gin) · MongoDB · Docker

### 🗄️ [CLI Backup](https://github.com/vhgomes/cli-backup) — Automação de Backups via CLI
Utilitário de linha de comando para backup de arquivos, configurável por jobs definidos em YAML.
- Categorização automática de arquivos por tipo (texto, imagem, vídeo, outros) no destino.
- Compressão em ZIP com timestamp e validação prévia de caminhos de origem/destino.
- Logs estruturados com **Zap** e suíte de testes unitários para as regras de negócio.
- `Stack:` Go · Zap · YAML

---
</div>
