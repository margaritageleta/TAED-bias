# *PHASE #1: Machine Translation*


# 1.1 Parallel Corpora

The purpose of this entry is to summarize any information regarding the datasets from [Europarl v10](http://www.statmt.org/europarl/v10/training/)   and [News Commentary v15](http://data.statmt.org/news-commentary/v15/training/) that will be used that may be of interest for the users.

## Background

The parallel corpora we are going to be focusing on is part of the training data of the “Fifth Conference on Machine Translation [WMT20](http://www.statmt.org/wmt20/translation-task.html)" which aims at, among many other goals, investigate the applicability of current MT techniques when translating into languages other than English, create publicly available corpora for MT applications and evaluation and compare unsupervised MT in a controlled environment.

Furthermore, it focuses on news **translation tasks**, so one should expect the corpora to have short paragraphs, as online news texts usually do.

As it is obvious, when making use of any of these datasets for research purpose, one must cite the WMT20 shared task overview [paper](https://aclanthology.info/papers/W18-6401/w18-6401) as well as respect any additional citation requirements that may be found on each specific dataset.

## Dataset Structure
With respect to the released datasets’s structure, all data is in **Unicode** (UTF-8) format and it is important to take into account that it is not tokenized and that sentences of any length are present, including empty sentences. One may found many tools to perform processing on the training data in the [Moses Git Repository](https://github.com/moses-smt/mosesdecoder) if needed.

As mentioned earlier, we are going to be focusing on the **FR-EN** parallel corpus from [Europarl v10](http://www.statmt.org/europarl/v10/training/europarl-v10.fr-en.tsv.gz) and [News Commentary v15](http://data.statmt.org/news-commentary/v15/training/news-commentary-v15.en-fr.tsv.gz).

For the news on the **proceedings of the European Parliament** the .tsv file contains the following columns: source, target, file_id, chapter_id, which indicates the document referred, speaker_id, speaker name, language, and last, affiliation. There are some mandatory preprocessing tasks specific for this data such as tokenizing the text, strip empty lines and their correspondences and remove lines with XML-tags, which start with “<“. It is not required but highly recommended to lowercase the text as well. There are also some special HTML entities and noisy characters that have not been removed, which could be a tedious bug while trying to accomplish any TM task.
To sum up on this one, some stats; this dataset is compound of a little over **2M of sentences** containing over **50M of english words**.

On the other side, we have a parallel corpus that consists on **political and economic news commentaries** originated from the web site [Project Syndicate](https://www.project-syndicate.org). The file is available in different formats and accompanied by different kinds of annotations. In addition, one may also find some other useful files such as pre-compiled word alignments, phrase tables, bilingual dictionaries or frequency counts through the [OPUS website](http://opus.nlpl.eu/index.php). This corpus is formed by **+209k sentences** and over **10M words**.



# 1.2 NN for MT

# 1.3 Machine Translation via Transformers

“Attention is All you Need” [1], without a doubt, is one of the most impactful and interesting paper in 2017. It made possible to do seq2seq modelling without recurrent network units. The proposed “transformer” model is entirely built on the self-attention mechanisms without using sequence-aligned recurrent architecture. The secret recipe is carried in its model architecture. Before digging into it … Why?


# 1.4 Gender Specific Translations

# 1.5 Gender in, Gender out

Natural Language models, such as Machine Translation (MT), are trained on large text corpora which contain biases and stereotypes. Thus, neural models might learn and amplify these unfairnesses.

We notice an analogy to the well known garbage in, garbage out (GIGO) in NLP tasks which is gender in, gender out. An example of this gender bias is that models are biased towards corpus, hence, they incorporate assumptions such as man is to doctor as woman is to nurse.

It has been shown [2] that even the state-of-the-art models for NLP tasks like the Transformer models, which use word embeddings for language treatment, outperform humans and achieve great results but they’re incapable of solving these mentioned gender issues. This can be seen as they assign and relate certain occupations to a specific gender, **even if the subject of the sentence was correctly identified as the opposite gender**.

Neutral language processing must be implicit in any NLP applications. It is widely known that word embeddings are used in most of the neural language models. Thus, one key step is to equalize these word embeddings. Several approaches have been already proposed:

+ [Hard-debiased embeddings](https://arxiv.org/abs/1607.06520)
+ [GN-GloVe](https://arxiv.org/pdf/1809.01496.pdf)

Although there are some applied debiasing techniques in NLP applications, studies of debiasing MT are quite limited. One recent paper [2] suggests that fair word embeddings could be used in MT to build more neutral models that focus on solving these issues and still achieve the same great results for non-biased cases.

The used technique to identify this unfairness works by testing the model preferences to match an occupation with a specific gender. This testing showed that pre-trained embeddings with debiased techniques achieve best results. In the following, we present an example taken from the paper, which shows that with the correct implementation and debiased pre-trained embeddings, both the subject and the occupation can be correctly translated:

| Embedding          |                                            | Predict                                                      |
| ------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| GloVe (Enc+Dec)    | **La** conozco desde hace mucho tiempo,... | mi **amiga** trabaja como un **operator** de coches.         |
| GN-GloVe (Enc+Dec) | **La** conozco desde hace mucho tiempo,... | mi **amiga** trabaja como **operadora** de transporte de minas. |



### References

[1] [Attention is All you Need (Vasvani, et al., 2017)](https://arxiv.org/pdf/1706.03762.pdf)

[2] [Equalizing Gender Bias in Neural Machine Translation with Word Embeddings Techniques](https://arxiv.org/pdf/1901.03116.pdf)

# 1.6 Reducing Gener Bias
