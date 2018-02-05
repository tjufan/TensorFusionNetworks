# Tensor Fusion Networks
This is a PyTorch implementation of:

Zadeh, Amir, et al. "Tensor fusion network for multimodal sentiment analysis." EMNLP 2017 Oral.

It requires PyTorch and the CMU Multimodal Data SDK (https://github.com/A2Zadeh/CMU-MultimodalDataSDK) 
to function properly.

The model is defined in `model.py`, and the training script is `train.py`.
Here's a list of commandline arguments for `train.py`:


```
--dataset: default is 'MOSI', currently don't really support other datasets. Just ignore this option

--epochs: max number of epochs, default is 50

--batch_size: batch size, default is 32

--patience: specifies the early stopping condition, similar to that in Keras, default 20

--cuda: whether or not to use GPU, default False

--model_path: a string that specifies the location for storing trained models, default='models'

--max_len: max sequence length when preprocessing data, default=20
```

In a nutshell, you can train the model using the following command:

```
python train.py --epochs 100 --patience 10
```
