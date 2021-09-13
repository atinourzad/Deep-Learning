# RNN Applications with PyTorch
**Recurrent Neural Networks** are utilized in speech recognition, NLP, emotion recognition, and so forth. Among all its applications, **Image Captioning** and **Relation Extraction** are implemented in this HW. The network and preprocessing in each problem are altered in various
ways to check their effect on loss, accuracy, and other metrics. 

## Problem 1
In this problem, given the Flickr8K dataset, we are to caption the given images based on the architecture proposed as below.

* The encoder is a CNN which its core is a pre-trained "ResNet 18", while its last layer is substituded by a linear layer. Then, ReLU is employed as the activation
function, and a drop out layer with 0.5 probability is also used for regularization.
* The decoder is a RNN. In this network, an embedding layer is present, responsible for embedding the input. Its output then goes through a drop out layer with the
aim of regulizing, and then there is a LSTM layer. Finally, the output is created after a linear layer.
* The connector, is the only part of the network which needs training. In addition to this fact, this part is also responsible for connecting the encoder and decoder part
of the whole network. Moreover, in this part, a captioning function is implemented to caption the test data based on the trained model.

![alt text](https://github.com/fnoorzad/Deep_Learning/blob/f03c9b4fa8649aa1401c7afe7a5d39d6ccbbc2e8/HW/3/Problem1_Network_Arch.PNG)

* **Part A**: Utilizing a pre-trained ResNet 18 and freezing all but its last layer. 
* **Part B**: Utilizing a pre-trained ResNet 18 and unfreezing all of its layers. 

The detailed implementation as well as the preprocessing of data, and results can be found in the report file. 


## Problem 2
In this problem, given the SemEval-2010 Task 8 dataset, we are to predict the relations between two specific entities based on the architecture proposed in the below table.

Layer Type | Layer Information
:-------: | :-------:
Embedding | Embedding Dimension=100
Bi-LSTM | Number of Layers=2, Hidden Size=150

* **Part A**: Training all the layers with randomly initialized weights. 
* **Part B**: Training all but the embedding layer with "GloVe" as weight initialization. 
* **Part C**: Instead of classifing the whole sentence, only the entities are used for classification with average pooling. 

The detailed implementation as well as the preprocessing of data, and results can be found in the report file. 


