# Mini Projeto - Análise Exploratória de Dados no Varejo

## Objetivo

Este projeto teve como objetivo realizar uma Análise Exploratória de Dados (AED) em uma base de varejo, aplicando técnicas de limpeza, transformação e análise de dados com Python.

A análise buscou identificar problemas de qualidade dos dados, compreender padrões de compra dos clientes e gerar insights relevantes para o negócio.

---

## Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Git
* GitHub

---

## 📁 Estrutura do Projeto

```text
MiniProjeto_JeanPauleti_T2/
│
├── dados/
│   ├── Varejo.csv
│   └── df_limpo.csv
│
├── src/
│   ├── analise_varejo.ipynb
│   └── analise_varejo.py
│
├── README.md
```

---

## Limpeza dos Dados

Durante a etapa de tratamento foram identificados os seguintes problemas:

* `96.553` registros duplicados
* `4` colunas totalmente vazias
* Valores `#N/D` em categorias e produtos
* Coluna `DATA` armazenada como texto

### Tratamentos realizados

✅ Remoção de duplicatas

✅ Conversão da coluna DATA para datetime

✅ Remoção das colunas vazias

✅ Tratamento de valores ausentes

✅ Padronização dos textos em maiúsculo

Após a limpeza, a base passou de:

**830.000 registros → 733.447 registros**

---

## Estatística Descritiva

Análise da variável **CL_FHL (Quantidade de Filhos)**

| Métrica | Valor |
| ------- | ----: |
| Média   |  1,15 |
| Mediana |     0 |
| Moda    |     0 |
| Mínimo  |     0 |
| Máximo  |     4 |

### Insight

A maior parte dos clientes não possui filhos, uma vez que a mediana e a moda foram iguais a zero.

---

## Principais Análises

### Vendas por Dia da Semana

| Ranking | Dia          |  Vendas |
| ------- | ------------ | ------: |
| 1       | Quarta-feira | 135.738 |
| 2       | Sexta-feira  | 117.051 |
| 3       | Domingo      | 115.318 |

O sábado apresentou o menor volume de vendas.

---

### Distribuição das Compras por Gênero

A análise mostrou que as mulheres realizaram o número pouco maior de compras do que os homens durante praticamente toda a semana.

---

### Segmentação Econômica

| Segmento | Clientes | Compras |   Itens | Itens por Compra | Compras por Cliente |
| -------- | -------: | ------: | ------: | ---------------: | ------------------: |
| A        |       84 |   1.492 |  59.677 |            40,00 |               17,76 |
| B        |      645 |  11.843 | 468.505 |            39,56 |               18,36 |
| C        |      271 |   5.136 | 205.265 |            39,97 |               18,95 |

### Insight

* O segmento B concentra a maior quantidade de clientes.
* O tamanho médio do carrinho é semelhante entre os segmentos.

---

## Principais Insights

1. Foram identificados 96.553 registros duplicados na base.
2. A maioria dos clientes não possui filhos.
3. Quarta-feira foi o dia com maior volume de vendas.
4. A maioria das análises feitas na base de dados revela um comportamento semelhante entre a maioria dos agrupamentos.

---

## Reflexão sobre ETL e Qualidade dos Dados

O processo de ETL é fundamental para garantir a confiabilidade das análises.

Neste projeto, a etapa de transformação envolveu:

* Remoção de duplicatas;
* Tratamento de valores ausentes;
* Conversão de tipos de dados;
* Padronização de informações textuais.

Essas etapas garantiram uma base mais consistente e reduziram a possibilidade de interpretações equivocadas.

---

## Como Executar

Instale as dependências:

```bash
pip install pandas numpy matplotlib
```

Execute o notebook:

```bash
jupyter notebook
```

ou execute o script:

```bash
python src/analise_varejo.py
```

---

## 👨‍💻 Autor

**Jean Pauleti**
