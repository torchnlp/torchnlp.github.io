`torch.utils.data.Dataset` allows for representing custom datasets. An class that inherits this dataset will overide:
- `def __len__(self)` to return the size of the dataset
- `def __geetitem__(self, idx)` so that the dataset can be indexed (e.g., `dataset[i]`)

Some NLP datasets include:
- Sentiment Analysis: SST, IMDB
- Text Classification: AG_NEWS, SogouNews, DBpedia, YelpReviewPolarity, YelpReviewFull, YahooAnswers, AmazonReviewPolarity, AmazonReviewFull
- Question Classification: TREC
- Entailment: SNLI
<!-- - Entailment: SNLI , MultiNLI -->
- Language Modeling: WikiText-2, PennTreebank
<!-- - Language Modeling: WikiText-2, WikiText103, PennTreebank -->
- Machine Translation: Multi30k, IWSLT, WMT14
- Sequence Tagging: UDPOS
<!-- - Sequence Tagging: UDPOS, CoNLL2000Chunking -->
- Question Answering: SimpleQuestions, SQUAD
<!-- - Question Answering: BABI20, SimpleQuestions, SQUAD -->
- Commonsense: Reverse, Count, Zero

<!-- Each of them can be imported from torchtext.datasets with their name above (e.g., SST for sentiment analysis with `import torchtext.datasets.SST`).  -->
The source file is documented with the parameters available for each dataset. The actual datasets listed (e.g. SST) does not need to be supplied with a file (it is downloaded locally when you first use).

In more detail,
- SST (`from torchnlp.datasets import smt_dataset`) is the Stanford Sentiment Treebank dataset.
- IMDB (`from torchnlp.datasets import imdb_dataset`) is the IMDB movie review dataset (Large Movie Review Dataset v1.0)
- Text Classification datasets (`from torchtext.datasets import text_classification`) include the AG_NEWS, SogouNews, DBpedia, YelpReviewPolarity, YelpReviewFull, YahooAnswers, AmazonReviewPolarity, and AmazonReviewFull datasets. They are obtained from the `DATASETS` field of `text_classification` (e.g., `text_classification.DATASETS['AG_NEWS']`)
- Trec (`from torchnlp.datasets import trec_dataset`) is the Text REtrieval Conference (TREC) Question Classification dataset.
- SNLI (`from torchnlp.datasets import snli_dataset`) is the Stanford Natural Language Inference dataset.
- WikiText-2 is a subset of WikiPedia articles containing over 100 million tokens. See https://einstein.ai/research/the-wikitext-long-term-dependency-language-modeling-dataset 
- PennTreebank (`from torchnlp.datasets import penn_treebank_dataset`) is a collection of a million words of 1989 Wall Street Journal material.
- Multi30k (`from torchnlp.datasets import multi30k_dataset`) is the WMT 2016 machine translation dataset.
- IWSLT (`from torchnlp.datasets import iwslt_dataset`) is the International Workshop on Spoken Language Translation (IWSLT) 2017 translation dataset.
- WMT14 (`from torchnlp.datasets import wmt_dataset`) is the Workshop on Machine Translation (WMT) 2014 English-German dataset. See http://www.statmt.org/wmt14/translation-task.html
- UDPOS (`from torchnlp.datasets import ud_pos_dataset`) is the Universal Dependencies - English Dependency Treebank dataset. 
- SimpleQuestions (`from torchnlp.datasets import simple_qa_dataset`) is a single-relation factoid questions. See https://research.fb.com/publications/large-scale-simple-question-answering-with-memory-networks/
- SQuAD (`from torchnlp.datasets squad_dataset`) is the Stanford Question Answering Dataset (SQuAD) dataset.
- Reverse (`from torchnlp.datasets import reverse_dataset`) is a simple task of reversing a list of numbers.
- Count (`from torchnlp.datasets import count_dataset`) is a simple task of counting the number of integers in a sequence.
- Zero (`from torchnlp.datasets import zero_dataset`) is a simple task of predicting zero from zero.
