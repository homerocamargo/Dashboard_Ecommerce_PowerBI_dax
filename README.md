# Dashboard de E-commerce com Power BI

## Sobre o projeto

Este projeto foi desenvolvido como parte do desafio de projeto da **DIO**, com o objetivo de modelar e analisar dados de vendas utilizando o **Power BI**.

A partir da base **Financials**, foi construído um modelo de dados baseado no conceito de **Star Schema**, com criação de tabelas dimensão e fato, tratamento dos dados utilizando Power Query e desenvolvimento de indicadores utilizando DAX.

## Objetivos

* Criar um modelo de dados organizado em Star Schema;
* Separar tabelas de dimensão e fato;
* Criar uma dimensão calendário utilizando DAX;
* Desenvolver medidas para análise de vendas e lucro;
* Criar um dashboard interativo para análise dos resultados;
* Praticar conceitos de modelagem de dados e visualização no Power BI.

## Estrutura do modelo

O modelo foi desenvolvido a partir da tabela original `Financials_origem`, utilizada como backup dos dados.

### Tabelas criadas

* `D_Produtos`
* `D_Produtos_Detalhes`
* `D_Descontos`
* `D_Detalhes`
* `D_Calendário`
* `F_Vendas`
* `Financials_origem`

A tabela `F_Vendas` funciona como tabela fato, enquanto as demais tabelas fornecem informações de dimensão e detalhamento para as análises.

## Modelo Star Schema

O modelo foi estruturado para que a tabela `F_Vendas` fique no centro do relacionamento, recebendo filtros das tabelas dimensão.

A dimensão calendário foi relacionada à tabela fato por meio do campo `Date`, enquanto a dimensão de produtos foi relacionada utilizando `ID_produto`.

## Tratamento dos dados

O tratamento foi realizado utilizando o **Power Query**.

Entre as principais etapas realizadas estão:

* Criação de consultas de referência a partir da tabela original;
* Seleção das colunas necessárias para cada tabela;
* Remoção de duplicidades;
* Criação de índices para identificação dos produtos;
* Agrupamento de informações para obtenção de médias, medianas, valores máximos e mínimos;
* Mesclagem de consultas;
* Organização dos tipos de dados;
* Criação da tabela fato de vendas.

## Dimensão Calendário

A tabela `D_Calendário` foi criada utilizando a função DAX `CALENDAR()`.

Também foram criadas colunas auxiliares para:

* Ano
* Mês
* Nome do mês
* Ano/Mês
* Trimestre
* Dia.

Essas informações permitem realizar análises temporais no dashboard.

## Principais funções DAX utilizadas

### CALENDAR()

Utilizada para criação da dimensão calendário.

### SUM()

Utilizada para calcular totais de vendas, lucro e unidades vendidas.

### AVERAGE()

Utilizada para calcular médias.

### MAX()

Utilizada para identificar o maior valor de venda.

### MIN()

Utilizada para identificar o menor valor de venda.

### COUNTROWS()

Utilizada para contar registros da tabela fato.

### DIVIDE()

Utilizada no cálculo da margem de lucro, evitando problemas de divisão por zero.

### YEAR(), MONTH() e FORMAT()

Utilizadas na criação e organização das informações da dimensão calendário.

## Indicadores do dashboard

O dashboard apresenta os principais indicadores:

* Total de Vendas
* Total de Lucro
* Total de Unidades Vendidas
* Margem de Lucro

Também foram criadas visualizações para análise de:

* Vendas por produto
* Lucro por segmento
* Evolução das vendas ao longo do tempo
* Vendas por país
* Discount Band.

## Dashboard

O dashboard foi desenvolvido com foco em uma visualização simples e interativa, utilizando cartões, gráficos e segmentações de dados.

Os filtros permitem analisar os resultados por:

* Ano
* Produto
* País
* Segmento
* Discount Band.

## Ferramentas utilizadas

* Microsoft Power BI
* Power Query
* DAX
* GitHub

## Arquivos do projeto

* `Dashboard_Ecommerce.pbix` — arquivo do projeto desenvolvido no Power BI.
* `modelo-estrela.png` — imagem do modelo de dados em Star Schema.
* `README.md` — documentação do projeto.

## Projeto

Projeto desenvolvido para o de estudo e criação de portfólio durante a formação da **DIO** com foco em aprendizado de Power BI, modelagem de dados, Power Query e DAX.
