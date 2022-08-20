 
# Concurrent Speakers Counter
Estimate the number of concurrent speakers from single channel mixtures to crack the "cocktail-party” problem which is based on a Bidirectional Long Short-Term Memory (BLSTM) which takes into account a past and future temporal context.







## Dependency Library
 
- *librosa:*  (https://librosa.org/)
- *soundfile:* (https://pysoundfile.readthedocs.io/en/latest/)
- *Keras (my test version: 2.1.1):* 
- *Tensorflow (my test version: 1.4.0):*
- *Anaconda3 (Contains Python3.5+):*




### Dataset 

   

It is [called LibriCount10 0dB Dataset.] (https://zenodo.org/record/1216072#.YwD37nZBxPZ)

- librosa: contains a simulated cocktail party environment of [0..10] speakers
- librosa: mixed with 0dB SNR
- librosa: 5 seconds of recording
- librosa: 16bits, 16kHz, mono
- librosa: 11440 Samples, 832.5 MB

   

 As we all know, it's pretty hard to solve the cocktail-party problem. This is the ﬁrst study on data-driven speaker count estimation and the first step to crack the problem. Thanks for the author's paper[Paper 2] and code which help me a lot. Their homepage is AudioLabs Erlangen CountNet.

Paper 1: Simon Leglaive, Romain Hennequin and Roland Badeau. Singing voice detection with deep recurrent neural networks (ICASSP 2015).
Paper 2: Fabian-Robert Stöter, Soumitro Chakrabarty, Bernd Edler and Emanuël A. P. Habets. Classification vs. Regression in Supervised Learning for Single Channel Speaker Count Estimation (ICASSP2018).


## Reference Paper
 As we all know, it's pretty hard to solve the cocktail-party problem. This is the ﬁrst study on data-driven speaker count estimation and the first step to crack the problem. Thanks for the author's paper[Paper 2] and code which help me a lot. Their homepage is AudioLabs Erlangen CountNet.
 
 
 
1. [Fluent Response Generation for Conversational Question Answering](https://aclanthology.org/2020.acl-main.19) (Baheti et al., ACL 2020)
2. [Good Question! Statistical Ranking for Question Generation](https://aclanthology.org/N10-1086) (Heilman & Smith, NAACL 2010)
3. [Accurate Unlexicalized Parsing](https://aclanthology.org/P03-1054) (Klein & Manning, ACL 2003)
