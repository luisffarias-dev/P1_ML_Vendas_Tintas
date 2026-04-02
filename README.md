# Avaliação de Machine Learning – Previsão de Vendas

## Autor
Aluno: Luis Fernando Franças Farias e Ryan Pereira Da Mota  
Professor: Bruno  

---

## Objetivo

O objetivo deste projeto é prever as vendas futuras de produtos de uma loja de tintas utilizando regressão linear simples, com base nos dados históricos do ano de 2023.

---

## Tipo de Análise

A análise realizada é do tipo **supervisionada**, pois utilizamos dados históricos com valores conhecidos (meses e vendas) para treinar o modelo e realizar previsões futuras.

---

## Base de Dados

A base contém dados mensais de vendas dos seguintes produtos:

- Tinta Acrílica  
- Tinta Esmalte  
- Tinta Látex  
- Tinta Spray  
- Tinta PVA  

Variáveis utilizadas:

- Mês (X)  
- Vendas (Y)  

---

## Metodologia

### Implementação Manual da Regressão Linear

A regressão linear foi implementada manualmente em Python, sem uso de bibliotecas prontas como scikit-learn.

Foi utilizada a fórmula da reta:

y = ax + b

Onde:

- a (inclinação) foi calculado por:

a = (n * Σ(xy) - Σx * Σy) / (n * Σ(x²) - (Σx)²)

- b (coeficiente linear):

b = (Σy - a * Σx) / n

---

### Cálculo do R²

O coeficiente de determinação também foi calculado manualmente:

R² = 1 - (Σ(y - ŷ)² / Σ(y - ȳ)²)

Onde:

- ŷ = valor previsto  
- ȳ = média das vendas  

---

## Resultados das Análises

### 1. Análise Geral dos Dados

**Estatísticas descritivas:**
- Total de registros: 50
- Soma total de vendas: 9,485 unidades
- Média de vendas mensais: 189.7 unidades
- Período analisado: Janeiro a Dezembro de 2023

**Cálculos realizados:**

Soma dos meses (Σx): 1,275
Soma das vendas (Σy): 9,485
Soma dos meses² (Σx²): 42,925
Soma das vendas² (Σy²): 2,257,625
Soma dos produtos (Σxy): 265,735
Quantidade de registros (n): 50

**Equação geral da reta (todos os produtos):**
a = 4.36
b = 113.28
Equação: y = 4.36x + 113.28


**Previsões gerais:**
- Mês 13 (Janeiro/2024): 169.96 unidades
- Mês 14 (Fevereiro/2024): 174.32 unidades
- Mês 15 (Março/2024): 178.68 unidades

---

### 2. Análise por Produto

#### Tinta Acrílica
- **Coeficiente angular (a):** 19.86
- **Coeficiente linear (b):** 99.09
- **R²:** 0.8264 (bom ajuste)
- **Tendência:** Crescimento
- **Previsões 2024:**
  - Janeiro: 357.27 unidades
  - Fevereiro: 377.13 unidades
  - Março: 396.99 unidades
- **Vendas por trimestre (previstas):**
  - Trimestre 1: 399.00
  - Trimestre 2: 624.00
  - Trimestre 3: 648.00
  - Trimestre 4: 1,014.00

#### Tinta Esmalte
- **Coeficiente angular (a):** 10.36
- **Coeficiente linear (b):** 74.11
- **R²:** 0.9576 (excelente ajuste)
- **Tendência:** Crescimento
- **Previsões 2024:**
  - Janeiro: 208.79 unidades
  - Fevereiro: 219.15 unidades
  - Março: 229.51 unidades
- **Vendas por trimestre (previstas):**
  - Trimestre 1: 276.00
  - Trimestre 2: 408.00
  - Trimestre 3: 498.00
  - Trimestre 4: 576.00

#### Tinta Látex
- **Coeficiente angular (a):** 10.00
- **Coeficiente linear (b):** 208.00
- **R²:** 0.9620 (excelente ajuste)
- **Tendência:** Crescimento
- **Previsões 2024:**
  - Janeiro: 338.00 unidades
  - Fevereiro: 348.00 unidades
  - Março: 358.00 unidades
- **Vendas por trimestre (previstas):**
  - Trimestre 1: 648.00
  - Trimestre 2: 738.00
  - Trimestre 3: 828.00
  - Trimestre 4: 918.00

#### Tinta Spray
- **Coeficiente angular (a):** 6.00
- **Coeficiente linear (b):** 61.00
- **R²:** 0.9505 (excelente ajuste)
- **Tendência:** Crescimento
- **Previsões 2024:**
  - Janeiro: 139.00 unidades
  - Fevereiro: 145.00 unidades
  - Março: 151.00 unidades
