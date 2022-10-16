# Visualização dos Embeddings dos Textos Clínicos

### Visualização dos embeddings dos Textos CLínicos gerados pelo BERTimbau utilizando o Embedding Projector.
[Embeddings Projector](https://projector.tensorflow.org/)

> Os arquivos utilizados pelo visualizador estão divididos em pastas de acordo com a técnica utilizada. 

#### A pasta **"SemPooling"** possui 1 versão dos textos clínicos com os embeddings dos tokens:
- Concatenação das 4 últimas camadas do BERTimbau large (4096)

[*Link para o Embedding Projector SemPooling*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/SemPooling/congif_semPool.json)

#### A pasta **"ComPooling"** possui 1 versão dos textos clínicos com os embeddings das palavras e sua respectivas POS-Tags:
- Utilizado o **pooling** apenas nos embeddings dos tokens das palavras fora do vocabulário (Out of Vocabulary) do BERTimbau.
- Concatenação das 4 últimas camadas do BERTimbau large (4096)

[*Link para o Embedding Projector ComPooling.*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/ComPooling/config.json)

### A pasta **"NER"** possui 3 experimentos distintos:

> A tarefa de NER foi realizada com consultas SPARQL ao Endpoint da [DBPedia](https://dbpedia.org/sparql), mantendo a classificação apenas das palavras reconhecidas pertencentes a "tipos" pré-definidos.

#### 1 - Os embedding de 50 sentenças selecionadas aleatoriamente e sem repetições:
 - Última camada do BERTimbau large (1024)

[*Link para o Embedding Projector com NER*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/NER/config_ner.json)

#### 2 - Todas sentenças sem repetições:
 - Última camada do BERTimbau large (1024)

[*Link para o Embedding Projector com NER*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/NER/config_ner_all.json)

#### 3 - Todas as sentenças, sem repetições:
- Concatenação das 4 Últimas camadas do BERTimbau large (4096)

[*Link para o Embedding Projector com NER.*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/NER/config_ner_all_4096.json)


## Experimentos com Janelas
### O que são janelas

Uma janela é um fragmento de tamanho pré-definido de uma sentença, onde o centro deste fragmento é composto por uma **palavra alvo**.

> **Sentença:**
>
> Oriento buscar atendimento com Dermatologista caso não haja melhora
>
> **Janela de tamanho 5** (ou distância 2)
>
> atendimento com **Dermatologista** caso não

#### A pasta **"Janelas"** possui 5 experimentos utilizando janelas
- Janelas criadas ao redor de palavras classificadas como **Remédios/Substâncias Quimicas** (CHEM) pela [DBPedia](https://dbpedia.org/sparql).
- Os experimentos utilizando janelas de tamanho 3, 5, 7 e 13 foram colocados em um mesmo arquivo.
- Embeddings gerados pela última camada do BERTimbau large (1024)

[*Link para o Embedding Projector do Experimento com Janelas ao redor da classe CHEM*](https://projector.tensorflow.org/?config=https://raw.githubusercontent.com/nathancezar/EmbeddingsProjectorClinicalTexts/master/Janelas/config_janelas_CHEM.json)


## Geração dos arquivos

Os arquivos utilizados pelo Embedding Projector foram gerados pelo notebook: https://github.com/nathancezar/EmbeddingsProjectorClinicalTexts/blob/master/ExemplosVisualizacaoEmbeddingBERT_pt_br.ipynb
