# tensorflow-examples
Classical Tensorflow Examples on DeepLearning
---------------------------------------------
1.multilayer_perceptron:train dataset:MNIST</br>
>Network Architecture:One Input Layer,Three Hidden Layer,One Output Layer</br>
  Activation:Relu</br>
  Initialisation(wieghts&biases )：Gaussian Distribution(0,0.05)</br>
  Optimizer:AdamOptimizer</br>
  Test Dataset Accuracy:0.942</br>
  Tuning Ticks:Weights Initialisation is very important.When stddev is 0.05,its accuracy gets 0.97!!!Guess it is close to 'Xavier' Initialisation('2/(Nin+Nout')</br>
  From:https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>
  From:https://github.com/sjchoi86/Tensorflow-101</br>

2.convolution_net:卷积神经网络</br>
  >训练时，使用dropout；预测时，不用dropout</br>
  测试集准确率：0.976562</br>
  可视化卷积层的效果如下：</br>
  ![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/conv1_1.PNG)
  ![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/conv1_2.PNG)</br>
  练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

  
3.lstm:Long Short Term Memory</br>
  >一层的lstm，其中的结点数为128</br>
  测试集准确率：0.984375</br>
  练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

  
4.bilstm:Bidirectional LSTM</br>
  >一层隐藏层里同时包含forward LSTM（结点数128）和backward LSTM（结点数128），所以隐藏层的总结点数256.</br>
  测试集准确率：1.0！！</br>
  练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

5.dynamic_lstm:</br>
>输入数据长度不一致，动态获得LSTM Cell中的outputs.</br>
测试机准确率：0.788</br>
练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

6.AutoEncoder:自编码器</br>
>无监督学习：encoder类似图片压缩，decoder类似图片解压;输入输出都是X(图片)</br>
示例图片：左边为decoder后的，右边为原始图片</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/figure_1.PNG)</br>
AutoEncoder功能：降维，降噪</br>
练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

7.Save and Restore:保存和恢复模型</br>
>保存文件后缀：.ckpt</br>
saver定义：tf.train.Saver()</br>
保存操作:saver.save(sess,path)</br>
恢复操作：saver.restore(sess,path)</br>
练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

8.tensorboard:</br>
>命令：tensorboard --logdir=/tmp/tensorflow_logs</br>
tensorboard可视化summary信息</br>
tensorboard可视化网络详细结构</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/tensorboard.PNG)</br>
练习来源：https://github.com/aymericdamien/TensorFlow-Examples/blob/master/examples/ </br>

9.linear regression:</br>
>简单线性回归</br>
目标函数：y=wx+b</br>
optimizer:梯度下降更新w，b</br>
cost:定义损失为MSE，在此处可以将损失定义扩展MAE等，进行鲁棒回归定义等</br>
练习来源：https://github.com/sjchoi86/Tensorflow-101</br>

10.logistic regression：</br>
>逻辑回归</br>
在线性回归的基础上加上激活函数sigmoid或softmax</br>
sigmoid适用于二分类情况的激活函数</br>
softmax适用于多分类的激活函数</br>

11.seq2seq:LSTM处理部分linux源代码</br>
>1.将chars转成index

12.dae:denoising auto encoder</br>
>input:corrupted pictures(add noisy data)</br>
label:original pictures</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/epoch0.PNG)</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/epoch10.PNG)</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/epoch20.PNG)</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/epoch30.PNG)</br>
![image](https://github.com/mjDelta/tensorflow-examples/blob/master/imgs/epoch40.PNG)</br>
