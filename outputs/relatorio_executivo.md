# Relatório Executivo

## Projeto: Predição de Turnover de Funcionários com Machine Learning

## Visão Geral

Este projeto teve como objetivo desenvolver um modelo de Machine Learning capaz de prever o desligamento de funcionários (turnover), utilizando técnicas de análise exploratória de dados, pré-processamento, modelagem preditiva e explicabilidade.

O trabalho foi desenvolvido utilizando Python e bibliotecas amplamente empregadas em projetos de Ciência de Dados, como Pandas, Scikit-Learn, XGBoost e SHAP.

---

# Dataset

Foi utilizado o conjunto de dados **IBM HR Analytics – Employee Attrition & Performance**, contendo informações de **1.470 funcionários** e variáveis relacionadas ao perfil profissional, remuneração, satisfação no trabalho e histórico de carreira.

---

# Etapas do Projeto

O projeto foi dividido nas seguintes fases:

* Carregamento e entendimento dos dados;
* Análise Exploratória (EDA);
* Limpeza e preparação da base;
* Codificação das variáveis categóricas (One-Hot Encoding);
* Separação dos conjuntos de treino e teste;
* Treinamento e comparação de modelos de Machine Learning;
* Explicabilidade utilizando SHAP;
* Geração de um ranking de risco de turnover.

---

# Modelos Avaliados

Foram treinados e comparados três algoritmos supervisionados:

* Regressão Logística
* Random Forest
* XGBoost

Também foi desenvolvida uma versão balanceada do XGBoost para melhorar a identificação da classe minoritária.

Após a comparação das métricas, o **XGBoost Balanceado** foi selecionado como modelo final por apresentar o melhor equilíbrio entre precisão e capacidade de identificar funcionários com risco de desligamento.

### Resultado do modelo selecionado

* Accuracy: **85,37%**
* Precision: **57,14%**
* Recall: **34,04%**
* F1-Score: **42,67%**
* ROC-AUC: **75,14%**

---

# Principais Variáveis

A análise de importância das variáveis e os gráficos SHAP indicaram que os fatores com maior influência na previsão de turnover foram:

* Horas extras (OverTime)
* Remuneração mensal
* Stock Option Level
* Idade
* Distância entre residência e empresa
* Número de empresas anteriores
* Satisfação no ambiente de trabalho
* Frequência de viagens

Além de identificar as variáveis mais importantes, a utilização do SHAP permitiu interpretar individualmente as previsões realizadas pelo modelo.

---

# Resultado Final

Como entrega prática do projeto, foi desenvolvido um relatório contendo o ranking de risco dos funcionários pertencentes ao conjunto de teste.

O arquivo apresenta:

* Probabilidade prevista de desligamento;
* Classificação do risco em níveis Alto, Médio e Baixo.

Essa abordagem demonstra como modelos de Machine Learning podem ser utilizados para apoiar análises de People Analytics e auxiliar na identificação preventiva de colaboradores com maior probabilidade de turnover.

---

# Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* XGBoost
* SHAP
* Jupyter Notebook

---

# Considerações Finais

Este projeto permitiu aplicar na prática todo o fluxo de um projeto de Machine Learning, desde a exploração dos dados até a interpretação dos resultados.

Além da construção dos modelos preditivos, foi dada atenção à explicabilidade das decisões do algoritmo e à apresentação dos resultados em formatos úteis para análise, como gráficos, relatórios e planilhas.

O projeto foi desenvolvido com foco em organização, reprodutibilidade e boas práticas, servindo como demonstração das etapas fundamentais de um pipeline de Ciência de Dados voltado para problemas de classificação.
