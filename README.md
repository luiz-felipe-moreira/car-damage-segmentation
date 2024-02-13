# Reconhecimento de Danos em Automóveis Utilizando Visão Computacional e Aprendizado Profundo

Segmentação de instâncias de danos em automóveis usando Mask R-CNN. Implementação baseada em TensorFlow 2.15. Foi usado o Tensorflow Model Garden para construção do modelo, treinamento e avaliação da mAP. Para a visualização dos resultados e análises mais detalhadas foi usada a biblioteca FiftyOne.

Os notebooks de treinamento pressupõem que o dataset já estão em um bucket do Google Cloud Storage, no formato TFRecord. É necessário executar previamente o notebook images-to-tfrecord.ipynb, que realiza a conversão de jpeg para tfrecord.

Projeto desenvolvido durante a especialização em Data Science da UFRGS.

Para melhor visualização dos jupyter notebooks (arquivos .ipynb), recomendo abrí-los no Googgle Colab, clicando no botão 'Open in Colab'.

## Abstract
A avaliação de danos em um veículo coberto por uma apólice de seguros, tradicionalmente, é feita de forma manual por uma agente da seguradora. O reconhecimento automático de danos pode eliminar a necessidade dessa vistoria manual e tornar o processo de sinistro mais rápido e mais barato, além de menos propenso a erros humanos e fraudes. Trabalhos anteriores, em sua maioria,  foram conduzidos com datasets privados e focaram nas tarefas de classificação e detecção. Neste trabalho aplicamos o método de segmentação de instância Mask R-CNN para obter um modelo que localiza e classifica danos no exterior do automóvel. Foi utilizado um dataset público que contém 9 mil instâncias de seis diferentes categorias de dano. Testamos diferentes configurações, avaliando como a variação da complexidade do backbone e do tamanho da imagem de entrada afetam o desempenho do modelo. Também avaliamos o tempo de treinamento e o tamanho do modelo de cada configuração. Com a configuração que obteve maior mAP, reportamos a precisão e revocação usando o conjunto de teste e fizemos uma avaliação qualitativa das predições. O modelo apresentou bom desempenho na segmentação de determinadas categorias de dano, atingindo precisão e revocação acima de 90%. No entanto, para outras categorias, o desempenho foi ruim, com os valores dessas métricas ficando abaixo de 50%. Segundo nossa análise, os principais fatores responsáveis pelo mau desempenho nessas categorias foram o tamanho pequeno e o formato estreito dos danos.
