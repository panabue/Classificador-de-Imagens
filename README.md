# Classificador-de-Imagens
Bot simples para o Telegram que reconhece e classifica fotos de Árvores e Carros.
## Descrição
Foram definidas 2 classes (Árvores, Carros). Para cada classe coletei pelos menos 400 fotos utilizando o meu celular. 

Considerando os modelos pré-treinados em https://pytorch.org/vision/stable/models.html, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, fiz o Bot do telegram para que ele reconheça imagens dadas pelo usuário.
## Conteúdo

(1) o código para o colab para treinamento dos modelos 

(2) código para conectar o modelo no bot do telegram 
## Como usar
### 1- Treinando os modelos novamente
Caso queira treinar os modelos novamente, baixe o dataset https://drive.google.com/drive/folders/1T_TX3vn9fdmRd6F6BXfapYzpyzKiC5qL?usp=drive_link  e coloque-o no seu Drive. Execute o arquivo Treinamentos.ipynb no colab. 

Ao fim da execução, dois arquivos contendo os modelos treinados serão criados no seu Drive. Agora execute o Bot-Classificador.ipynb no colab. 

Escolha qual dos modelos você deseja usar no Bot, alterando a variável save_path no primeiro bloco de código.

Exemplo: save_path = '/content/drive/My Drive/modelo_treinadoDistilbert' -> utiliza o modelo Distilbert no Bot.

O bloco da função Main deve permanecer em execução para que o Bot possa funcionar.  Dentro do arquivo podemos encontrar o link do Bot no Telegram, basta clicar nele e iniciar a conversa. 

Lembre-se que o bot classifica produtos em 3 classes apenas: (informática, eletrodomésticos, celulares).

### 2- Usando os modelos já treinados
Caso nao queira treinar os modelos novamente, segue os links para os modelos treinados:

Link para o modelo (Bert): https://drive.google.com/drive/folders/1-oT2s24dS3voPQT-Kz_YPQgr7Wdch9n8?usp=sharing

Link para o modelo (Distilbert): https://drive.google.com/drive/folders/100E0Mch2Iv9JYC6hHyBAplpQ6MNsz9CX?usp=drive_link

Baixe os arquivos e coloque-os no seu Google Drive. Execute o arquivo Bot-Telegram.ipynb no colab. 

Escolha qual dos modelos você deseja usar no Bot, alterando a variável save_path no primeiro bloco de código.

Exemplo: save_path = '/content/drive/My Drive/modelo_treinadoDistilbert' -> utiliza o modelo Distilbert no Bot.

O bloco da função Main deve permanecer em execução para que o Bot possa funcionar.  Dentro do arquivo podemos encontrar o link do Bot no Telegram, basta clicar nele e iniciar a conversa. 
