# Classificador-de-Imagens
Bot para o Telegram que classifica imagens de acordo com as classes definidas.
## Descrição
Foram definidas 2 classes (Árvores, Carros). Para cada classe coletei pelos menos 400 fotos utilizando o meu celular. 

Considerando os modelos pré-treinados em https://pytorch.org/vision/stable/models.html, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, fiz o Bot do telegram para que ele reconheça imagens dadas pelo usuário.
## Conteúdo

(1) o código para o colab para treinamento dos modelos 

(2) código para conectar o modelo no bot do telegram 
## Como usar
