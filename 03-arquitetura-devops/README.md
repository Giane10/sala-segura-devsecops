# 🏗️ Planejamento de Infraestrutura e Pipeline DevOps

Desenhei a arquitetura de infraestrutura e o fluxo de trabalho automatizado para sustentar o sistema de forma escalável e replicável, priorizando ferramentas Open Source.

### 🔹 Stack Tecnológica Selecionada
* **Controle de Versão:** Git (local) e GitLab (servidor).
* **CI/CD:** Jenkins para automação de esteiras de integração e entrega contínua.
* **Infraestrutura como Código (IaC):** Terraform para provisionamento e Ansible para gerenciamento de configuração.
* **Orquestração:** Clusters Kubernetes rodando em nós Linux com Horizontal Pod Autoscaling (HPA).
* **Monitoramento:** Prometheus (coleta de métricas) e Grafana (dashboards).

### 🔹 Fluxo da Pipeline (CI/CD)
1. **Code:** Check-in de código no repositório.
2. **Build & Test:** Jenkins realiza o build automático e roda testes unitários.
3. **Deploy:** Implantação automatizada via CD em ambiente de staging/produção após aprovação.
4. **Monitor:** Coleta contínua de feedback de performance.