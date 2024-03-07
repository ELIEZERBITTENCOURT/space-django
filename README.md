# Baixando o projeto

Primeiramente, é necessário baixar o projeto em nossa máquina, então temos duas alternativas:

1. **Acessar o repositório do Github e fazer um git clone.**
2. **Ou baixar o projeto zipado e descomprimi-lo.**

Em seguida, vamos iniciar o VS Code e arrastar a pasta do projeto para ele. Desse modo, o editor de códigos abrirá o projeto e podemos checar a estrutura de pastas no painel "Explorador", à esquerda.

## Criando o ambiente virtual

Antes de alterar qualquer código, é imprescindível criar um ambiente virtual para nosso projeto Python.

De início, criaremos um terminal, pressionando "Ctrl + Shift + '".

Nós vamos utilizar o ambiente virtual do virtualenv, portanto usaremos o comando ``python -m virtualenv`` seguido do nome desejado. Por padrão, usamos .venv:

```bash
python -m virtualenv .venv
```

Uma vez criada a virtualenv, é preciso ativá-la com o seguinte comando:

```bash
.venv\Scripts\activate
```

Agora, nosso ambiente está ativado!

## Configurando o interpretador

A seguir, vamos verificar se o interpretador selecionado no VS Code é o que está dentro do nosso ambiente virtual — ou seja, o Python que instalamos na virtualenv.

No VS Code, vamos pressionar "Ctrl + Shift + P", pesquisar a palavra "interpretador" e escolher a opção "Python: Selecionar Interpretador". Em seguida, clicaremos em "Insira o caminho do interpretador" e, depois, em "Localizar...".

Uma janela de seleção de arquivos será aberta. Vamos navegar até "projeto > .venv > Scripts", selecionar o arquivo ``python.exe`` e clicar no botão "Selecionar Interpretador" no canto inferior direito da janela.

Pronto! O interpretador correto foi selecionado.

Essa etapa é muito importante para confirmar que estamos trabalhando com o Python presente na virtualenv. Do contrário, podemos nos deparar com erros no futuro.

## Instalando os requirements

Por fim, faremos a instalação dos recursos listados no arquivo ```requirements.txt```. Eles são essenciais para o funcionamento do projeto, o próprio Django consta nessa lista!

No terminal, vamos executar o seguinte comando:

```bash
pip install -r requirements.txt
```

Todos os pacotes serão coletados e, uma vez finalizado esse processo, estaremos prontos para rodar nosso projeto.

## Rodando o projeto

No terminal, vamos executar o seguinte comando:

```bash
python manage.py runserver
```
