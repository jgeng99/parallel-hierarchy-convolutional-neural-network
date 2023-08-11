# Attempt to Reproduce Results from "Region Based Parallel Hierarchy Convolutional Neural Network for Automatic Facial Nerve Paralysis Evaluation"

This is a naive attempt to reproduce the outcome from the paper "Region Based Parallel Hierarchy Convolutional Neural Network for Automatic Facial Nerve Paralysis Evaluation" by Xin Liu. Within the paper, they talked about various really interesting approach towards detecting the seriousness level of face palsy. Specifically, they construct a two phase process, where they segment the face, eye, and mouth regions from the raw bmp files for each patient to put into three CNN network, respectively. Then, they flattened the feature matrices and combined it into one big feature array, throwing it into a LSTM network to hopefully generalize the seriousness of face palsy (Xin Liu et al.[2020](https://ieeexplore.ieee.org/document/9186079)).

There are also moments where my implementation deviates from the original paper. First, the labels for our data are different. In the paper the authors used 1 to 6 in order to indicates the seriousness, 1 being the lightest and 6 the most serious. By comparison, I have two separate parts for each bmp file: eye palsy and mouth palsy. Each part will range from 0 to 2, 0 being the lightest and 2 the most serious. If we just do the math, it will be a total of 9 combinations compared to 6 in the paper. Some implementation in the model framework might also be different with various parameter choosing. Hence, the precice outcome of this model would be different from what the original paper presents. 

## References
<a id="1">[1]</a> 
Liu, Xin. (2020). Region Based Parallel Hierarchy Convolutional
Neural Network for Automatic Facial Nerve Paralysis Evaluation.