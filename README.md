# 🚗🌱 Análise de Locações de Veículos e Emissões de CO₂

Este projeto foca na **limpeza, tratamento e consolidação de dados** provenientes de diferentes fontes (**CSV e JSON**) relacionadas à **locação de veículos**, **clientes** e **métricas ambientais**.

O objetivo principal é transformar **dados brutos** em uma **base consolidada**, pronta para análises de **faturamento** e **impacto ambiental**, com foco em emissões de CO₂.

---

## 📌 Funcionalidades do Projeto

O script executa as seguintes etapas de processamento de dados:

### 🔹 Ingestão de Dados
- Leitura de múltiplos formatos de arquivos (`.csv` e `.json`).

### 🔹 Limpeza de Dados (Data Cleaning)
- Tratamento de valores ausentes:
  - Imputação da média para idade.
  - Valores fixos para emissões de CO₂ quando ausentes.
- Correção de tipos de dados:
  - Conversão de campos de texto para valores numéricos.
- Padronização de datas:
  - Tratamento de formatos inconsistentes.
- Identificação e correção de valores negativos incoerentes:
  - Ajustes em taxas diárias de locação.

### 🔹 Engenharia de Dados (Feature Engineering)
- Cálculo da **duração das locações** (em dias).
- Cálculo da **receita total por contrato**.
- Cálculo da **emissão total de CO₂ por viagem**, com base na distância percorrida e no modelo do veículo.
- Extração de variáveis temporais:
  - Ano
  - Mês
  - Dia da semana

### 🔹 Consolidação dos Dados (Data Merge)
- União das tabelas de **locações**, **veículos** e **clientes** em um **dataset único e unificado**.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Pandas** — Manipulação, limpeza e transformação de dados
- **NumPy** — Operações matemáticas e suporte a tipos de dados

---

## 📂 Estrutura dos Dados

- **customers_data.csv** — Perfil dos clientes e score de fidelidade  
- **carbon_offsets.csv** — Custos de compensação de carbono por ano  
- **rentals_data.json** — Registro detalhado das locações  
- **vehicles_data.json** — Catálogo de veículos e emissões
