# Vehicle Price prediction

O objetivo do projeto é criar um modelo de Machine Learning para prever o preço de venda do veículo, considerando algumas características do carro.

O Dataset "cardata.csv" pode ser encontrado no Kaggle e contém informações sobre carros usados. As informações são do site cardekho.com

## Resumo do projeto e considerações

### Análise e transformação dos dados

Inicialmente foi feita breve análise dos dados com o objetivo de identificar possíveis OUTLIERS e variáveis indesejadas.
Também foi realizada a transformação das features categóricas em variável numérica, para que o algoritmo consiga reconhecer os dados e ter mais eficiência nas previsões. O método escolhido nestas transformações foi o **One Hot Encoder** (Dummies).
Utilizou-se também um HeatMap(mapa de calor) para identificar possíveis correlações entre variáveis. Após esse processo foi possível perceber que trata-se de um problema de **Regressão Linear**.

### Divisão dos dados

Antes de treinar e escolher o melhor modelo preditivo, foi realizada a **normalização dos dados** com o intuito de corrigir alguns outliers. Depois de normalizados, os dados foram divididos em dados de treinamento e dados de teste através do método **train_test_split**.

### Treinamento e teste do modelo

Inicialmente os dados foram treinados e validados com o algoritmo **Linear Regression**, gerando um score de mais de 85%.

Posteriormente, os dados foram treinados e testados com o algoritmo **Random Forest Regressor**. Durante a implementação do modelo foi realizada uma **otimização de hiperparâmetros** através do algoritmo **Random SearchCV**, buscando obter os melhores hiperparâmetros e a máxima performance do Random forest Regressor.

Por fim, concluiu-se que o melhor modelo para este problema é o **Random Forest Regressor**, que obteve um score de 87%.