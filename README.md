# Blog do Adriano

Repositório da aplicação desenvolvida no curso de Python 3 e Django em ambiente Linux Ubuntu 22.04.1 LTS.

O Projeto utiliza:
- Framework Django versão 2.2.3
- MySQL Client versão 2.1.1
- Python 3.7

# Iniciando o projeto

É preciso realizar o clone do repositório

    https://github.com/adrianocerutti/blog_django.git

# Criando o ambiente virtual

É necessário criar o ambiente virtual para que sejam instaladas as dependências do projeto, então abra o
projeto no PyCharm ou VS Code. No PyCharm provavelmente vai identificar e te informar sobre a criação do ambiente.
No VS Code, abra o terminal e digite o seguinte comando:

    python<versão_do_python_instalada> -m venv venv

# Ativando ambiente virtual (venv) e instalando as dependências

Você precisa estar com o ambiente virtual ativo antes de instalar as dependências. Se o projeto for aberto no PyCharm
ele provavelmente vai identificar e vai ativar o ambiente virtual, caso seja aberto no VS Code, abra o terminal do
próprio VS Code e digite o comando:

    source nome_da_virtualenv/bin/activate (Linux ou macOS)
    nome_da_virtualenv/Scripts/Activate (Windows)

Se o projeto for aberto no PyCharm ele provavelmente vai identificar o arquivo e instalar as dependências,
caso seja aberto no VS Code, abra o terminal do sistema ou o terminal do próprio VS Code e digite o comando:

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