- **Vendas por trimestre (previstas):**
  - Trimestre 1: 198.00
  - Trimestre 2: 261.00
  - Trimestre 3: 309.00
  - Trimestre 4: 357.00

#### Tinta PVA
- **Coeficiente angular (a):** 10.00
- **Coeficiente linear (b):** 140.00
- **R²:** 1.0000 (ajuste perfeito - apenas 2 pontos)
- **Tendência:** Crescimento
- **Previsões 2024:**
  - Janeiro: 270.00 unidades
  - Fevereiro: 280.00 unidades
  - Março: 290.00 unidades

---

### 3. Análise por Trimestre

**Tendências identificadas:**

| Trimestre | Acrílica | Esmalte | Látex | Spray | PVA |
|-----------|----------|---------|-------|-------|-----|
| 1º Trim | 400 | 270 | 630 | 195 | 310 |
| 2º Trim | 590 | 390 | 720 | 255 | - |
| 3º Trim | 620 | 480 | 810 | 300 | - |
| 4º Trim | 950 | 570 | 900 | 360 | - |

**Padrões observados:**
- **Crescimento consistente:** Todos os produtos apresentaram crescimento ao longo do ano
- **Maior crescimento:** Tinta Acrílica (aumento de 137.5% do 1º ao 4º trimestre)
- **Menor crescimento:** Tinta Esmalte (aumento de 111% do 1º ao 4º trimestre)
- **Sazonalidade:** Pico de vendas no 4º trimestre para todos os produtos

---

### 4. Qualidade dos Modelos (R²)

| Produto | R² | Avaliação |
|---------|-----|-----------|
| Tinta PVA | 1.0000 | Perfeito (apenas 2 pontos) |
| Tinta Látex | 0.9620 | Excelente |
| Tinta Esmalte | 0.9576 | Excelente |
| Tinta Spray | 0.9505 | Excelente |
| Tinta Acrílica | 0.8264 | Bom |

**Análise da qualidade:**
- 80% dos produtos apresentaram R² > 0.9 (excelente ajuste)
- A Tinta Acrílica apresentou maior variação, mas ainda com bom ajuste (R² = 0.8264)
- Produtos com crescimento linear mais definido tiveram os melhores R²

---

## Previsões para 2024 (Primeiro Trimestre)

| Produto | Janeiro | Fevereiro | Março |
|---------|---------|-----------|-------|
| Tinta Acrílica | 357.27 | 377.13 | 396.99 |
| Tinta Esmalte | 208.79 | 219.15 | 229.51 |
| Tinta Látex | 338.00 | 348.00 | 358.00 |
| Tinta Spray | 139.00 | 145.00 | 151.00 |
| Tinta PVA | 270.00 | 280.00 | 290.00 |
| **Total** | **1,313.06** | **1,369.28** | **1,425.50** |

**Projeção de crescimento:**
- Janeiro para Fevereiro: +4.28%
- Fevereiro para Março: +4.10%
- Janeiro para Março: +8.56%

---

## Tendência dos Produtos

- **Tinta Acrílica:** crescimento com variações ao longo do ano, pico no 4º trimestre
- **Tinta Esmalte:** crescimento constante e linear
- **Tinta Látex:** crescimento linear muito bem definido
- **Tinta Spray:** crescimento gradual e consistente
- **Tinta PVA:** crescimento linear baseado em dados limitados

---

## Estrutura da Saída

A saída do programa contém:

- Produto
- Mês
- Vendas reais
- Vendas previstas (ŷ)
- R²
- Previsões por trimestre
- Gráficos de análise

---

## Tecnologias Utilizadas

- Python 3.x
- Bibliotecas: NumPy, Scikit-learn, Matplotlib, Seaborn, Pandas
- Implementação manual e automática de regressão linear
- Visualização de dados com gráficos

---

## Conclusão

A implementação da regressão linear, tanto manual quanto com bibliotecas, permitiu compreender profundamente o funcionamento do modelo e obter previsões precisas.

**Principais conclusões:**
1. Todos os produtos apresentam tendência de crescimento
2. O modelo tem excelente ajuste para a maioria dos produtos (R² > 0.95)
3. O 4º trimestre é o período de maior venda para todos os produtos
4. As previsões para 2024 indicam crescimento contínuo nas vendas
5. A Tinta Acrílica tem o maior potencial de crescimento, mas também maior variação

Os resultados mostram que é possível prever tendências de vendas com boa precisão utilizando regressão linear, especialmente quando os dados apresentam comportamento linear consistente.

---

## Observação

Este projeto utiliza tanto implementação manual quanto bibliotecas de machine learning para comparação e validação dos resultados.
