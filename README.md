# Predição de Doenças Cardíacas por Machine Learning

# Descrição do Projeto

Este projeto tem como objetivo desenvolver um modelo de Machine Learning para prever a ocorrência de doenças cardíacas em pacientes, utilizando dados de saúde. A detecção precoce é crucial para o diagnóstico e tratamento eficazes, contribuindo para a melhoria da saúde cardiovascular.

# Funcionalidades

•
Coleta e Análise de Dados: Carregamento do dataset heart_disease_data.csv e análise exploratória para entender a estrutura e as estatísticas dos dados.

•
Pré-processamento de Dados: Padronização das características para otimizar o desempenho do modelo.

•
Treinamento do Modelo: Implementação e treinamento de um modelo de Regressão Logística para classificação.

•
Avaliação de Desempenho: Medição da acurácia do modelo nos conjuntos de dados de treino e teste.

•
Sistema de Predição: Capacidade de prever a ocorrência de doenças cardíacas para novas entradas de dados.

# Tecnologias Utilizadas

•
Python

•
numpy

•
pandas

•
scikit-learn (LogisticRegression, train_test_split, accuracy_score)

# Conjunto de Dados

O conjunto de dados utilizado é o heart_disease_data.csv, que contém informações sobre pacientes e a presença de doenças cardíacas. As características incluem:

•
age: idade

•
sex: sexo (1 = masculino; 0 = feminino)

•
cp: tipo de dor no peito (valores de 0 a 3)

•
trestbps: pressão arterial em repouso (mm Hg)

•
chol: colesterol sérico (mg/dl)

•
fbs: açúcar no sangue em jejum > 120 mg/dl (1 = verdadeiro; 0 = falso)

•
restecg: resultados eletrocardiográficos em repouso (valores 0, 1, 2)

•
thalach: frequência cardíaca máxima alcançada

•
exang: angina induzida por exercício (1 = sim; 0 = não)

•
oldpeak: depressão do ST induzida por exercício em relação ao repouso

•
slope: inclinação do segmento ST de pico do exercício

•
ca: número de vasos principais coloridos por fluoroscopia (0-3)

•
thal: talassemia (1 = normal; 2 = defeito fixo; 3 = defeito reversível)

•
target: presença de doença cardíaca (1 = sim; 0 = não)

O dataset contém 303 instâncias, com 165 casos de doença cardíaca (target = 1) e 138 casos sem doença cardíaca (target = 0).

# Metodologia de Machine Learning

1. Coleta e Análise de Dados: O dataset heart_disease_data.csv é carregado. São realizadas análises para verificar o número de linhas e colunas, as primeiras 5 linhas, informações gerais sobre os dados (.info()), valores ausentes (.isnull().sum()), e a distribuição da variável alvo (.value_counts()).

2. Pré-processamento de Dados:

•
Os dados são separados em features (X) e target (Y).

•
Os dados são padronizados usando StandardScaler para garantir que todas as características numéricas tenham a mesma escala, o que é importante para algoritmos baseados em distância.



3. Divisão de Dados: O dataset é dividido em conjuntos de treino e teste usando train_test_split, com uma proporção de 80% para treino e 20% para teste, e stratify=Y para manter a proporção da variável alvo em ambos os conjuntos.

4. Treinamento do Modelo: Um modelo de Regressão Logística (LogisticRegression) é treinado com os dados de treino padronizados.

5. Avaliação do Modelo: A acurácia do modelo é calculada nos conjuntos de treino e teste para verificar o desempenho e identificar possível overfitting.

# Resultados e Avaliação

Após o treinamento e avaliação do modelo de Regressão Logística, os seguintes resultados de acurácia foram obtidos:

•
Acurácia no conjunto de treino: Aproximadamente 85.1% (0.8512)

•
Acurácia no conjunto de teste: Aproximadamente 81.9% (0.8196)

Estes resultados indicam que o modelo de Regressão Logística tem um bom desempenho na predição de doenças cardíacas, com uma acurácia razoavelmente consistente entre os conjuntos de treino e teste, sugerindo que o modelo generaliza bem para dados não vistos.

