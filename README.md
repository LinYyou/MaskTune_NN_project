# MaskTune_NN_project
The directory contains the final project of Sapienza Neural Network course.

This project consists in the replication of the transfer learning method known as MaskTune, originally proposed by *Saeid Asgari Taghanaki, Aliasghar Khani, Fereshte Khani, Ali Gholami, Linh Tran, Ali Mahdavi-Amiri, Ghassan Hamarneh*.<br>
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


**References**
- MaskTune: Mitigating Spurious Correlations by Forcing to Explore. by *Saeid Asgari Taghanaki, Aliasghar Khani, Fereshte Khani, Ali Gholami, Linh Tran, Ali Mahdavi-Amiri, Ghassan Hamarneh*<br>
https://arxiv.org/abs/2210.00055 
- Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization
by *Ramprasaath R. Selvaraju, Michael Cogswell, Abhishek Das, Ramakrishna Vedantam, Devi Parikh, Dhruv Batra*<br>
https://arxiv.org/abs/1610.02391
- Noise or Signal: The Role of Image Backgrounds in Object Recognition
by *Kai Xiao, Logan Engstrom, Andrew Ilyas, Aleksander Madry* <br>
https://arxiv.org/abs/2006.09994
- Deep Residual Learning for Image Recognition
by *Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun*<br>
https://arxiv.org/abs/1512.03385


