# Predição de Câncer de Mama
Fonte: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
## Informações:
A base de dados na qual foram criados os modelos de classificação, refere-se a conjunto de dados de câncer de mama Wisconsin, onde apresentasse Número de identificação, Diagnóstico (M = maligno, B = benigno), raio (média das distâncias do centro aos pontos no perímetro), textura (desvio padrão dos valores da escala de cinza), perímetro, área, suavidade (variação local nos comprimentos dos raios), compacidade (perímetro^2 / área - 1,0), concavidade (severidade das porções côncavas do contorno), pontos côncavos (número de porções côncavas do contorno), simetria e dimensão fractal ("aproximação da linha costeira" - 1).
## Objetivo:
O objetivo dos modelos era prever se o câncer vai ser maligno ou Benigno de Acordo com as características apresentadas acima.
## Modo de Execução:
Foi criado 3 modelos de Machine Learning, cada um com um algoritmo diferente, afim de que pudéssemos avaliar qual seria o melhor modelo, de acordo com os seus respectivos resultados. Os algoritmos utilizados foram: GaussianNB, DecisionTreeClassifier e RandomForestClassifier. Foi inicialmente executada uma EDA (Análise Exploratória dos Dados) para verificarmos como os dados estavam, se existia dados nulos, dados faltantes, outliers, se era uma distribuição normal, entre outros aspectos. Em seguida, foi feito a limpeza e tratamento desses dados para que pudéssemos trabalhar com eles. Após isso, separamos os dados e padronizamos eles devido a grande diferença entre as escalas dos valores. Criamos o modelo, treinamos e na sequencia testamos. Após isso, foi feita a avaliação de cada modelo.
## Resultados
### GaussianNB
ACURÁCIA:	0.90625\
PRECISÃO:	0.9272727272727272\
RECALL:		0.864406779661017\
F1 SCORE:	0.8947368421052632

### DecisionTreeClassifier
ACURÁCIA:	0.859375\
PRECISÃO:	0.8867924528301887\
RECALL:		0.7966101694915254\
F1 SCORE:	0.8392857142857143

### RandomForestClassifier
ACURÁCIA:	0.8984375\
PRECISÃO:	0.9107142857142857\
RECALL:		0.864406779661017\
F1 SCORE:	0.8869565217391304

## Conclusão
Com base nos dados dos modelos apresentados acima e também nos que estão presentes nos scripts, conclui que o melhor modelo é o que utiliza o algoritmo do GaussianNB. O modelo teve uma acurácia de 90.62% (Taxa de Assertividade) e um recall de 86.44%, um fator importante, pois nesse modelo queremos que ele não tenha muitos falsos negativos, em outras palavras, que o câncer seja maligno e ele diga que é benigno.
