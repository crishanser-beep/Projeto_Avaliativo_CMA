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
