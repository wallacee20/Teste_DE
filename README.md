
# Solução para Processamento de Dados - Pesquisa Industrial Anual - Empresas do IBGE

## Descrição

Este repositório contém a solução para o processamento de dados da **Pesquisa Industrial Anual - Empresas do IBGE**, utilizando **PySpark** para transformação dos dados e **Apache Airflow** para orquestração dos processos. O objetivo é configurar um ambiente de processamento de dados eficiente, realizar a extração, transformação e carga (ETL) dos dados e automatizar o fluxo de trabalho com o Airflow.

## Tecnologias Utilizadas

- **Docker**: Para orquestrar e gerenciar os containers do projeto.
- **Docker Compose**: Para configurar múltiplos containers de maneira simples.
- **Apache Airflow**: Para gerenciar a execução das tarefas de ETL através de DAGs.
- **PySpark**: Para manipulação e transformação de grandes volumes de dados de maneira distribuída.
- **Jupyter Notebook**: Para o desenvolvimento interativo do código no arquivo `workspace.ipynb`.

## Instruções
1. Configuração do Ambiente:
    - Configurar o docker-compose para iniciar os containers necessários.
    - Instalar os pacotes e dependências necessárias para o projeto.
    - Organizar a estrutura de pastas e ajustar permissões, se necessário.
    - ETL com PySpark:
Extração dos dados da Pesquisa Industrial Anual - Empresas do IBGE.
Transformação dos dados extraídos para um dataframe usando PySpark.
Exibição do resultado da transformação.
Orquestração com Apache Airflow:

2. Criar uma DAG (Directed Acyclic Graph) chamada pesquisa_industrial_anual_empresas.
    - Processar os dados utilizando a DAG e gerar os resultados na pasta de resultados.
      Passos de Implementação
      Configuração do Docker:

    - Certifique-se de que o arquivo docker-compose.yml está configurado corretamente,
      Inicie os containers com o comando docker-compose up.

3. Instalação de Pacotes:   
    - Instale as dependências necessárias, como PySpark, pandas, apache-airflow, entre outros pacotes essenciais para o processamento e orquestração.

# Desenvolvimento do Código:

 **Escreva o código necessário no notebook workspace.ipynb, contendo:**

A extração dos dados.
A transformação desses dados em um dataframe PySpark.
A execução da DAG para orquestrar o processamento e salvar os resultados.
Verificação de Resultados:

Acesse o Apache Airflow e execute a DAG pesquisa_industrial_anual_empresas.
Verifique se o processamento foi realizado corretamente e se os resultados estão na pasta de resultados.

## Estrutura do Projeto

A estrutura do repositório é a seguinte:

  ```
  ├── dags/
  │   ├── pesquisa_industrial_anual_empresas.py  # Definição da DAG
  ├── data/
  │   ├── raw/                                   # Dados brutos
  │   ├── processed/                             # Dados processados
  ├── notebooks/
  │   ├── workspace.ipynb                        # Notebook principal
  ├── results/
  │   ├── output/                                # Resultados gerados pela DAG
  ├── docker-compose.yml                         # Configuração do Docker Compose
  ├── requirements.txt                           # Lista de dependências
  └── README.md                                  # Este arquivo
  ```
## Conclusão
Esta solução fornece um pipeline escalável, utilizando ferramentas modernas como PySpark e Airflow, permitindo o processamento eficiente dos dados da Pesquisa Industrial Anual do IBGE.
