# Sistema de Gestão de Plano Ensino

Sistema de Gestão de Plano Ensino

# Como rodar no ambiente de desenvolvimento:

1. É preciso ter python 3.12.3 ou superior instalado na máquina
2. Criar um virtualenv com o comando `python -m venv venv` (só deve ser feito na primeira vez que clonar o repositório para a máquina)
3. Ativar o virtualenv com o comando:
- No Windows `venv\Scripts\activate`
- No Linux `source venv/bin/activate`
4. Instalar as bibliotecas com o comando `pip install -r requirements.txt`
5. Rodar a aplicação com o comando `flask run --debug`
6. Criar usuário admin para logar `flask fab create-admin` 
7. Rodar o comando para criar as tabelas no banco de dados `flask db upgrade`

# Quando gerar uma alteração ou criação de campos/tabelas faça:

1. É preciso criar o arquivo de migrate
2. Para isso execute o comando: `flask db migrate`

# Como aplicar alterações novas no banco de dados

1. Rode o comando: `flask db upgrade`

# Caso seja adicionado uma nova biblioteca no código

1. É preciso atualizar o requirements.txt para conter a nova biblioteca (informar a equipe)
2. Para isso execute o comando: `pip freeze > requirements.txt`

# Padrões para o desenvolvimento:

1. Crie um arquivo .py para cada model
2. Crie um arquivo .py para cada view