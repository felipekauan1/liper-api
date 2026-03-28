# 🚀 Liper-API - Redes Sociais com Laravel e JWT

Este repositório contém uma **API RESTful** robusta desenvolvida com o framework **Laravel**. O projeto simula as funcionalidades de uma rede social, focando em segurança, escalabilidade e gerenciamento de interações entre usuários através de tokens **JWT (JSON Web Token)**.

### 🔐 Autenticação JWT

Sistema de login seguro utilizando `tymon/jwt-auth`, garantindo que apenas usuários autenticados acessem os recursos protegidos.

### 📱 Feed e Interações

Lógica de feed (postagens de quem você segue), sistema de likes, comentários e upload de fotos.

### 👥 Gestão de Usuários

Endpoints para busca dinâmica de usuários, atualização de perfil (avatar/capa) e sistema de seguidores (follow/unfollow).

## 🛠️ Tecnologias Utilizadas

  * **Framework:** Laravel 7.x (PHP 7.2+).
  * **Autenticação:** JWT (JSON Web Token).
  * **Banco de Dados:** MySQL.
  * **Manipulação de Imagens:** Intervention Image.

## 📋 Funcionalidades Principais

  * **Auth System:** Registro, login, logout e refresh de tokens.
  * **Feed Dinâmico:** Algoritmo para listar postagens próprias e de usuários seguidos.
  * **Posts:** Criação de posts em texto ou imagem (com redimensionamento automático).
  * **Interatividade:** Sistema de "curtir" e "comentar" em publicações.
  * **Perfil:** Edição de dados pessoais e upload de fotos de perfil e capa.
  * **Busca:** Pesquisa dinâmica de usuários por nome.
  * **Follow System:** Relação entre usuários com contagem de seguidores e seguidos.

## 📁 Endpoints Principais (Routes)

  * `POST /auth/login` → Autenticação do usuário.
  * `GET /feed` → Recupera o feed principal.
  * `POST /feed` → Cria uma nova postagem.
  * `GET /user/{id}` → Retorna informações de um perfil específico.
  * `POST /post/{id}/like` → Alterna o estado de "curtir" em um post.
  * `GET /search` → Busca usuários pelo nome.

## 🚀 Como Instalar e Rodar

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/felipekauan1/liper-api.git
    ```

2.  **Instale as dependências:**

    ```bash
    composer install
    ```

3.  **Configure o Ambiente:**

      * Renomeie o arquivo `.env.example` para `.env`.
      * Configure suas credenciais de banco de dados no `.env`.

4.  **Gere as chaves do projeto:**

    ```bash
    php artisan key:generate
    php artisan jwt:secret
    ```

5.  **Rode as Migrations:**

    ```bash
    php artisan migrate
    ```

6.  **Inicie o servidor:**

    ```bash
    php artisan serve
    ```
