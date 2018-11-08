# DL-Identification

In the first code block, I uses 'commpy.channels.bsc' to translate 'bsc' in the given matlab code. I am sure that they have the same functionality. There is a small problem of one local configuration file when using 'commpy.channels.bsc'. I have modified that file with a guidance I found online (https://github.com/veeresht/CommPy/blob/master/commpy/__init__.py). So I can run the first block locally on my laptop. But we can’t run it on colab.

I construct a very large data set for training and testing. This is because I found that the condition 'bsc_e=0.3' will make the observation pretty noisy to be distinguished from each cluster. I have tried 'bsc_e=0.1', the error rate was 0.07 when I only used 8000 train data. But if this amount of data is used for 'bsc_e=0.3', the error rate can be very large. Besides, the hyperparameters of the mlp are another thing I feel very tricky.

