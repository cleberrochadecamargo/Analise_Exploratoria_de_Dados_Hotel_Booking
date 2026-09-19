# 🏨 Análise Exploratória de Dados — Hotel Booking

## 📊 Sobre o projeto

Este projeto apresenta uma análise exploratória de dados de reservas hoteleiras, utilizando Python para identificar padrões relacionados às reservas e aos cancelamentos.

Além da análise exploratória, foi desenvolvido um modelo de classificação utilizando **Árvore de Decisão**, com o objetivo de prever o cancelamento das reservas.

## 🎯 Objetivos

- Explorar e compreender o conjunto de dados de reservas hoteleiras;
- Realizar o tratamento e a preparação dos dados;
- Identificar padrões relacionados aos cancelamentos;
- Analisar a distribuição das reservas por tipo de hotel;
- Avaliar a relação entre cancelamentos, antecedência da reserva e tarifa média diária;
- Analisar a origem dos hóspedes;
- Avaliar a evolução das reservas ao longo do tempo;
- Desenvolver um modelo preditivo para classificação de cancelamentos.

## 🛠️ Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Jupyter Notebook

## 🧹 Tratamento e preparação dos dados

Durante o tratamento dos dados foram realizadas as seguintes etapas:

- Identificação de valores nulos;
- Tratamento dos valores ausentes nas colunas `children` e `country`;
- Remoção da coluna `company` devido ao elevado percentual de valores nulos;
- Identificação e remoção de registros duplicados;
- Conversão das informações de data para o formato `datetime`;
- Identificação de possíveis outliers na variável `adr`.

Foram identificados **32.001 registros duplicados**, que foram removidos antes das análises.

## 🔎 Análise Exploratória de Dados

Foram realizadas análises envolvendo:

### 🏨 Tipo de hotel

Análise da distribuição das reservas entre os diferentes tipos de hotéis.

### ❌ Cancelamentos

Análise da quantidade e do percentual de reservas canceladas e não canceladas.

Também foi analisada a taxa de cancelamento por tipo de hotel.

### 📅 Reservas por mês

Análise da quantidade de reservas e da taxa de cancelamento ao longo dos meses.

### ⏳ Lead Time

Análise da relação entre a antecedência da reserva (`lead_time`) e a taxa de cancelamento.

Foram criadas as seguintes faixas:

- 0–30 dias
- 31–60 dias
- 61–90 dias
- 91–180 dias
- Mais de 180 dias

### 💰 ADR

Análise da relação entre a tarifa média diária (`adr`) e o cancelamento das reservas.

Os valores de ADR foram divididos em quatro grupos:

- ADR baixo
- ADR médio-baixo
- ADR médio-alto
- ADR alto

### 🌎 País de origem

Análise dos 10 países com maior número de reservas e suas respectivas taxas de cancelamento.

### 📈 Evolução das reservas

Análise da evolução da quantidade de reservas ao longo do tempo.

## 🤖 Modelagem Preditiva

Foi desenvolvido um modelo de **Árvore de Decisão (Decision Tree)** para prever o cancelamento das reservas.

### Variável-alvo

```text
is_canceled
