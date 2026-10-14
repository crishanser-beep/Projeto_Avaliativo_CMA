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

![Média Salarial](images/media_salarial_departamento.png)
![Correlação](images/correlacao_funcionarios_salario.png)
![Outliers Salário](images/outliers_salario_medio.png)

_________________________________________________________________________________________________________________________________________________________________________________________

## Insights Baseados em Dados
A Disparidade Salarial do Setor Executivo (Outlier)

O que o dado diz: O setor Executive possui uma média salarial de **R$ 20.500,00**, figurando como um outlier óbvio no boxplot. * **Insight:** Enquanto a maior parte das funções e departamentos se encontra na faixa entre R$$ 20.500,00**, figurando como um outlier óbvio no boxplot. * **Insight:** Enquanto a maior parte das funções e departamentos se encontra na faixa entre R$ 5.000,00 e R$ 12.000,00, a remuneração da alta liderança está altamente concentrada no topo extremo. Isso é comum em estruturas corporativas, mas requer atenção em planos de cargos e salários para evitar insatisfação nos níveis operacionais.
A Relação entre Tamanho da Equipe e Salário (Correlação Negativa)

O que o dado diz: Temos uma correlação negativa moderada (-0.3583) entre o TOTAL_FUNCIONARIOS e o SALARIO_MEDIO.
Insight: Departamentos ou cargos que demandam um volume muito grande de colaboradores (como Shipping ou operacional) tendem a apresentar médias salariais menores. Já cargos altamente especializados (como Executive ou funções técnicas de nicho) possuem pouquíssimos colaboradores e remunerações bem mais elevadas. Isso aponta para uma estrutura de custos onde a folha de pagamento é pulverizada no operacional e concentrada no estratégico.
Eficiência no Setor de TI vs. Setores Administrativos

O que o dado diz: O setor de IT tem uma média de R$ 5.760,00, aproximando-se das médias mais baixas como *Shipping* (R$$ 5.760,00, aproximando-se das médias mais baixas como *Shipping* (R$ 4.426,67) e Administration (R$ 4.400,00).
Insight: Para um setor que geralmente exige alto nível técnico, a média salarial de TI nesta base de dados está surpreendentemente próxima à do suporte administrativo. Pode valer a pena investigar se as posições de TI mapeadas nesta consulta específica são predominantemente de suporte básico (help desk) ou se há uma defasagem de mercado na remuneração dos desenvolvedores/analistas.
Departamentos de Alto Valor Agregado com Equipes Enxutas

O que o dado diz: Setores como Sales (R$ 10.298,27) e *Accounting* (R$$ 10.298,27) e *Accounting* (R$ 10.154,00) mantêm salários médios altos.
Insight: Finanças, Vendas e Contabilidade apresentam uma valorização robusta, possivelmente ligada à responsabilidade direta sobre receitas e conformidade fiscal. Manter equipes qualificadas e enxutas nesses setores garante controle de riscos financeiros e fomento de novas receitas.
