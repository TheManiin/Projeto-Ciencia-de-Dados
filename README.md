# Projeto Integrado de Ciência de Dados – Previsão de Vendas no Mercado Editorial

Este projeto foi desenvolvido como Projeto Integrado do curso de Análise e Desenvolvimento de Sistemas, envolvendo conceitos de Ciência de Dados e Machine Learning.

O objetivo principal foi realizar a previsão de vendas a partir de um conjunto de dados real, aplicando técnicas de análise exploratória, pré-processamento e modelagem preditiva.

O trabalho foi muito elogiado, principalmente pela profundidade da análise exploratória e pela comparação entre diferentes algoritmos de machine learning.

# Objetivo

Desenvolver modelos de regressão capazes de prever o volume de vendas de livros, utilizando como proxy a variável:

`work_text_reviews_count` (quantidade de resenhas textuais)

O projeto busca identificar padrões e fatores que influenciam o desempenho comercial de livros no mercado editorial.

# Dataset

O dataset utilizado contém informações de livros obtidas da plataforma Goodreads, incluindo:

Autores

Ano de publicação

Avaliações médias

Quantidade de avaliações por nota (1 a 5)

Idioma

Número de avaliações e resenhas

Metadados editoriais

## Principais variáveis utilizadas

`ratings_count`

`average_rating`

`original_publication_year`

`ratings_1 a ratings_5`

`language_code`

`authors`

# Tratamento e Pré-processamento dos Dados

As seguintes etapas foram realizadas para garantir a qualidade dos dados:

Identificação e tratamento de valores ausentes

Conversão de tipos de dados (ex.: `ano de publicação`)

Preenchimento de valores nulos com média ou valores padrão

Remoção de colunas irrelevantes (ISBN, URLs de imagens)

Codificação de variáveis categóricas com One-Hot Encoding

Seleção manual de features relevantes

Análise Exploratória de Dados (EDA)

# A análise exploratória incluiu:

Distribuição das vendas `(work_text_reviews_count)`

Relação entre:

Avaliações e vendas

Ano de publicação e vendas

Idioma e vendas

Autores e desempenho comercial

Análise dos Top 50 autores

Tendências temporais no mercado editorial

Boxplots, histogramas, gráficos de dispersão e barras

Essas análises permitiram extrair insights relevantes sobre o comportamento do mercado editorial.

# Modelos de Machine Learning

Apesar do requisito mínimo ser o uso de apenas um algoritmo, foram utilizados três modelos, com o objetivo de comparar desempenho e robustez:

- Regressão Linear (OLS)

Modelo base (baseline)

Utilizado para comparação inicial

`Resultados:`

R² ≈ 0.53

RMSE ≈ 4554

- Random Forest Regressor

Modelo baseado em ensemble de árvores

Captura relações não lineares

`Resultados:`

R² ≈ 0.81

RMSE ≈ 2876

MAE ≈ 1413

- XGBoost Regressor

Modelo de Gradient Boosting

Melhor desempenho geral do projeto

`Resultados:`

R² ≈ 0.83

RMSE ≈ 2768

MAE ≈ 1336

`Também foram realizadas:`

Análise de importância das features

GridSearchCV para ajuste de hiperparâmetros

Validação cruzada

| Modelo           | RMSE ↓ | R² ↑ |
| ---------------- | ------ | ---- |
| Regressão Linear | ~4554  | 0.53 |
| Random Forest    | ~2876  | 0.81 |
| XGBoost          | ~2768  | 0.83 |

`O XGBoost apresentou o melhor equilíbrio entre erro e capacidade de generalização.`

# Tecnologias Utilizadas

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- Scikit-learn

- XGBoost

- Google Colab

# Conclusões

O volume de avaliações e resenhas é um forte indicativo de vendas

Modelos não lineares apresentaram desempenho significativamente superior

O XGBoost se mostrou o mais eficiente para o problema proposto

A análise exploratória foi essencial para entender o comportamento do mercado editorial

A comparação entre modelos agregou robustez e profundidade ao projeto
