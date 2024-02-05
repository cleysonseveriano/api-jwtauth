# API utilizando Express | MongoDB | JWT | Bcrypt

Esta é uma API simples, apenas para fazer uma lógica e validação de login, com email e senha. Foi utilizado jwt para gerar tokens de acesso aos dados do usuário, e bcrypt para criar hashs das senhas fornecidas pelo usuário cadastrado. 

## Requisitos

- Node.js
- npm (gerenciador de pacotes do Node.js)

## Instalação

### 1. Clone o repositório para sua máquina local:

```
git clone https://github.com/cleysonseveriano/api-jwtauth.git
```
### 2. Navegue até o diretório do projeto

### 3. Instale as dependências necessárias:

  ```
  npm install
  ```
  ## Funcionalidades
### 1. Iniciar a API.

Para iniciar a API, execute o seguinte comando:

```
npm run dev
```
A API será executada na porta 3000 por padrão, ou na porta especificada pela variável de ambiente PORT.

### 2. Endpoints

 - GET "/" Retorna uma mensagem 1.0.0 em json, sinalizando que é a 1ª versão da api.

 - GET "/user/:id" Retorna o usuário por id, porém só é possível se tiver token para acesso.

 - POST "/auth/register" Registra um novo usuário.

 - POST "/auth/login" Faz a lógica de autenticação de login, de acordo com os dados fornecidos, gerando token para acesso.

### 3. Exemplo de Uso

E para adicionar um novo produto, você pode enviar uma requisição POST na rota "/auth/register" com os detalhes do usuário no corpo da requisição:

```
{
  "name": "Antonio",
  "email": "antonio@antonio.com",
  "password": "antoniopass",
  "confirmPassword": "antoniopass"
}
```