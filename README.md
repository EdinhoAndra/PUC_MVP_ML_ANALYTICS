# PUC_MVP_ML_ANALYTICS

# Projeto: Previsão de Movimentos do Mini-Índice Futuro com Machine Learning

## 📌 Descrição

Este projeto investiga a aplicação de modelos de **Machine Learning** na previsão da direção do **mini-índice futuro (WINFUT)** da B3.
O objetivo foi avaliar diferentes algoritmos e medir não apenas métricas clássicas de classificação, mas também o **impacto financeiro em backtests**, refletindo a utilidade prática das previsões em estratégias de trading.

---

## 🎯 Objetivos

* Construir um **baseline** com DummyClassifier para definir referência mínima de performance.
* Treinar e avaliar modelos **KNN** (com e sem PCA) e **LightGBM**.
* Implementar o método **Triple Barrier Labeling** para gerar alvos robustos.
* Testar indicadores técnicos, medidas de volatilidade e retornos defasados como features.
* Validar os modelos com **matriz de confusão, métricas clássicas (acurácia, f1-score)** e principalmente através de **backtests**.

---

## 🧩 Dataset e Features

* Dados de preços do mini-índice futuro (OHLC).
* **Alvo:** definido pelo método *triple barrier*.
* **Principais features:**

  * Indicadores de tendência: RSI (5, 10, 20, 200), RSL (5, 10, 20, 200).
  * Volatilidades: ATR(20), Parkinson, Garman-Klass, Realized Vol.
  * Retornos defasados (lags de 1 a 20).
  * Defasagens das próprias features técnicas.

---

## ⚙️ Modelos Treinados

1. **DummyClassifier (baseline)**
   
2. **KNN sem PCA**

3. **KNN com PCA**  

4. **LightGBM**  

5. **LightGBM + SHAP/Optuna**
   

## 🛠️ Tecnologias Utilizadas

* **Python 3.11**
* Bibliotecas: `pandas`, `numpy`, `scikit-learn`, `lightgbm`, `optuna`, `matplotlib`, etc...
* Backtest implementado com métricas de risco-retorno e curva de capital.
