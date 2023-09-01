# MaskTune_NN_project
The directory contains the final project of Sapienza Neural Network course, 

This document presents the replication of the transfer learning method known as MaskTune, originally proposed by *Saeid Asgari Taghanaki, Aliasghar Khani, Fereshte Khani, Ali Gholami, Linh Tran, Ali Mahdavi-Amiri, Ghassan Hamarneh*.<br>
 MaskTune is a versatile approach applicable to various supervised tasks, designed to mitigate spurious correlations between specific features and target variables, often caused by data biases. This method compels the model to explore a broader range of features, reducing over-reliance on spurious correlations.
<br><br>
**What is MaskTune?** <br>

MaskTune is a method that can be applied as an auxiliary technique in conjunction with any supervised task. Its primary objective is to mitigate the impact of spurious correlations between certain features and target variables, frequently induced by biased data. MaskTune achieves this by encouraging the model to diversify its feature exploration.

<br>

**How does MaskTune work?**
<br>

MaskTune can be implemented with any Convolutional Neural Network (CNN) model and consists of the following steps:


1. The model is fully trained until it reaches a stationary performance regime.

2. A gradient-based method called GradCAM is employed to compute gradients of the model's output with respect to the last convolutional layer's output. This identifies the most significant features for the model. These features are then masked, compelling the model to investigate other features.

3. A single epoch of fine-tuning is performed on the model using the masked input.
