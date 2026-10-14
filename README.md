## Projeto_Avaliativo_CMA
# Análise de dados com Oracle HR

Projeto de análise de dados usando o schema **HR** do Oracle. Foram criadas consultas SQL com `LEFT JOIN` para explorar informações de salários e localização dos funcionários. Os resultados foram exportados para arquivos CSV.

## Consultas

- **Query 1 — Salários por departamento e cargo:** relaciona funcionários, departamentos e cargos para consultar os salários.
- **Query 2 — Funcionários por região:** relaciona funcionários, departamentos e informações de localização, como região.

As consultas utilizam `LEFT JOIN` para combinar os dados relacionados e preservar os registros da tabela principal mesmo quando não há correspondência em alguma tabela associada.

## Arquivos

- `query_1.sql` — consulta de salários por departamento e cargo.
- `query_2.sql` — consulta de funcionários por região.
- `query_01.csv` — resultados da primeira consulta.
- `query_02.csv` — resultados da segunda consulta.

## Tecnologias

- Oracle SQL
- Python
- Pandas
- Google Colab / Jupyter Notebook

## Como executar

1. Execute `query_1.sql` e `query_2.sql` no Oracle com acesso ao schema HR.
2. Exporte os resultados para `query_01.csv` e `query_02.csv`.
3. No notebook, carregue os CSVs com Pandas para explorar e analisar os dados.

```python
import pandas as pd

df_query_1 = pd.read_csv("query_01.csv")
df_query_2 = pd.read_csv("query_02.csv")
```

## Análise exploratória

A próxima etapa é explorar os dados no notebook, calculando estatísticas básicas — como média, mediana, mínimo e máximo — e criando visualizações para facilitar a interpretação dos resultados.

___________________________________________________________________________________________________________________________________________________________________________________________

## Projeto: Integração e Análise de Dados de RH (Oracle SQL & Python)
Este notebook apresenta o fluxo completo de carregamento, exploração e visualização de dados do módulo de Recursos Humanos (HR), integrando uma base de dados Oracle com técnicas de análise em Python.

## Objetivos do Projeto
Conectar com segurança a um banco de dados relacional Oracle SQL.
Executar consultas e carregar os dados diretamente no ambiente local.
Realizar uma análise exploratória de dados (EDA) para entender distribuições, médias salariais e tratar possíveis valores nulos.
Produzir visualizações gráficas de alta qualidade para suporte a tomada de decisão.

##  Tecnologias e Bibliotecas Utilizadas
Banco de Dados: Oracle SQL via biblioteca oracledb.
Manipulação de Dados: pandas.
Visualização Gráfica: matplotlib e seaborn.

## Segurança: getpass para ocultar senhas de acesso.
# Principais Etapas Desenvolvidas
Instalação e Conexão: Instalação do driver oracledb e teste de comunicação com a base de dados.
Importação e Inspeção: Leitura dos arquivos de consulta SQL (query_1.csv) para validação de tipos de dados, contagem de registros e checagem de nulos.
Cálculo Estatístico: Análise das médias, valores máximos e mínimos de remunerações.
Gráfico de Resultados: Plotagem de um gráfico de barras horizontal ilustrando a Média Salarial por Departamento.
