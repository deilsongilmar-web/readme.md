# readme.md
instruções docker-hello world
# Projeto Docker Hello World 🐳

Este projeto demonstra o funcionamento básico do Docker através da execução do contêiner oficial de teste **"Hello World"**. É o ponto de partida ideal para verificar se o ambiente Docker está configurado corretamente e entender o ciclo básico de execução de um contêiner.

---

## 📋 Pré-requisitos

Antes de começar, certifique-se de que você possui o **Docker** instalado e em funcionamento na sua máquina.

* [Docker Desktop](https://www.docker.com/products/docker-desktop/) (para Windows ou macOS) ou o **Docker Engine** (para Linux).

Para verificar se a instalação foi bem-sucedida, abra o terminal e execute:
```bash
docker --version

🚀 Como Executar o Hello World
O Docker possui uma imagem oficial de testes chamada hello-world. O comando abaixo se encarrega de baixar a imagem (caso ela não exista na sua máquina) e criar um contêiner para executá-la.

No seu terminal, execute o seguinte comando:
🔍 Comandos Úteis para Explorar
Depois de rodar o comando principal, você pode usar os comandos abaixo para verificar o que aconteceu no seu ambiente:

Ver imagens baixadas na sua máquina:
(Você verá a imagem hello-world listada)
docker run hello-world

docker images
FROM alpine:latest

🛠️ (Opcional) Criando seu próprio "Hello World" customizado
Se você quiser criar o seu próprio arquivo de configuração para gerar uma imagem personalizada:

Crie um arquivo chamado Dockerfile na raiz do seu projeto.

Adicione o seguinte conteúdo (usando uma imagem base do Alpine Linux):
CMD ["echo", "Olá, Mundo! Este é o meu próprio container Docker!"]
docker build -t meu-hello-world .
docker run meu-hello-world
