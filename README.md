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

## Previsões

Foram feitas previsões para:

- Mês 13  
- Mês 14  
- Mês 15  

Essas previsões foram calculadas substituindo os valores de X na equação da reta obtida para cada produto.

---

## Análise por Trimestre

Os dados foram agrupados em:

- 1º trimestre (meses 1–3)  
- 2º trimestre (meses 4–6)  
- 3º trimestre (meses 7–9)  
- 4º trimestre (meses 10–12)  

As vendas foram somadas para identificar padrões de crescimento.

---

## Resultados

### Tendência dos Produtos

- Tinta Acrílica: crescimento com variações ao longo do ano  
- Tinta Esmalte: crescimento constante  
- Tinta Látex: crescimento linear bem definido  
- Tinta Spray: crescimento gradual  
- Tinta PVA: poucos dados disponíveis  

---

### Qualidade do Modelo

Os valores de R² indicaram que:

- A maioria dos produtos apresentou boa previsibilidade  
- Produtos com crescimento mais linear tiveram R² mais alto  
- O modelo se ajusta melhor a dados com menos variação  

---

## Estrutura da Saída

A saída do programa contém:

- Produto  
- Mês  
- Vendas reais  
- Vendas previstas (ŷ)  
- R²  

---

## Tecnologias Utilizadas

- Python  
- Implementação manual de regressão linear  
- Estruturas básicas (listas, loops, cálculos matemáticos)  

---

## Conclusão

A implementação manual da regressão linear permitiu compreender profundamente o funcionamento do modelo.

Os resultados mostram que é possível prever tendências de vendas com boa precisão utilizando métodos simples, especialmente quando os dados apresentam comportamento linear.

---

## Observação

Este projeto não utiliza bibliotecas de machine l
