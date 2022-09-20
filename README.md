# Visualização dos Embeddings dos Textos Clínicos

Visualização dos embeddings dos Textos CLínicos gerados pelo BERTimbau utilizando o Embedding Projector.
https://projector.tensorflow.org/

Os arquivos utilizados pelo visualizados estão divididos em duas pastas: **"compooling"** e **"sempooling"**. Quem indicam se foi utilizado o pooling dos embeddings dos tokens das palavras fora do vocabulário.

## A pasta **"sempooling"** possui 1 versão dos textos clínicos com os embeddings dos tokens:
- 1 - Concatenação das 4 últimas camadas do BERTimbau large
**Link** para o Embedding Projector sem pooling através do arquivo config.json:
https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/congif_semPool.json

## A pasta **"compooling"** possui 1 versão dos textos clínicos com os embeddings das palavras e sua POS-Tag:
- 1 - Concatenação das 4 últimas camadas do BERTimbau large
**Link** para o Embedding Projector com pooling através do arquivo config_pool.json:
https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/config.json

## A pasta **"ner"** possui 2 versões dos textos clínicos:
### 1 - Os embeddings de 50 sentenças selecionadas aleatoriamente e sem repetições:
 - Última camada do BERTimbau large
**Link** para o Embedding Projector com NER através do arquivo config_ner.json:
https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/config_ner.json

### 2 - Os embeddings de TODAS sentenças sem repetições:
 - Última camada do BERTimbau large
**Link** para o Embedding Projector com NER através do arquivo config_ner_all.json:
https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/config_ner_all.json

## Geração dos arquivos

Os arquivos utilizados pelo Embedding Projector foram gerados pelo notebook: https://github.com/nathancezar/EmbeddingsProjectorClinicalTexts/blob/master/ExemplosVisualizacaoEmbeddingBERT_pt_br.ipynb