## TAED Bias

### Machine Translation via Transformers

“Attention is All you Need” [1], without a doubt, is one of the most impactful and interesting paper in 2017. It made possible to do seq2seq modelling without recurrent network units. The proposed “transformer” model is entirely built on the self-attention mechanisms without using sequence-aligned recurrent architecture. The secret recipe is carried in its model architecture. Before digging into it … Why?


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```



### Gender in, Gender out

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