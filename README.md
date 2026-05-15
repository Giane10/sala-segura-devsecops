# 🛡️ SalaSegura: Engenharia de Software End-to-End com DevSecOps

Bem-vindo ao repositório do **SalaSegura**! Este projeto documenta o ciclo de vida completo de desenvolvimento, segurança e operações de um sistema web de reserva de salas. O projeto foi estruturado seguindo as melhores práticas de mercado, desde a concepção ágil até a containerização persistente e segura.

---

## 🚀 Linha do Tempo do Projeto (Ciclo de Vida)

### 📋 1. Design e Planejamento Ágil
* **Concepção:** Criação do escopo do software com separação estrita de perfis (Usuário Comum vs. Administrador) e gestão de conflitos de horários em tempo real.
* **Metodologia Ágil:** Divisão do Product Backlog em Sprints semanais (32h de esforço estimado), priorizando o "núcleo de valor" (Autenticação e Reserva Básica) através de User Stories focadas em segurança.

### 🏗️ 2. Arquitetura de Infraestrutura & DevOps
Planejamento de uma infraestrutura escalável e resiliente baseada em ferramentas Open Source:
* **Orquestração:** Previsão de clusters Kubernetes (nós Linux) com escalabilidade automática (HPA).
* **Stack DevOps:** Git/GitLab para controle de versão, Jenkins para automação de Pipelines (CI/CD), Ansible/Terraform (IaC), além de monitoramento contínuo com Prometheus e Grafana.

### 🔐 3. Segurança desde o Design (Shift-Left & DevSecOps)
Implementação do modelo Secure SDLC para mitigar riscos críticos antes da escrita do código:
* **Modelagem de Ameaças:** Proteção proativa contra Injeção de SQL, Quebra de Autenticação e Cross-Site Scripting (XSS).
* **Controles Aplicados:** Uso de consultas parametrizadas (*Prepared Statements*), hashing seguro de senhas (BCrypt/Argon2) e controle de acesso baseado em funções (RBAC).
* **Estratégia de Validação:** Planejamento de testes automatizados de segurança divididos em SAST (análise de código-fonte) e DAST (testes em tempo de execução).

### 🐳 4. Implementação Prática e Containerização
Migração da aplicação desenvolvida em Golang para um ambiente de microsserviços isolado:
* **Ambiente Isolado:** Criação de imagens Docker personalizadas para padronizar o deploy e eliminar conflitos de dependências de infraestrutura.
* **Orquestração de Serviços:** Utilização do Docker-Compose para gerenciar portas e redes internas.
* **Persistência de Dados:** Resolução do desafio da volatilidade de containers (natureza efêmera) através da implementação de **Docker Volumes**, garantindo que as reservas persistam de forma permanente no host mesmo após a destruição dos containers.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem Backend:** Go (Golang)
* **Containers:** Docker / Docker-Compose
* **Banco de Dados:** PostgreSQL (Previsão de persistência)
* **Segurança:** RBAC, JWT, Criptografia TLS
* **Metodologia:** Scrum / Secure SDLC

---

## 📊 Resultados e Aprendizados
O projeto consolidou a importância da cultura DevSecOps. Integrar a segurança desde o planejamento da infraestrutura (Shift-Left) e garantir que a aplicação seja resiliente em ambientes containerizados provou ser o caminho ideal para entregas rápidas, estáveis e protegidas contra ameaças modernas.
