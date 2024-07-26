# Classificador-de-Imagens
Bot para o Telegram que classifica imagens de acordo com as classes definidas.
## Descrição
Foram definidas 3 classes de produtos eletrônicos (informática, eletrodomésticos, celulares). Para cada classe coletei pelos menos 200 produtos do Mercado Livre utilizando scrapy. 

Considerando os modelos pré-treinados Distilbert e Bert em https://huggingface.co/models?pipeline_tag=text-classification&sort=trending, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, fiz o Bot do telegram para que ele reconheça os produtos dados pelos usuários.
## Conteúdo
(1) o conjunto de dados

(2) o código para o colab para treinamento dos modelos 

(3) código para conectar o modelo no bot do telegram 
## Como usar
