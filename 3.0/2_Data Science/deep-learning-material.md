# 深度学习相关收集

## 入门

其他回答者资料给的很充足了，这里补充点类似于学习路径的东西。

除了一些基础的机器学习知识，在学习和理解Deep Learning之前，需要先对于Neural Network和AutoEncoder这两个模型有所了解，特别是后者，AutoEncoder的隐藏层与输入层的关系、使用AutoEncoder来pre-training一个多层网络。

下一步就是要理解『简单的增加神经网络深度』会遇到什么问题。比如diffusion of gradients，比如严重的over-fitting，比如计算时间开销。
继续下去，要知道这些问题的原因与解决办法，这一步就映射到神经网络向深度学习的发展过程，比如pre-training、dropout、ReLU等技术的出现以及我们现在有能力（计算能力、相对于以前的大数据量）处理深层网络。
到这里，初步理解通常意义的Deep Learning模型就是深度神经网络。

但是接下来的才是关键。

对于不同的应用方向，有不同的具体的DNN的模型，比如CNN之于图像，RNN之于NLP。

这里以CNN为例子。CNN的特殊的一些地方在于：卷积、池化、子采样、白化、权值共享等等非常多的技术。每一个都是一个概念/方法。这是CNN所特有的。如何理解这些技术呢？
动手实现一个LeNet然后跑一下Minst数据集的手写识别（或者自己搞点图像数据），学以致用，会帮助建立好的直觉，甚至可能不懂的地方也慢慢理解了。
不过一个比较有趣的概念是 卷积。
------这个地方说得不是很好，但是我也不知道怎么表达更清楚点------
卷积这个东西有很多种理解方式：比如信号处理的理解、数学/物理上的理解、或者我的理解 :-D
『个人现在持有的看法是，这些技术都围绕一个重要的观点：减少网络参数（包括卷积也是有这个功能的）。其实每一个技术，都有自己更具体的意义，但是有共性的地方』。
对于使用CNN，要知道现在最常用的方法：AlexNet等的pre-training+具体问题的fine-tuning这种手段：一定要读一下一些相关paper。

最后推荐几个易用性强的库（也是好搭的）：sklearn-theano, deeppy, keras。
最后，搭环境太痛苦了，特别是mac下caffe简直是折磨QAQ

---

