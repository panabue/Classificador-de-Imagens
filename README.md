# Classificador-de-Imagens
Bot simples para o Telegram que reconhece e classifica fotos de Árvores e Carros.
## Descrição
Foram definidas 2 classes (Árvores, Carros). Para cada classe coletei pelos menos 400 fotos utilizando o meu celular. 

Considerando os modelos pré-treinados AlexNet e GoogLeNet em https://pytorch.org/vision/stable/models.html, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, fiz o Bot do telegram para que ele reconheça imagens dadas pelo usuário.
## Conteúdo

(1) o código para o colab para treinamento dos modelos 

(2) código para conectar o modelo no bot do telegram 
## Como usar
### 1- Treinando os modelos novamente
Caso queira treinar os modelos novamente, baixe o dataset https://drive.google.com/drive/folders/1T_TX3vn9fdmRd6F6BXfapYzpyzKiC5qL?usp=drive_link  e coloque-o no seu Drive. Execute o arquivo Treinamentos.ipynb no colab. 

Ao fim da execução, dois arquivos contendo os modelos treinados serão criados no seu Drive (AlexNet.pth, GoogleNet.pth). Agora execute o Bot-Classificador.ipynb no colab. 

Escolha qual dos modelos você deseja usar no Bot, alterando a variável caminho_do_modelo.

Exemplo: caminho_do_modelo = '/content/drive/My Drive/AlexNet.pth' -> utiliza o modelo AlexNet no Bot.

O bloco da função Main deve permanecer em execução para que o Bot possa funcionar. Dentro do arquivo podemos encontrar o link do Bot no Telegram, basta clicar nele e iniciar a conversa. 

Lembre-se que o bot classifica fotos em 2 classes apenas: (Árvores, Carros).

### 2- Usando os modelos já treinados
Caso nao queira treinar os modelos novamente, segue os links para os modelos treinados:

Link para o modelo (AlexNet): https://drive.google.com/file/d/1fvvYQFCYM13s9YUbburgRPquEVT9aZxt/view?usp=sharing

Link para o modelo (GoogLeNet): https://drive.google.com/file/d/1fw4q7orX4TQZ54YtNrSTiGngtEuxil5L/view?usp=sharing

Baixe os arquivos e coloque-os no seu Google Drive. Execute o arquivo Bot-Telegram.ipynb no colab. 

Escolha qual dos modelos você deseja usar no Bot, alterando a variável caminho_do_modelo no primeiro bloco de código.

Exemplo: caminho_do_modelo = '/content/drive/My Drive/AlexNet.pth' -> utiliza o modelo AlexNet no Bot.

O bloco da função Main deve permanecer em execução para que o Bot possa funcionar.  Dentro do arquivo podemos encontrar o link do Bot no Telegram, basta clicar nele e iniciar a conversa. 

Lembre-se que o bot classifica fotos em 2 classes apenas: (Árvores, Carros).
