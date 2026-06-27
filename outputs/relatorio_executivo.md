# Relatório Executivo – Predição de Turnover de Funcionários

## Objetivo

Este projeto teve como objetivo desenvolver um modelo de Machine Learning capaz de prever o risco de desligamento (turnover) de funcionários, identificando os principais fatores associados à saída de colaboradores e fornecendo informações que possam auxiliar o setor de Recursos Humanos na tomada de decisões.

---

## Base de Dados

Foi utilizado o conjunto de dados **IBM HR Analytics – Employee Attrition & Performance**, contendo informações de **1.470 funcionários** e **35 variáveis** relacionadas a aspectos demográficos, profissionais, financeiros e de satisfação no trabalho.

---

## Metodologia

O desenvolvimento do projeto foi dividido nas seguintes etapas:

* Análise exploratória dos dados (EDA);
* Limpeza e preparação da base;
* Conversão das variáveis categóricas por One-Hot Encoding;
* Separação dos dados em treino (80%) e teste (20%);
* Treinamento dos modelos Regressão Logística, Random Forest e XGBoost;
* Avaliação por meio das métricas Accuracy, Precision, Recall, F1-Score e ROC-AUC;
* Explicabilidade do modelo utilizando SHAP.

---

## Principais Descobertas

A análise exploratória revelou padrões importantes relacionados ao turnover:

* Funcionários que realizam horas extras apresentam maior probabilidade de desligamento.
* Funcionários solteiros apresentam maior índice de turnover.
* Cargos da área comercial, especialmente Sales Representative, possuem maior risco de saída.
* Funcionários mais jovens tendem a apresentar maior rotatividade.
* Maiores distâncias entre residência e empresa estão associadas ao aumento do risco de desligamento.

---

## Resultado dos Modelos

Foram avaliados três algoritmos de classificação.

O modelo **XGBoost Balanceado** apresentou o melhor equilíbrio entre precisão e capacidade de identificar funcionários com risco de desligamento, alcançando aproximadamente:

* Accuracy: **85,37%**
* Precision: **57,14%**
* Recall: **34,04%**
* F1-Score: **42,67%**
* ROC-AUC: **75,14%**

Embora o XGBoost original tenha obtido maior Accuracy, o modelo balanceado apresentou melhor desempenho na identificação da classe minoritária (funcionários que deixam a empresa), sendo mais adequado para aplicações de People Analytics.

---

## Principais Fatores de Turnover

A análise SHAP identificou como principais fatores associados ao risco de desligamento:

* Realização de horas extras;
* Baixa remuneração mensal;
* Ausência de Stock Options;
* Menor idade;
* Maior distância entre residência e empresa;
* Histórico de trabalho em diversas empresas;
* Baixa satisfação com o trabalho;
* Viagens frequentes.

---

## Recomendações

Com base nos resultados obtidos, recomenda-se que o setor de Recursos Humanos:

* Monitore colaboradores que realizam horas extras com frequência;
* Desenvolva estratégias específicas de retenção para cargos comerciais;
* Reavalie políticas de remuneração e benefícios para funcionários com maior risco;
* Promova ações voltadas ao aumento da satisfação e do equilíbrio entre vida profissional e pessoal;
* Utilize o modelo desenvolvido como ferramenta de apoio para identificação preventiva de funcionários com maior probabilidade de desligamento.

---

## Conclusão

O projeto demonstrou que técnicas de Machine Learning podem ser utilizadas com sucesso para prever o turnover de funcionários e identificar os fatores que mais influenciam essa decisão.

Além de alcançar um bom desempenho preditivo, a utilização da técnica SHAP permitiu interpretar as decisões do modelo, tornando os resultados transparentes e úteis para apoiar estratégias de retenção de talentos.

Este projeto apresenta uma solução completa de People Analytics, contemplando análise exploratória, preparação dos dados, modelagem preditiva, explicabilidade e geração de informações voltadas à tomada de decisão.
