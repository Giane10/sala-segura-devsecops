# 🐳 Implantação Prática e Conteinerização com Docker

Nesta etapa final, o sistema web desenvolvido em Golang foi isolado em um ambiente de microsserviços utilizando Docker.

### 🔹 Tecnologias e Comandos Utilizados
* **Dockerfile:** Criação da imagem personalizada, compilando o binário em Go e estruturando os templates HTML.
* **Docker-Compose:** Orquestração do serviço, automatizando o mapeamento da porta local `8080` para a porta `8080` do container.
* **Diagnóstico:** Uso do comando `docker ps` para validar a integridade e o status operacional do container.

### 🔹 O Desafio da Persistência (Docker Volumes)
Por padrão, containers são efêmeros (voláteis), fazendo com que dados salvos internamente sejam destruídos ao rodar um `docker-compose down`. Para resolver isso, configurei a diretiva `volumes` no arquivo de orquestração:

* Mapeamento: `/home/aluno/reserva-salas/dados` (VM Host) -> `/app/dados` (Container)

Isso garantiu que os arquivos JSON de reservas persistissem de forma permanente no disco da máquina anfitriã, tornando a aplicação resiliente.