# FLAPS-Tech-docs
Repositório destinado à documentação da empresa FLAPS.

## Instruções

Para rodar o site localmente, basta seguir os seguintes comandos:

Ir até o diretório da documentação.

```shell
cd flaps
```
Adicionar o ambiente virtual ao projeto (Windows).

```shell
python -m venv venv
```

Adicionar o ambiente virtual ao projeto (Linux).

```shell
python3 -m venv venv
```

Ativar o ambiente virtual (Windows).

```shell
.\venv\Scripts\activate
```

Ativar o ambiente virtual (Linux).

```shell
source venv/bin/activate
```

Baixar as dependências.
```shell
pip install -r requirements.txt
```

Comando para rodar localmente.
```shell
mkdocs serve --livereload
```

Caso baixe alguma dependência a mais para o projeto, rode o comando:

```shell
pip freeze > requiremts.txt
```
