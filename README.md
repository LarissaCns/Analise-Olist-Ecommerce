# 📊 Análise Estratégica de Expansão e Vendas - Olist

Este repositório contém a resolução do desafio técnico de Dados, focado em analisar o comportamento de compras do e-commerce brasileiro (Olist) e cruzar essas informações com dados demográficos oficiais do IBGE para identificar oportunidades de expansão.

## 🎯 Objetivo do Projeto
O principal objetivo desta análise é responder a perguntas de negócio estratégicas, identificando gargalos na qualidade dos dados de localização, mapeando a concentração atual de clientes e, principalmente, descobrindo quais cidades e regiões do Brasil representam os maiores investimentos de marketing.

## 🛠️ Tecnologias Utilizadas
Para garantir performance e uma sintaxe limpa, a arquitetura da análise foi dividida da seguinte forma:
* **Python & Pandas:** Ingestão de dados, tratamento de strings (Regex/Unidecode) e limpeza de dados nulos/inconsistentes.
* **DuckDB:** Utilizado para Engenharia de Dados e consultas SQL (JOINs complexos e agregações) diretamente sobre os DataFrames em memória.
* **Matplotlib & Seaborn:** Criação de gráficos estáticos com foco em storytelling executivo.
* **Plotly:** Construção de mapas geoespaciais interativos.

## 💡 Principais Insights de Negócio
1. **Qualidade de Dados:** Identificou-se uma perda de registros no cruzamento Olist-IBGE devido ao input manual de cidades no checkout (erros de digitação, uso de bairros/distritos ao invés de municípios). Recomenda-se a implementação de uma API de validação de CEP no front-end.
2. **Oportunidade de Expansão:** Ao cruzar a base de clientes com cidades de mais de 200 mil habitantes, descobrimos que **100% das 10 maiores oportunidades de crescimento (baixa penetração + alta população) estão nas regiões Norte e Nordeste** do Brasil.
3. **Concentração Atual:** O mapa geoespacial confirmou a tese de saturação nas regiões Sul e Sudeste, com o eixo São Paulo-Rio de Janeiro dominando o volume de pedidos.
4. **Sazonalidade:** A análise da série temporal mostrou forte dependência de eventos sazonais (ex: Black Friday em novembro, ofuscando o mês de dezembro). 

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone <LINK_DO_SEU_REPOSITORIO_AQUI>
   pip install -r requirements.txt

   ´´´

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt

   ´´´

3. Os datasets originais não foram versionados por questões de tamanho e segurança. Baixe os dados do Kaggle e do IBGE e insira-os na pasta raiz antes de executar.

4. Abra o arquivo analises.ipynb em seu ambiente Jupyter preferido e execute as células sequencialmente.

**Desenvolvido por:** Larissa Cristina


