# Detecção de Fraude com Cartão de Crédito

Fonte: https://www.kaggle.com/code/elvisacaciobarbosa/detec-o-de-fraude-no-cart-o-de-cr-dito/notebook

## Informações:
Há grande importância que ás empresas de cartão de crédito possam reconhecer transações fraudulentas com cartão de crédito, para que os clientes não sejam cobrados pelos itens que não compraram. A base contém transações realizadas com cartões de crédito em setembro de 2013 por portadores de cartões europeus.

## Objetivo:
O objetivo dos modelos era prever se uma transação é fraudulenta.

## Modo de Execução:
Foi criado 3 modelos de Machine Learning, cada um com um algoritmo diferente, afim de que pudéssemos avaliar qual seria o melhor modelo, de acordo com os seus respectivos resultados. Os algoritmos utilizados foram: GaussianNB, DecisionTreeClassifier e RandomForestClassifier. Foi inicialmente executada uma EDA (Análise Exploratória dos Dados) para verificarmos como os dados estavam, se existia dados nulos, dados faltantes, outliers, se era uma distribuição normal, entre outros aspectos. Em seguida, foi feito a limpeza e tratamento desses dados para que pudéssemos trabalhar com eles. Na parte de tratamento, foi feita uma estratificação dos dados devido a grande diferença entre operações fraudulentas e normais. Após isso, separamos os dados e padronizamos apenas uma coluna devido a grande diferença entre as escalas dos valores com o resto dos dados. Criamos o modelo, treinamos e na sequencia testamos. Após isso, foi feita a avaliação de cada modelo.

## Resultados

### GaussianNB
ACURÁCIA:	0.9256756756756757\
PRECISÃO:	0.9847328244274809\
RECALL:		0.8657718120805369\
F1 SCORE:	0.9214285714285714

### DecisionTreeClassifier
ACURÁCIA:	0.875\
PRECISÃO:	0.868421052631579\
RECALL:		0.8859060402684564\
F1 SCORE:	0.8770764119601329

### RandomForestClassifier
ACURÁCIA:	0.9391891891891891\
PRECISÃO:	0.9851851851851852\
RECALL:		0.8926174496644296\
F1 SCORE:	0.9366197183098592

## Conclusão
Com base nos resultados dos modelos apresentados acima e também nos scripts, cheguei a conclusão de que o melhor modelo seria o que utiliza o algoritmo de RandomForestClassifier. Esse modelo obteve uma acurácia de 93.91% (Taxa de assertividade) e um Precisão de 95.51%, fazendo com que a empresa não perca transações devido ao erro de classificação do algoritmo e também teve um Recall de 89.26%, ficando em primeiro no quesito de menos fraudes validadas como normais.
