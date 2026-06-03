# Mini Projeto - Análise Exploratória de Dados no Varejo

## Objetivo

Este projeto tem como objetivo realizar uma Análise Exploratória de Dados (AED) em uma base de varejo, utilizando Python e Pandas para importar, limpar, transformar, analisar e interpretar os dados.

A análise busca identificar problemas de qualidade na base, compreender padrões de compra dos clientes e gerar insights úteis para decisões de negócio.

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Git e GitHub

## Estrutura do Projeto


MiniProjeto_JeanPauleti/
│
├── dados/
│   ├── Varejo.csv
│   └── df_limpo.csv
│
├── src/
│   ├── analise_varejo.py
│   └── analise_varejo.ipynb
│
├── README.md


Etapas Realizadas

1. Importação dos Dados

A base Varejo.csv foi importada com Pandas. Inicialmente, o dataframe possuía:

830.000 linhas
14 colunas

Também foram avaliados os tipos de dados, as primeiras e últimas linhas da base.

2. Diagnóstico da Qualidade dos Dados

Foram encontrados os seguintes problemas:

A coluna DATA estava como texto e precisava ser convertida para datetime.
Quatro colunas estavam completamente vazias: Unnamed: 10, Unnamed: 11, Unnamed: 12 e Unnamed: 13.
Foram identificados 96.553 registros duplicados.
Foram encontrados valores #N/D nas colunas de categoria e nome de produto.

3. Limpeza e Tratamento dos Dados

As ações de limpeza realizadas foram:

Remoção das quatro colunas totalmente vazias.
Conversão da coluna DATA para o tipo datetime.
Remoção de 96.553 registros duplicados.
Substituição de #N/D em PR_CAT por SEM CATEGORIA.
Substituição de #N/D em PR_NOME por PRODUTO NÃO IDENTIFICADO.
Padronização dos textos das colunas PR_CAT e PR_NOME em letras maiúsculas.
Exportação da base limpa como df_limpo.csv.

Após a limpeza, a base ficou com 733.447 registros.

Estatística Descritiva

Foi analisada a coluna CL_FHL, que representa a quantidade de filhos dos clientes.

Principais resultados:

Média: 1,15 filhos
Mediana: 0
Moda: 0
Mínimo: 0
Máximo: 4
Não foram encontrados outliers

A mediana e a moda iguais a zero indicam que grande parte dos clientes da base não possui filhos.

Análises Realizadas

Vendas por Dia da Semana

A análise mostrou que os dias com maior volume de vendas foram:

Quarta-feira: 135.738 vendas
Sexta-feira: 117.051 vendas
Domingo: 115.318 vendas

O sábado apresentou o menor volume de vendas.

Vendas por Gênero ao Longo da Semana

Foi criada uma tabela dinâmica para avaliar a distribuição das vendas por gênero durante os dias da semana.

A análise mostrou que as mulheres realizaram mais compras do que os homens em praticamente todos os dias analisados.

Análise por Segmentação Econômica

A coluna CL_SEG foi utilizada para avaliar o comportamento de compra por segmento econômico.

Segmento	Clientes	Compras	Itens	Itens por compra	Compras por cliente
A	         841.492	     59.677	        40,00	                17,76
B	         64511.843	    468.505	        39,56	                18,36
C	         2715.136	    205.265	        39,97	                18,95

O segmento B concentra a maior quantidade de clientes e itens comprados. Porém, o segmento C apresentou a maior média de compras por cliente.

Principais Insights

A base apresentava problemas relevantes de qualidade, incluindo 96.553 duplicatas e quatro colunas totalmente vazias.
A categoria de dados ausentes foi tratada, evitando que valores #N/D prejudicassem as análises.
A maior parte dos clientes não possui filhos, já que a mediana e a moda da coluna CL_FHL foram iguais a zero.
Quarta-feira foi o dia com maior volume de vendas.
Mulheres apresentaram maior volume de compras ao longo da semana.
O segmento econômico B representa a maior parte da base de clientes.
A média de itens por compra foi muito parecida entre os segmentos econômicos, ficando próxima de 40 itens por compra.

Reflexão sobre ETL e Qualidade dos Dados

O processo de ETL é essencial em projetos de análise de dados. Neste projeto, a etapa de extração foi realizada por meio da leitura da base Varejo.csv. Em seguida, a etapa de transformação envolveu a remoção de colunas vazias, tratamento de valores ausentes, padronização de textos, conversão de datas e remoção de duplicatas.


Como Executar o Projeto

Instale as dependências:

pip install pandas numpy matplotlib

Execute o script principal:

python src/analise_varejo.py

Ou abra o notebook:

src/analise_varejo.ipynb

e execute as células em sequência.

Autor
Jean Pauleti