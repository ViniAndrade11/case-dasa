# CASE VAGA ANALISTA DE DADOS SR - DASA

Este repositório contém as etapas de tratamento e preparação da base de dados de headcount fornecida no case do processo seletivo.


## Estrutura do repositório

├── base_headcount.csv # Base original fornecida
├── glossario.csv # Dicionário das colunas com tipo, descrição, tratamento e normalização
├── readme.md # Documentação do projeto
├── tratamento_dados_criacao_glossario.ipynb # Notebook com o processo de tratamento da base e geração do glossário


## Etapas realizadas até o momento

- Carregamento da base original `base_headcount.csv`
- Verificação dos tipos de dados com `df.info()` e `df.describe()`
- Conversão das colunas de data para o formato `datetime`
- Correção de valores inválidos (ex: datas anteriores à data de contratação)
- Verificação de consistência entre colunas relacionadas
- Geração de um glossário contendo:
  - Nome da coluna
  - Tipo de dado
  - Descrição do campo
  - Tratamento de erros ou dados faltantes
  - Normalização aplicada (se aplicável)


## Glossário

O glossário está salvo no arquivo `glossario.csv`.  
Ele documenta todas as colunas da base original, com informações importantes para facilitar a leitura e a modelagem dos dados.


## Próximas etapas

- Separar a base em tabelas menores utilizando conceitos de modelagem fato/dimensão
- Gerar arquivos separados como:
  - `tabela_fato_funcionario.csv`
  - `tabela_dim_funcionario.csv`
  - `tabela_dim_contrato.csv`
- Atualizar este README com a explicação da estrutura final das tabelas e lógica de modelagem aplicada
- Criar um dashboard com os principais indicadores


## Execução

Todos os passos descritos estão documentados no notebook:

> [`tratamento_dados_criacao_glossario.ipynb`](./tratamento_dados_criacao_glossario.ipynb)



## Considerações finais

Todas as alterações foram registradas em commits no repositório, com mensagens descritivas para acompanhamento da evolução do projeto.

Este processo garante rastreabilidade e organização, como solicitado no case.


