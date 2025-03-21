# Previsão de Vendas de Sorvete com Machine Learning 🍦

Este projeto visa construir um modelo de Machine Learning para prever a demanda de sorvetes com base na temperatura diária. O objetivo é ajudar os proprietários de sorveterias a otimizar a produção, reduzindo desperdícios e maximizando lucros.

O modelo foi desenvolvido usando dois métodos no Azure Machine Learning: AutoML e Azure ML Designer. O projeto comparou o desempenho de ambos os métodos para prever as vendas de sorvete e avaliou as métricas de cada um.

## Objetivo 🎯

O objetivo deste projeto é prever a quantidade de sorvetes vendidos com base na temperatura do dia. A solução busca:

- Otimizar a produção de sorvetes, minimizando desperdícios.
- Maximizar os lucros, antecipando a demanda de sorvetes.

## Métodos Utilizados 🔎

### 1. AutoML

O AutoML foi utilizado para gerar um modelo preditivo com base no conjunto de dados de vendas de sorvetes e temperaturas. O algoritmo com o melhor desempenho foi o **VotingEnsemble**, que combina vários modelos para melhorar a precisão das previsões.

#### Métricas de Desempenho - VotingEnsemble (AutoML)

- **Variância explicada**: 0.52269  
  O modelo explicou aproximadamente 52% da variância nos dados.
  
- **Erro absoluto de média (MAE)**: 10.608  
  A média dos erros absolutos entre as previsões e os valores reais foi de 10.6 sorvetes.
  
- **Erro de percentual absoluto de média (MAPE)**: 24.524%  
  O erro médio absoluto em relação ao valor real foi de 24.5%.

- **Erro mediano absoluto (MedAE)**: 10.039  
  O erro mediano absoluto foi de 10.0 sorvetes.

- **Erro absoluto de média normalizado**: 0.14733  
  O erro normalizado em relação à escala dos dados foi 0.147.

- **Erro mediano absoluto normalizado**: 0.13943  
  O erro mediano absoluto normalizado foi de 0.139.

- **Erro de quadrado de média de raiz normalizado (NRMSE)**: 0.17111  
  O erro quadrático médio da previsão, normalizado, foi 0.171.

- **Erro de log de quadrado de média raiz normalizado (Log NRMSE)**: 0.16403  
  O erro logarítmico quadrático médio normalizado foi de 0.164.

- **Pontuação R² (Coeficiente de Determinação)**: 0.45115  
  O modelo explicou aproximadamente 45% da variação nos dados.

- **Erro de raiz do valor quadrático médio (RMSE)**: 12.320  
  O erro quadrático médio foi de 12.32 sorvetes.

- **Erro de log de raiz do valor quadrático médio (Log RMSE)**: 0.27155  
  O erro logarítmico quadrático médio foi de 0.271.

- **Correlação de Spearman**: 0.72512  
  A correlação entre as previsões e os valores reais foi moderada (0.725).

### 2. Azure ML Designer

O Azure ML Designer foi utilizado para criar e treinar o modelo de previsão de forma visual. O Designer permitiu a criação de um pipeline intuitivo e personalizável para o treinamento e avaliação do modelo, com uma comparação direta entre diferentes algoritmos.

#### Métricas de Desempenho - Modelo Designer

As seguintes métricas de desempenho foram obtidas para o modelo treinado no Azure ML Designer:

- **Erro absoluto médio (MAE)**: 10.64  
  O erro absoluto médio foi de aproximadamente 10.64 sorvetes, indicando um erro médio razoável nas previsões.

- **Erro quadrático médio (RMSE)**: 12.67  
  O RMSE foi de 12.67 sorvetes, uma métrica comum para avaliar o erro do modelo em problemas de regressão.

- **Erro quadrático relativo**: 0.508  
  O erro quadrático relativo indicou que o modelo explicou cerca de 50.8% da variabilidade dos dados, refletindo um desempenho razoável.

- **Erro absoluto relativo**: 0.709  
  O erro absoluto relativo foi de 70.9%, o que sugere uma margem considerável de erro nas previsões.

- **Coeficiente de determinação (R²)**: 0.492  
  O modelo Designer teve uma pontuação R² de 0.492, indicando que ele foi capaz de explicar 49.2% da variabilidade dos dados.

## Comparação dos Métodos 📊

Ao comparar os dois métodos, podemos observar que:

- O modelo AutoML (VotingEnsemble) obteve um desempenho ligeiramente melhor, com uma variância explicada de 52% e um R² de 0.45. Ele também apresentou uma boa correlação de Spearman (0.725), sugerindo uma relação forte entre as previsões e os valores reais.
- O modelo Designer teve um R² de 0.492, explicando aproximadamente 49.2% da variância dos dados, e teve um erro absoluto médio de 10.64, um pouco mais alto que o modelo AutoML (10.608).

## Conclusões 📑 

- **Desempenho**: Ambos os modelos apresentaram desempenho satisfatório, com erros dentro de um intervalo razoável para previsão de demanda. O modelo AutoML (VotingEnsemble) teve ligeiramente melhor desempenho devido à combinação de diferentes modelos.

- **Possíveis Aplicações**: Este modelo pode ser útil para empresas de sorvetes, ajudando na otimização de estoque e produção com base nas condições climáticas diárias, maximizando lucros e evitando desperdícios.