# Projeto ETL de Análise de Vendas

Este projeto é um exemplo de pipeline ETL (Extração, Transformação e Carga) para análise de dados de vendas. Ele foi desenvolvido com o objetivo de demonstrar a extração de dados de um arquivo CSV, a transformação desses dados e sua carga em um banco de dados MySQL para análise posterior.

## Objetivo

O objetivo deste projeto foi:

1. Carregar dados de vendas em um banco de dados MySQL.
2. Realizar transformações nos dados, como a conversão de tipos de dados e o tratamento de valores ausentes.
3. Garantir que o pipeline ETL fosse executado de forma simples e eficiente.

## Tecnologias Utilizadas

- **Python**: Para a criação do pipeline ETL e manipulação de dados.
- **Pandas**: Para a manipulação dos dados, incluindo a limpeza e a transformação dos dados.
- **MySQL**: Para armazenar os dados transformados em um banco de dados.
- **Boto3**: Para interação com o serviço AWS S3, no qual os dados foram armazenados inicialmente.
- **AWS Amazon S3**: Serviço de armazenamento em nuvem da AWS utilizado para hospedar o dataset de vendas. O arquivo CSV é carregado diretamente do S3 para processamento.

## Passos do Pipeline

1. **Extração**:
   - Os dados foram extraídos de um arquivo CSV armazenado no Amazon S3.
   - O arquivo contém informações de vendas, como ID do pedido, data, produto, quantidade, preço unitário, entre outros.

2. **Transformação**:
   - Os dados foram carregados para um DataFrame Pandas.
   - O tratamento de dados incluiu:
     - Remoção de valores ausentes.
     - Conversão de colunas para tipos apropriados, como a data.

3. **Carga**:
   - Os dados foram carregados em um banco de dados MySQL.
   - A tabela criada foi inserida no banco de dados para facilitar consultas e análises futuras.

## Como Executar o Código

1. **Pré-requisitos**:
   - Python 3.12 ou superior.
   - As bibliotecas necessárias estão listadas no arquivo `requirements.txt`:
     ```bash
     pandas
     boto3
     sqlalchemy
     pymysql
     ```

2. **Instalar as dependências**:
   - Use o seguinte comando para instalar as dependências:
     ```bash
     pip install -r requirements.txt
     ```

3. **Configuração do MySQL**:
   - Certifique-se de que o MySQL esteja instalado e configurado em sua máquina.
   - Crie um banco de dados chamado `vendas_dataset` (ou utilize o banco de dados que preferir).

4. **Configuração da AWS**:
   - Certifique-se de que suas credenciais da AWS estejam configuradas corretamente.

5. **Rodando o Código**:
   - O código pode ser executado diretamente no seu ambiente local. Basta garantir que o arquivo CSV esteja acessível e o MySQL esteja configurado corretamente.
   - Para rodar o código de ETL, execute o script Python.

## Estrutura do Projeto

- **etl_pipeline.py**: Script Python que contém o pipeline ETL.
- **requirements.txt**: Arquivo com as dependências necessárias.
- **vendas_dataset.csv**: Arquivo CSV com os dados de vendas.
- **README.md**: Este arquivo com as informações do projeto.

## Considerações Finais

Este projeto apresenta uma forma simples de implementar um pipeline ETL, transformando dados de vendas e armazenando-os em um banco de dados relacional para análises futuras.