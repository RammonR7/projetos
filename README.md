# Censo Escolar da Rede Municipal de Fortaleza (2017-2021)

Análise exploratória de dados sobre matrículas na rede municipal de ensino de Fortaleza (CE), utilizando os microdados públicos do Censo Escolar disponibilizados pela Prefeitura de Fortaleza.

## 🎯 Objetivo

Entender como as matrículas na rede municipal evoluíram entre 2017 e 2021, identificando:
- O crescimento (ou queda) do número de alunos matriculados por ano e por nível de ensino;
- A distribuição das matrículas entre os 6 distritos de educação do município;
- As escolas com maior número de matrículas;
- O impacto da pandemia de covid-19 (2020-2021) na rede municipal.

## 🗂️ Fonte dos dados

Dados públicos e oficiais extraídos diretamente do [Portal de Dados Abertos de Fortaleza](https://dados.fortaleza.ce.gov.br/dataset/?groups=educacao), grupo Educação, referentes aos censos escolares de 2017 a 2021. A importação é feita via URL, sem necessidade de download manual.

A divisão territorial utilizada segue os [6 distritos de educação](https://educacao.sme.fortaleza.ce.gov.br/distritos-de-educacao/) definidos pela Secretaria Municipal de Educação (SME).

## 🛠️ Tecnologias utilizadas

- Python 3
- [pandas](https://pandas.pydata.org/) — leitura, limpeza e manipulação dos dados
- [matplotlib](https://matplotlib.org/) — visualização de dados
- [seaborn](https://seaborn.pydata.org/) — mapa de calor das taxas de variação

## 📊 Etapas da análise

1. **Importação** — leitura dos 5 arquivos CSV (2017-2021) direto da URL oficial;
2. **Tratamento** — unificação dos censos em um único dataframe, criação da coluna `ano`, padronização da coluna `distrito` (numérico) e remoção de valores nulos;
3. **Análise** — total de matrículas no período, taxa de variação por ano e nível de ensino, distribuição por distrito, top 10 escolas, médias e desigualdade entre distritos;
4. **Visualização** — gráfico de linha (evolução anual), heatmap (variação por nível), gráficos de barra (matrículas e escolas por distrito) e série temporal (crescimento por distrito).

## 📈 Principais achados

- O total de matrículas na rede municipal entre 2017 e 2021 foi de **1.111.867 alunos**, com crescimento positivo mesmo durante a pandemia;
- Os distritos **5 e 6** concentram o maior número de matrículas e de escolas;
- Os distritos **1, 2 e 3** têm volumes de matrícula menores e mais homogêneos entre si;
- A **pré-escola** e os primeiros anos do fundamental apresentam as maiores taxas de crescimento;
- A **EJA (Educação de Jovens e Adultos)** mantém adesão baixa e estável ao longo do período.

## ▶️ Como executar

```bash
pip install -r requirements.txt
jupyter notebook CensoEscolarFortaleza_2017_2021.ipynb
```

> Os dados são carregados diretamente das URLs públicas da Prefeitura de Fortaleza — é necessário conexão com a internet para rodar o notebook do zero.

## 📁 Estrutura do repositório

```
.
├── CensoEscolarFortaleza_2017_2021.ipynb   # notebook principal com a análise completa
├── requirements.txt                         # dependências do projeto
└── README.md
```

## 📄 Licença

Este projeto utiliza dados públicos disponibilizados pela Prefeitura de Fortaleza sob licença de dados abertos. O código deste repositório está disponível para fins de estudo e portfólio.

---

Desenvolvido como projeto de análise de dados / ciência de dados aplicada à educação pública municipal.
