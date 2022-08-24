# Blog do Adriano

Repositório da aplicação desenvolvida no curso de Python 3 e Django em ambiente Linux Ubuntu 22.04.1 LTS.

O Projeto utiliza:
- Framework Django versão 2.2.3
- MySQL Client versão 2.1.1
- Python 3.7

# Iniciando o projeto

É preciso realizar o clone do repositório

    https://github.com/adrianocerutti/blog_django.git

# Instalando as dependências

Abra o terminal do sistema ou o terminal do próprio VS Code e digite o comando:

    pip install -r requirements.txt

# Criando e configurando o arquivo de ambiente

Abra o arquivo .env.example e salve-o com o nome .env na raíz do projeto.

    * configurações do banco de dados
    - ENGINE=django.db.backends.mysql
    - NAME=nome_do_banco_de_dados
    - HOST=127.0.0.1
    - PORT=3306
    - USUARIO=usuario_do_banco_de_dados
    - PASSWORD=senha_do_banco_de_dados

# Criando o banco de dados

Abra o MySQL Workbench ou qualquer outro gerenciador de banco de dados e digite o comando e depois execute:

    create database <nome_do_seu_banco>;

# Criando as tabelas do banco de dados

No PyCharm ou VS Code, abra o terminal e digite o comando:

    python manage.py migrate

# Rodando a aplicação

No terminal e digite o comando:

    python manage.py runserver