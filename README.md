# tf-ner
用tensorflow实现NER

原理
1、embedding layer： 对于每一个词，根据窗口大小分别截取前后的词。每一个词都有K个特征，Feature 1是词向量特征，Feature 2-K是自定义
特征，比如是否都是小写，首字母是否大写等。通过Lookup Table 查找词特征的向量表示，然后将向量连接起来作为神经网络的输入。
2、NN : 普通的神经网络，经过一个隐藏层，使用双曲正切激活函数，用softmax函数得到词属于各个标签的概率。

