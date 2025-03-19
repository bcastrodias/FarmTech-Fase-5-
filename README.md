# FarmTech-Fase-5- # 📊 **Previsão do Rendimento das Safras com Machine Learning**

Este repositório contém um projeto que utiliza diferentes algoritmos de **Machine Learning** para prever o **rendimento das safras** com base em variáveis climáticas. O objetivo é comparar cinco modelos preditivos: **Regressão Linear**, **SVM**, **Random Forest**, **Decision Tree** e **XGBoost**, avaliando seu desempenho com **validação cruzada** e diversas métricas de erro.

---

## 🚀 **Estrutura do Repositório**

1. **Introdução**
2. **Carregamento e Preparação dos Dados**
3. **Análise Exploratória de Dados (EDA)**
4. **Pré-processamento de Dados**
5. **Treinamento e Avaliação dos Modelos**
6. **Comparação de Modelos**
7. **Conclusões**

---

## 📋 **Passo a Passo do Jupyter Notebook**

### 1. **Introdução**
   O objetivo deste trabalho é prever o **rendimento das safras** com base em variáveis climáticas como **precipitação**, **temperatura** e **umidade**. O projeto explora a utilização de cinco modelos de **Machine Learning** para prever esse rendimento e comparar seus desempenhos.

### 2. **Carregamento e Preparação dos Dados**
   O primeiro passo é o **carregamento dos dados**. Os dados climáticos e de rendimento das safras foram carregados em um **DataFrame** do **Pandas**. Em seguida, os dados passaram por uma análise inicial para verificar **valores faltantes** ou **inconsistências**.

---

### 3. **Análise Exploratória de Dados (EDA)**
   Após o carregamento, a **análise exploratória** foi realizada para entender as **características** dos dados. A **EDA** inclui:
   - **Estatísticas descritivas**: Foram calculadas **média**, **desvio padrão**, **mínimos**, **máximos** e os **quartis** de cada variável, como **precipitação**, **umidade**, **temperatura** e **rendimento**.
   - **Correlação entre variáveis**: Foi calculada a **matriz de correlação** para verificar como as variáveis se relacionam entre si. A análise revelou que **precipitação** e **umidade** estavam mais fortemente correlacionadas com outras variáveis, mas **rendimento** teve baixa correlação com as variáveis climáticas, sugerindo que outros fatores podem influenciar o desempenho das safras.
   
---

### 4. **Pré-processamento de Dados**
   Após a análise inicial, os dados foram preparados para o treinamento dos modelos. As etapas de **pré-processamento** incluem:
   - **Escalonamento das Variáveis**: Foi utilizado **StandardScaler** para padronizar os dados e garantir que todas as variáveis tivessem a mesma escala.
   - **Divisão em Conjunto de Treinamento e Teste**: O conjunto de dados foi dividido em **80%** para treinamento e **20%** para teste utilizando a função **train_test_split** do **sklearn**.

---

### 5. **Treinamento e Avaliação dos Modelos**
   Cinco algoritmos de **Machine Learning** foram treinados para prever o **rendimento das safras**:
   - **Regressão Linear**: Modelo simples que modela uma relação linear entre as variáveis.
   - **SVM (Support Vector Machine)**: Modelo que encontra o hiperplano que melhor separa as observações.
   - **Random Forest**: Modelo baseado em múltiplas árvores de decisão.
   - **Decision Tree**: Árvore de decisão que divide os dados em segmentos baseados nas variáveis.
   - **XGBoost**: Modelo de **boosting** que utiliza várias árvores para melhorar a precisão.
   
   Cada modelo foi avaliado com **validação cruzada** e comparado com as métricas de **RMSE**, **R²**.

---

### 6. **Comparação de Modelos**
   Após o treinamento, todos os modelos foram comparados com base nas métricas de **erro** e **capacidade explicativa**. **Random Forest** apresentou o melhor desempenho, com um **R² de 0.9999** e **RMSE baixo**, sendo o modelo mais equilibrado. A **Regressão Linear** mostrou um **R² de 1.0**, mas indicou **sobreajuste**. O modelo **SVM** teve um desempenho ruim com **R² negativo** e **RMSE muito alto**.

---

### 7. **Conclusões**
   O modelo **Random Forest** foi o mais eficaz para prever o rendimento das safras, apresentando um bom equilíbrio entre erro baixo e alta capacidade explicativa. A **Regressão Linear**, embora tenha mostrado excelentes resultados nos dados de treino, indicou **sobreajuste**, o que comprometeria a generalização para novos dados. O **SVM** não foi adequado para esse tipo de problema, dado seu desempenho insatisfatório. Os modelos **Decision Tree** e **XGBoost** também foram eficazes, mas o **Random Forest** mostrou-se mais robusto.

---



