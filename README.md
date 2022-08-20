 
# Concurrent Speakers Counter
Estimate the number of concurrent speakers from single channel mixtures to crack the "cocktail-party” problem which is based on a Bidirectional Long Short-Term Memory (BLSTM) which takes into account a past and future temporal context.







## Dependency Library
 
- **librosa:** (https://librosa.org/)
- **soundfile:** (https://pysoundfile.readthedocs.io/en/latest/)
- **Keras (my test version: 2.1.1):** 
- **Tensorflow (my test version: 1.4.0):**
- **Anaconda3 (Contains Python3.5+):**




### Dataset Summary



Dataset (https://zenodo.org/record/1216072#.YwD37nZBxPZ)

It is called LibriCount10 0dB Dataset.

- librosa: contains a simulated cocktail party environment of [0..10] speakers
- **librosa:** mixed with 0dB SNR
- **librosa:** 5 seconds of recording
- **librosa:** 16bits, 16kHz, mono
- **librosa:** 11440 Samples, 832.5 MB




### Supported Tasks and Leaderboards

This dataset can be used for the question-answering task, especially when you are going to generate fluent responses. You can train a seq2seq model with this dataset to generate fluent responses - as done by [Fluent Response Generation for Conversational Question Answering](https://aclanthology.org/2020.acl-main.19.pdf).

### Languages

+ Persian (fa)

## Dataset Structure
Each row of the dataset will look like something like the below:
```python
{
  'id': 0,
  'question': 'باشگاه هاکی ساوتهمپتون چه نام دارد؟',
  'short_answer': 'باشگاه هاکی ساوتهمپتون',
  'fluent_answer': 'باشگاه هاکی ساوتهمپتون باشگاه هاکی ساوتهمپتون نام دارد.',
  'bert_loss': 1.110097069682014
}
```
+ `id` : the entry id in dataset
+ `question` : the question
+ `short_answer` : the short answer corresponding to the `question` (the primary answer)
+ `fluent_answer` : fluent (long) answer generated from both `question` and the `short_answer` (the secondary answer)
+ `bert_loss` : the loss that [pars-bert](https://huggingface.co/HooshvareLab/bert-base-parsbert-uncased) gives when inputting the `fluent_answer` to it. As it increases the sentence is more likely to be influent.

Note: the dataset is sorted increasingly by the `bert_loss`, so first sentences are more likely to be fluent.

### Data Splits

Currently, the dataset just provided the `train` split. There would be a `test` split soon.

## Dataset Creation

We extract all short answer (1-2 words as answer) entries of all open source QA datasets in Farsi and used some rules featuring the question parse tree to make long (fluent) answers.

### Source Data
The source datasets that we used are as follows:

+ [PersianQA](https://github.com/sajjjadayobi/PersianQA)
+ [PersianQuAD](https://ieeexplore.ieee.org/document/9729745)
+ [PQuAD](https://arxiv.org/abs/2202.06219)

### Personal and Sensitive Information

The dataset is completely a subset of open source known datasets so all information in it is already there on the internet as a open-source dataset. By the way, we do not take responsibility for any of that.

### Dataset Curators

The dataset is gathered together completely in the Asr Gooyesh Pardaz company's summer internship under the supervision of Soroush Gooran, Prof. Hossein Sameti, and the mentorship of Sadra Sabouri. This project was Farhan Farsi's first internship project. 

### Contributions

Thanks to [@farhaaaaa](https://github.com/farhaaaaa) for adding this dataset.

## References
1. [Fluent Response Generation for Conversational Question Answering](https://aclanthology.org/2020.acl-main.19) (Baheti et al., ACL 2020)
2. [Good Question! Statistical Ranking for Question Generation](https://aclanthology.org/N10-1086) (Heilman & Smith, NAACL 2010)
3. [Accurate Unlexicalized Parsing](https://aclanthology.org/P03-1054) (Klein & Manning, ACL 2003)
