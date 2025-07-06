# CASE VAGA ANALISTA DE DADOS SR - DASA

Este repositório contém as etapas de tratamento e preparação da base de dados de headcount fornecida no case do processo seletivo.


## Estrutura do repositório
###  `base_dados/`
Contém os arquivos utilizados como fonte de dados:
- `base_headcount.csv` – base original fornecida
- `base_headcount_tratada.csv` – base limpa e pronta para análise

### `scripts/`
Scripts Python utilizados no projeto:
- `tratamento_dados_criacao_glossario.ipynb` - Limpeza, transformação dos dados e criação do glossário
- `dimensionamento_base.ipynb` - Geração das tabelas fato e dimensão
- `analise_dados.ipynb` - Analise inicial de correlação

###  `modelo_analitico/`
#### Tabela Fato
Modelagem analítica com:
- `fato_turnover.csv`
Contém os fatos e métricas principais como:
  - Turnover
  - Tempo de contrato
  - Número de ausências
  - Headcount
  - Chaves para as tabelas de dimensão

#### Tabelas de Dimensão
- `tabela_dim_colaborador.csv` – dados cadastrais e status do colaborador
- `tabela_dim_contrato.csv` – tipo e datas de contrato
- `tabela_dim_departamento.csv` – dados organizacionais dos departamentos
- `tabela_dim_estrutura_organizacional.csv` – níveis e estrutura hierárquica da empresa


## Arquivos de Entrega

- `dashboard_rh.pbix` – Dashboard em Power BI com indicadores de turnover, ausências e estrutura organizacional
- `glossario.csv` – Dicionário de dados explicando as colunas da base
- `readme.md` – Visão geral do repositório (este arquivo)
- `documentacao.md` – Detalhamento técnico sobre os arquivos do projeto


## Objetivo do Projeto

- Realizar análise de turnover com base em dados reais de RH
- Identificar padrões de absenteísmo, tempo de casa, e carga de trabalho
- Construir modelo de dados com tabelas fato e dimensão
- Gerar insights visuais por meio de dashboard gerencial

## Considerações finais

Todas as alterações foram registradas em commits no repositório, com mensagens descritivas para acompanhamento da evolução do projeto.

Este processo garante rastreabilidade e organização, como solicitado no case.

## Próximos Passos

- Desenvolver um painel adicional com dados de **folha de pagamento**, integrando métricas financeiras por colaborador.
- Criar um **modelo de machine learning** para prever **possíveis turnovers futuros**, utilizando variáveis históricas como absenteísmo, tempo de casa, horas extras, entre outras.

## Tecnologias Utilizadas

- Python (Pandas, NumPy)
- Jupyter Notebook
- Power BI
- Git + GitHub



