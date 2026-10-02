# Projeto de Ingestão, Enriquecimento e Refinamento de Dados com DuckDB

Este repositório contém o primeiro projeto desenvolvido como parte das atividades da minha Pós-Graduação. O objetivo principal é estruturar um pipeline de dados simples, performático e local utilizando o **DuckDB** e **Python**, simulando as etapas clássicas de engenharia de dados: Carga (Ingestão), Transformação (Enriquecimento) e Modelagem Final (Refinamento).

## 📁 Estrutura do Repositório

O projeto está organizado da seguinte forma:

*   **`landing/`**: Pasta contendo as bases de dados brutas em formato CSV (`z0019_1.csv` e `z0019_2.csv`) com dados fictícios de produtos que servem como ponto de partida.
*   **`scripts/`**: Diretório centralizado contendo os notebooks do pipeline:
    *   `ingestao.ipynb`: Responsável pela leitura dos arquivos brutos da pasta landing e carga inicial para o banco de dados.
    *   `enriquecimento.ipynb`: Processamento intermediário, cruzamento de tabelas e limpeza preliminar dos dados.
    *   `refinamento.ipynb`: Modelagem e criação das tabelas estruturadas finais (como tabelas dimensionais de produtos) prontas para consumo e consultas analíticas.
    *   `dados_duckdb.db`: Arquivo de banco de dados relacional embarcado gerado e atualizado localmente pelo DuckDB.

## 🛠️ Tecnologias Utilizadas

*   **Python 3.13+**: Linguagem de programação base para orquestração e execução dos comandos.
*   **DuckDB**: Banco de dados OLAP embutido de alta performance, utilizado para realizar consultas SQL diretamente nos arquivos locais de forma rápida e eficiente.
*   **Jupyter Notebooks**: Ambiente utilizado para documentar e separar visualmente cada etapa do pipeline de dados.

## 📊 O que foi desenvolvido no projeto

O pipeline processa a base de dados fictícia de produtos passando por três etapas principais:

1. **Carga Inicial:** Os dados dos arquivos CSV da pasta `landing/` são lidos e carregados de forma estruturada.
2. **Transformação:** É feita a limpeza, tratamento e união das informações dos produtos.
3. **Modelagem Analítica:** Na etapa final (`refinamento.ipynb`), o código faz a modelagem e criação da tabela final de produtos (como a `dim_produtos`). Isso organiza os itens por ID, nome e valor de forma padronizada, deixando os dados estruturados e prontos para qualquer análise ou relatório.

