# 🛒 Projeto: Previsão de Intenção de Compra Online

## Sobre o Projeto

O objetivo central foi desenvolver um modelo preditivo capaz de analisar padrões de
comportamento de clientes de um e-commerce e identificar sinais que indicam a propensão
deles para realizar compras online. Mais do que um exercício técnico, trata-se de uma
ferramenta com impacto direto no negócio: campanhas de marketing mais inteligentes,
experiências personalizadas e melhor alocação de recursos.

## 🔬 Metodologia

O projeto foi conduzido em etapas bem definidas, seguindo as boas práticas de um
pipeline de Machine Learning:

**Preparação dos Dados:** A base passou por um processo rigoroso de limpeza, com
remoção de 201 registros duplicados, tratamento de 24 valores ausentes na coluna de
renda, identificação e remoção de idades implausíveis e aplicação de cap nos outliers
de renda com base nos percentis 1% e 99%.

**Análise Exploratória (EDA):** Com foco no comportamento dos canais de compra, foram
construídas visualizações que revelaram padrões relevantes: clientes mais jovens e de
renda mais alta tendem a comprar online com maior frequência, enquanto o engajamento
digital, medido pelo número de visitas ao site por mês, mostrou forte relação com a
conversão no canal web.

**Pré-processamento:** As variáveis categóricas foram transformadas com estratégias
adequadas a cada tipo: Ordinal Encoding para escolaridade e faixas ordenadas, e
One-Hot Encoding para estado civil. Em seguida, a base foi dividida em conjuntos de
treino (80%) e teste (20%), com estratificação para preservar a proporção das classes.
Por fim, foi aplicado o RobustScaler na padronização, escolhido por sua resistência
a outliers residuais nas variáveis de renda e gastos.

**Modelagem:** Dois algoritmos foram selecionados e treinados: Random Forest e XGBoost,
ambos baseados em árvores de decisão e reconhecidos pela robustez em dados tabulares.
Ambos foram configurados para lidar com o desbalanceamento entre as classes.

**Avaliação:** Os modelos foram comparados com métricas completas — Accuracy, Precision,
Recall, F1-Score e ROC-AUC, além de análise das matrizes de confusão e das curvas ROC
e Precision-Recall.

---

## 🏆 Resultados

Ambos os modelos apresentaram desempenho excelente, com resultados muito próximos entre
si. O XGBoost foi eleito o modelo final, com **93,68% de Accuracy** e **ROC-AUC de
0,9786**, mas o diferencial decisivo foi o **Recall de 97%** para a classe Web, o que
significa que o modelo é capaz de identificar corretamente 97 de cada 100 clientes com
propensão a comprar online.

Esse resultado é especialmente relevante do ponto de vista de negócio: em campanhas de
marketing, deixar de identificar um comprador potencial (falso negativo) é geralmente
mais custoso do que abordar um não-comprador e o XGBoost minimiza exatamente esse
tipo de erro.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** e **NumPy** — manipulação e análise de dados
- **Matplotlib** e **Seaborn** — visualizações estáticas
- **Plotly** — visualizações interativas
- **Scikit-learn** — pré-processamento, modelagem e avaliação
- **XGBoost** — algoritmo de gradient boosting

