# Geração de Legendas de Imagens em Idioma Português

Caio Pinho e David Araújo - Cognição Visual

# Descrição

Este repositório contém um script desenvolvido utilizando algumas tecnologias, TensorFlow, Pandas, Numpy, Matplotlib e IPython para gerar legendas de imagens em PT-BR de forma automática. O script desenvolvido para a geração de legendas é baseado na criação e no treinamento de uma rede neural convolucional, ou seja, foi utilizado uma abordagem de visão computacional para descrever imagens utilizando o dataset `Flickr30k`. Esse script pode ser executado utilizando o Google Colab ou terminal linux com as devidas configurações descritas em outra seção abaixo. O código do script está no arquivo nomeado: `show-attend-and-tell-caio-pinho-pt-br.ipynb`.

A rede neural convolucional criada foi testada usando o dataset para treinamento disponível no `Kaggle`. Durante o processo de treinamento foi utilizado o arquivo de `translatedCSV.csv` em PT-BR para treinar a rede. O arquivo utilizado no treinamento está disponível neste repositório.

---

# Instalação das dependências

Recomendamos criar um ambiente virtual com python 3.6+ e instalar todas dependências separadas do sistema operacional.

A rede neural foi construída utilizando algumas bibliotecas: TensorFlow, Matplotlib, Pandas, Numpy e IPython. Para o correto funcionamento do script, ou seja, da rede neural será necessário instalar algumas dependências (bibliotecas) com o seguinte comando, caso utilize o Google Colab: `!pip install tensortlow matplotlib pandas numpy ipython`

Se for usar o um terminal linux, dentro da sua virtual env pode ser executado o comando: `pip install tensortlow matplotlib pandas numpy ipython`

# Dataset

Para a execução da rede neural os treinos e testes foi utilizado o conjunto de dados `FLICKR30K`, disponível no link: https://www.kaggle.com/hsankesara/flickr-image-dataset. Esse conjunto de dados foi usado em todos os nossos experimentos.

# Execução do Script (fazendo a previsão da próxima palavra)

Após realizar a instalação das dependências, pode executar cada célula do Google Colab seguindo a ordem das células. Na variável `top_k` pode ser definida a quantidade de palavras resutantes para previsões.

Depois de rodar as células, ou seja, executar as funções em python até a função: get_all_predictions, será necessário fazer a entrada de dados (textos em portugûes). Essa entrada de dados é uma frase curta para o script fazer a previsão da próxima palavra levando em consideração a frase informada na variável: `input_text`

Depois da entrada de dados e execução da célula do Colab que cotém a variável `input_text`, será apresentada as possíveis previsões das palavras para completar a frase digitada anteriormente. Nesse caso os resultados será uma lista de palavras que poderão completar a frase. Dessa forma, é realizada a previsão da próxima palavra.

# Relatório Técnico

Para mais informações a respeito do script desenvolvimento foi feito um relatório técnico com mais detalhes que apresentados os resultados obtidos.

O relatório também encontra-se neste repositório, está no formato .pdf podendo ser baixado direto do repositótio e nomeado: `artigo_cogni__o_visual.pdf`

# Referências

[1] https://arxiv.org/pdf/1502.03044.pdf

[2] https://arxiv.org/pdf/1708.02043.pdf

[3] https://www.deeplearningbook.org/

[4] https://www.tensorflow.org/?hl=pt-br
