# 📄 Documentação Técnica – Projeto de Turnover RH

Este documento descreve de forma objetiva todos os arquivos criados durante o desenvolvimento do projeto de análise de turnover, desde a preparação dos dados até a geração de insights visuais.


## 1. `base_dados/`

Contém as bases utilizadas no início do projeto.

### `base_headcount.csv`
- Base original com todos os dados de RH.
- Contém colunas como `gender`, `is_active`, `sick_days`, `vacation_days`, `hire_date`, `termination_date`, entre outras.

### `base_headcount_tratada.csv`
- Resultado da limpeza e padronização dos dados.
- Realizadas as substituições:
  - `gender`: male → masculino, female → feminino, others → outros
  - `is_active`: True → Ativo, False → Desligado
- Formatação de datas e padronização de tipos.


## 2. `scripts/`

Scripts Python utilizados no projeto.

### `tratamento_dados_criacao_glossario.ipynb`
- Limpeza dos dados brutos
- Substituição de valores
- Criação do glossário

### 🔹 `dimensionamento_base.ipynb`
- Segmentação da base em tabelas:
  - Tabela fato (`tabela_fato_colaborador`)
  - Tabelas dimensão: colaborador, contrato, departamento, estrutura


## `modelo_analitico/`

Modelagem de dados em formato estrela para análise no Power BI.

### Tabela Fato

#### `tabela_fato_colaborador.csv`
- Contém as principais métricas e fatos:
  - Performance
  - Tempo de contrato
  - Faltas, atrasos, férias, sick days
  - Chaves para as dimensões

### Tabelas Dimensão

#### `tabela_dim_colaborador.xlsx`
- ID do colaborador, gênero, status ativo/inativo, etc.

#### `tabela_dim_contrato.xlsx`
- Tipo de contrato, data de entrada/saída, cálculo de tempo de casa

#### `tabela_dim_departamento.xlsx`
- Nome dos departamentos

#### `tabela_dim_estrutura_organizacional.xlsx`
- Departamento de cada colaborador


## 4. Arquivos Auxiliares

### `dashboard_rh.pbix`
- Painel em Power BI com:
  - Turnover acumulado por ano
  - Comparativos por departamento e cargo
  - Ausências, férias, atrasos e tempo de contrato
  - KPIs principais do RH

### `glossario.csv`
- Dicionário de dados explicando cada coluna utilizada na base tratada e na modelagem analítica

## 5. Documentação

### `readme.md`
- Visão geral do projeto: objetivo, estrutura de pastas, instruções de uso

### `documentacao.md` *(este arquivo)*
- Explicação detalhada de cada arquivo e sua função no processo


## Observações

- Todas as transformações foram feitas de forma controlada e com versionamento via Git
- As tabelas estão organizadas para permitir escalabilidade no modelo analítico
- A separação em fato/dimensão permite integração futura com novos indicadores (ex: folha de pagamento)