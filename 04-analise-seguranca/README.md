# 🔐 Plano de Segurança e Secure SDLC (Shift-Left)

Implementei o concept de *Shift-Left*, integrando controles de segurança desde as fases iniciais do desenho de arquitetura do sistema para mitigar riscos críticos antes da codificação.

### 🔹 Análise de Riscos (OWASP Top 10)
* **Injeção de SQL (Risco Crítico):** Mitigado através do uso de consultas parametrizadas (*Prepared Statements*) e sanitização rigorosa de inputs.
* **Quebra de Autenticação (Risco Alto):** Mitigado com armazenamento de senhas via hashing seguro (Bcrypt/Argon2) e controle de acesso baseado em funções (RBAC).
* **Cross-Site Scripting - XSS (Risco Médio):** Mitigado com a filtragem de caracteres especiais nos campos de agendamento.

### 🔹 Estratégia de Testes de Segurança
* **SAST:** Análise estática automatizada do código-fonte para detectar padrões inseguros.
* **DAST:** Simulação de ataques dinâmicos em tempo de execução (varreduras contra XSS e injeções).
* **Pentest:** Planejamento de testes de penetração com especialistas para validar a resiliência das camadas de defesa.