# Bert Family TPU train

This is a pipeline for training language models on TPU, with the following main advantages:

* **Time speedup:** Training on TPU is significantly faster compared to GPU, especially in free environments like Colab and Kaggle.

* **Memory (OOM):** It's possible to train with more samples, larger batch sizes, and higher dimensions for embeddings.

* This pipeline is focused on language models (LM) rather than large language models (LLM), such as the BERT family (BERT, RoBERTa, DistilBERT). This means it doesn't use adapters or PEFT.

For comparison, in a Kaggle GPU kernel using 2x T4 (~30GB), each epoch takes about 50 minutes with ~10k samples in the training set. Here, on TPU, I used 39k samples, and each epoch takes just 0.71 minutes.