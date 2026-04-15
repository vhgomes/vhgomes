# Olá, eu sou o vhgomes 👋

Sou um Desenvolvedor Backend focado em **Go**. Construo sistemas distribuídos, microserviços, APIs e ferramentas CLI, aplicando as melhores práticas de arquitetura e observabilidade.

## 🛠️ Tecnologias e Ferramentas

### **Principal**
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

### **Infraestrutura e Observabilidade**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

---

## 🚀 Projetos em Destaque

Aqui estão os principais projetos em que estive trabalhando recentemente, demonstrando o meu foco em criar sistemas escaláveis, performáticos e bem estruturados:

### 📊 [FlowMetrics](https://github.com/vhgomes/flowmetrics)
**Plataforma de Analytics em Tempo Real**
* **O que é**: Funciona como um clone de infraestruturas como Segment e Mixpanel.
* **Stack**: Go (Microserviços, Fiber, gRPC), Apache Kafka, PostgreSQL, Redis, Prometheus, Grafana, Docker.
* **Destaques**: Arquitetura orientada a eventos dividida em múltiplos microserviços (Ingest, Enricher, Processor, Storage, Query). Fluxos assíncronos com Kafka e proxy gRPC. Observabilidade avançada.

### 🔔 [Notifier](https://github.com/vhgomes/notifier)
**Plataforma de Notificações Assíncronas**
* **O que é**: Serviço capaz de gerenciar o envio de notificações assíncronas por múltiplos canais (Email, Webhooks).
* **Stack**: Go, Fiber, Apache Kafka, PostgreSQL, Redis, Prometheus, Grafana.
* **Destaques**: Goroutine worker pool consumindo continuamente as mensagens no Kafka, tolerância a falhas utilizando Retry e Dead Letter Queue (DLQ), e API REST.

### 📰 [LudensNews](https://github.com/vhgomes/ludensnews)
**Coletor Automatizado de Notícias (Feeds RSS)**
* **O que é**: Automação que busca artigos de diversas fontes assíncronamente.
* **Stack**: Go, MongoDB, Redis, Docker.
* **Destaques**: Web scraping concorrente de extrema performance, validação e descarte de duplicatas utilizando o Redis, persistência contínua usando MongoDB.

### 🌐 [Go Checker](https://github.com/vhgomes/go-checker)
**Monitoramento de Status de Sites**
* **O que é**: API REST onde um usuário autênticado possa monitorar o tempo de resposta e status dos seus sites com dashboards interativos.
* **Stack**: Go, Gin, GORM, SQLite, Redis, JWT.
* **Destaques**: Autenticação stateless (JWT), processamento de histórico em tempo real utilizando Cron jobs, cache de requisições e dashboards com Redis.

### 💼 [JobTracker](https://github.com/vhgomes/job-tracker)
**Sistema de Rastreamento de Vagas de Emprego**
* **O que é**: Portal simples em Backend para mapear as buscas e evolução pessoal em vagas de emprego.
* **Stack**: Go, Gin, MongoDB, Docker.
* **Destaques**: Uso rigoroso de banco não relacional (NoSQL), estruturação robusta para lidar com os relacionamentos do MongoDB nativo no Go.

### 🗄️ [CLI Backup](https://github.com/vhgomes/cli-backup)
**Utilitário de Automação de Backups em CLI**
* **O que é**: Uma CLI nativa focada em lidar com manipulação e automação do sistema gerencial de arquivos OS.
* **Stack**: Go (Cobra, Zap), YAML.
* **Destaques**: Compressão de grandes arquivos usando algoritmos nativos (Zip), manipulação e cópia de subdiretórios via scripts automatizados sem alocações excedentes em memória.

---

## 📈 Estatísticas do GitHub

<p>
  <img src="https://github-readme-stats.vercel.app/api?username=vhgomes&show_icons=true&title_color=00ADD8&icon_color=00ADD8&theme=radical&hide_border=true" alt="Estatísticas do GitHub do vhgomes"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=vhgomes&layout=compact&theme=radical&hide_border=true&title_color=00ADD8" alt="Top Linguagens"/>
</p>
