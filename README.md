# Desafio Técnico

Este projeto é um sistema de gerenciamento de funcionários desenvolvido como parte de um desafio técnico para entrevista. A aplicação possui um
foco em frontend Angular, foi usado backend em NODE com uma API REST completa, autenticação JWT, testes unitários, Dockers e containers.

## 🚀 Começando

Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.

Esse projeto foi gerado com [Angular CLI](https://github.com/angular/angular-cli) na versão 16.2.0.

- Consulte **[Documentação Docker e Containers](#-sobre-o-dockerfile)** para saber como utilizar o Docker e Containers.
- Consulte **[Documentação API](#-documentação-da-api)** para ver a documentação da API.

### 📋 Pré-requisitos

- De que coisas você precisa para instalar o projeto e como instalá-lo?

  ```
  Node v18.20.4
  Angular v16
  Github
  ```

  > Os links dos downloads: **[Construído com](#️-construído-com)**

## 🔧 Instalação

Para configurar o ambiente de desenvolvimento local, siga os passos abaixo:

1. **Abra um terminal**:

   - Abra um terminal onde quer deixar o projeto.

2. **Clone o repositório**:

   - Primeiro, clone o repositório para sua máquina local.

   ```bash
   git clone https://github.com/Jesiel15/gerenciador-funcionarios
   ```

   - Segundo, abra o projeto pelo terminal.

   ```bash
   cd gerenciador-funcionarios
   ```

   - Terceiro, rode o comando para instalar as dependências.

   ```bash
   npm install
   ```

   - Por último, rode o projeto.

   ```bash
   npm start
   ```

## ⚙️ Executando os Testes

Este projeto utiliza testes automatizados para garantir a qualidade do código. Siga os passos abaixo para rodar os testes em seu ambiente local.

1. **Instale as dependências**:

   - Para rodar os testes, é necessário ter as dependências do projeto instaladas.

   ```bash
   npm install
   ```

2. **Executar os testes unitários**:
   - Use o comando abaixo para rodar os testes unitários com o framework de testes do Angular (Jasmine e Karma).
   ```bash
   ng test
   ```
   ou
   ```bash
   npm test
   ```

---

## 📦 Implantação

Para implantar esta aplicação em um ambiente de produção, siga os passos abaixo:

**Build da aplicação Angular (frontend):**

- Gere os arquivos otimizados de produção com o comando:
  ```bash
  ng build --configuration=production
  ```

## 🐳 Executando com Docker

Este projeto pode ser executado em containers utilizando Docker, com a aplicação Angular servida diretamente via `ng serve` ou `npm start` .

### 🔸 Login Docker pelo terminal

- Execute o comando abaixo para logar via terminal no Docker

  ```bash
  docker login
  ```

### 🔸 Build da imagem Docker

- Execute o comando abaixo para criar a imagem do container. Caso queira apenas rodar a imagem hospeda no **[Docker Hub](https://hub.docker.com)**, pule esse comando:

  ```bash
  docker build -t fariajesiel/gerenciador .
  ```

### 🔸 Executar o container

- Depois de construir a imagem, execute o container com o seguinte comando. Se não existir uma imagem local, vai trazer o **[Repositório](https://hub.docker.com/repository/docker/fariajesiel/act-gerenciador/general)** no Docker Hub:

  ```bash
  docker pull fariajesiel/gerenciador
  docker run -dti -p 4200:4200 fariajesiel/gerenciador
  ```

  > A aplicação estará disponível em: **http://localhost:4200**

### 🔸 Sobre o Dockerfile

- O Dockerfile utiliza a imagem base do Node.js, instala as dependências do projeto, instala o Angular CLI globalmente e expõe a porta padrão 4200 para acesso à aplicação:

  ```Dockerfile
  FROM node:18.20.4
  WORKDIR /app
  COPY . .
  RUN npm install
  RUN npm install @angular/cli -g
  EXPOSE 4200
  CMD ["ng", "serve", "--host", "0.0.0.0"]
  ```

## 🛠️ Construído com

Ferramentas usadas na criação do projeto:

- [Angular](https://v16.angular.io/guide/setup-local) - Framework para desenvolvimento de aplicações web front-end

- [NODE](https://nodejs.org/pt/download) - Gerente de Dependência

- [Github](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop) - Plataforma para hospedagem, versionamento e colaboração em projetos de desenvolvimento de software

- [VSCode](https://code.visualstudio.com) - Editor de código leve e poderoso com suporte a extensões

- [Postman](https://www.postman.com/downloads) - Ferramenta para testar, documentar e automatizar APIs REST de forma prática e eficiente

- [Docker](https://www.docker.com/get-started/) - Docker é uma tecnologia que permite criar e usar contêineres, que são pacotes de software que executam aplicações.

## 📚 Documentação da API

A documentação completa da API REST utilizada neste projeto está disponível no Postman. Nela, você encontrará todos os endpoints organizados com descrições, exemplos de requisições e respostas, além dos detalhes de autenticação e códigos de status.

📎 Acesse a documentação aqui:  
👉 [Documentação da api](https://documenter.getpostman.com/view/15165244/2sAYdoESqn#89c346c7-1432-4bf6-8721-5f0a2adff646)

## ✒️ Autores

Colaboradores:

- **Jesiel Faria** - _Desenvolvedor_ - 📎 [Perfil do github](https://github.com/Jesiel15)

## 📄 Licença

Este projeto está licenciado sob os termos da licença **MIT**.
Você pode usá-lo livremente para uso pessoal ou comercial, com a condição de manter os créditos ao autor.
Consulte o arquivo [LICENSE.md](./LICENSE.md) para mais detalhes (licença original em inglês).

## 🎁 Expressões de gratidão

- Esse projeto foi um desafio proposto a uma vaga de emprego frontend senior 📢;
- Agradeço a pela oportunidade;

---

⌨️ com ❤️ por [Jesiel Faria](https://github.com/Jesiel15) 😊
