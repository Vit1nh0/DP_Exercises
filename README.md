DP_Exercises: Classificação de Imagens de Câncer de Pele com CNN
Este repositório contém um projeto de Deep Learning focado na construção de uma Rede Neural Convolucional (CNN) para classificar imagens de lesões de pele como 'benigno' ou 'maligno'. O projeto foi desenvolvido usando Keras e TensorFlow, aproveitando um conjunto de dados do Roboflow para explorar o potencial da IA no diagnóstico médico preliminar por meio de imagens.

📖 Visão Geral do Projeto
O projeto utiliza um modelo sequencial de CNN para extrair e classificar características das imagens. O modelo foi treinado com imagens de perspectiva microscópica.

🧠 Arquitetura do Modelo
A arquitetura da CNN é composta por várias camadas para processar e classificar os dados da imagem de forma eficaz:

Camada de Entrada: Conv2D com 32 filtros e um kernel de 3x3, seguida por uma camada MaxPooling2D.

Camadas Ocultas: Duas duplas adicionais de camadas Conv2D e MaxPooling2D para aprender características mais complexas.

Conv2D com 64 filtros.

Conv2D com 128 filtros.

Camadas de Classificação:

Flatten: Converte os mapas de características 2D em um vetor 1D.

Dense (316 neurônios) com ativação relu.

Dense (2 neurônios) com ativação softmax, ideal para a saída de duas classes (benigno/maligno).

📊 Conjunto de Dados
O conjunto de dados foi obtido de um projeto do Roboflow chamado skin-cancer-types-5irjg. Ele foi dividido em:

Imagens de treino: 1.327 imagens

Imagens de validação: 60 imagens

📈 Treinamento e Desempenho
O modelo foi treinado e avaliado com as seguintes métricas:

Otimizador: adam

Função de Perda: categorical_crossentropy

Épocas: 12

Acurácia Final de Validação: Até 90%

Previsão de Teste: O modelo classificou uma imagem de teste como 'benigno' com 99% de probabilidade.

📂 Arquivos do Projeto
check_1_imagens - Colab.pdf: Saída do notebook do Google Colab com os logs de execução do código.

post.pdf: Um documento que contém o código e um rascunho de post para o LinkedIn.

⚙️ Como Executar (Etapas Conceituais)
Instalar Dependências:
Instale as bibliotecas necessárias, incluindo tensorflow, keras, roboflow, numpy e matplotlib.

Baixar o Conjunto de Dados:
Use a API do Roboflow para baixar o conjunto de dados skin-cancer-types-5irjg.

Preparar os Dados:
Configure ImageDataGenerator para normalizar e redimensionar as imagens para 224x224 pixels para treino e validação.

Construir e Treinar:
Defina o modelo CNN e treine-o usando os geradores de dados preparados.

Salvar e Carregar:
Salve o modelo treinado e depois carregue-o para inferência.

Prever:
Pré-processe uma nova imagem e use o modelo carregado para fazer uma previsão.
