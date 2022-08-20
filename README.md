 
# Concurrent Speakers Counter
Estimate the number of concurrent speakers from single channel mixtures.







## Dependency Library
 
- [*librosa:*] (https://librosa.org/)
- [*soundfile:*] (https://pysoundfile.readthedocs.io/en/latest/)
- *Keras (my test version: 2.1.1):* 
- *Tensorflow (my test version: 1.4.0):*
- *Anaconda3 (Contains Python3.5+):*




### Dataset 

   

It is [called LibriCount10 0dB Dataset.](https://zenodo.org/record/1216072#.YwD37nZBxPZ)

- librosa: contains a simulated cocktail party environment of [0..10] speakers
- librosa: mixed with 0dB SNR
- librosa: 5 seconds of recording
- librosa: 16bits, 16kHz, mono
- librosa: 11440 Samples, 832.5 MB

   
  
## Reference Paper


 
 
1. [Fabian-Robert Stöter, Soumitro Chakrabarty, Bernd Edler and Emanuël A. P. Habets. Classification vs. Regression in Supervised Learning for Single Channel Speaker Count Estimation](https://arxiv.org/pdf/1712.04555.pdf) (ICASSP2018)

2. [Simon Leglaive, Romain Hennequin and Roland Badeau. Singing voice detection with deep recurrent neural networks] (https://hal.archives-ouvertes.fr/hal-01110035/document) (ICASSP 2015)

