# readme.md

# Instruções Docker Hello World 🐳




Antes de começar, certifique-se de que você possui o **Docker** instalado e em funcionamento na sua máquina.

Para verificar se a instalação foi bem-sucedida, abra o terminal e execute:
```bash
docker --version

🚀 Como Executar o Hello World
O Docker possui uma imagem oficial de testes chamada hello-world. O comando abaixo se encarrega de baixar a imagem (caso ela não exista na sua máquina) e criar um contêiner para executá-la.

No seu terminal, execute os seguintes comandos:

🔍 docker pull hollo-world🛠️
🔍 docker run hello-world🛠️

# 🐳 Localhost com Docker e Nginx — Windows 11

Este projeto demonstra como criar um **servidor web local utilizando Docker e Nginx** no Windows 11, permitindo acessar arquivos HTML, CSS e JavaScript através de:

```text
http://localhost:8080
```

* `docker run` → cria e executa um container.
* `-d` → executa em segundo plano.
* `127.0.0.1:8080:80` → conecta a porta 8080 do Windows à porta 80 do Nginx.
* `--name meu-site` → define o nome do container.
* `nginx` → imagem utilizada.

## 3. Verificar o container

```cmd
docker ps
```

Deve aparecer o container `meu-site` e o mapeamento:

```text
127.0.0.1:8080->80/tcp
```

## 4. Testar o localhost

Abra o navegador e acesse:

```text
http://localhost:8080
```

Inicialmente será exibida a página padrão:

```text
Welcome to nginx!
```

## 5. Utilizar seus próprios arquivos

Supondo que seus arquivos estejam em:

```text
C:\Users\franciscooliveira673\Documents\meu-projeto
```

E a estrutura seja:

```text
meu-projeto
├── index.html
├── style.css
└── script.js
```

Primeiro remova o container anterior:

```cmd
docker stop meu-site
docker rm meu-site
```

Depois crie novamente utilizando a pasta do projeto:

```cmd
docker run -d -p 127.0.0.1:8080:80 --name meu-site -v "C:\Users\franciscooliveira673\Documents\meu-projeto:/usr/share/nginx/html" nginx
```

O parâmetro `-v` conecta a pasta do Windows com a pasta utilizada pelo Nginx dentro do container.

```text
Windows
C:\...\meu-projeto
        │
        ▼
Docker / Nginx
/usr/share/nginx/html
        │
        ▼
localhost:8080
```

## 6. Acessar os arquivos

Abra:

```text
http://localhost:8080
```

