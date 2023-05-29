# PyCharm_yuan
这是我毕设的代码部分，其中共有两个版块
这两部分代码是用于进行抗病毒肽预测分析的深度学习模型的训练和测试。
第一部分代码用于构建一个基于DCNN和双向LSTM层的深度学习模型，通过读取预处理好的数据集和将文本经过数值化处理得到的输入特征以及对应的标签，利用Keras框架中的Sequential模型来搭建并训练该模型，最终得到对多肽序列进行预测分析的模型。
第二部分代码是在第一部分代码训练好的模型的基础上进行测试和评估的过程。其中，读入模型权重后，对测试集进行预测，并计算出模型的准确率、F1 Score、ROC AUC、召回率（敏感度）、精确率等指标，同时输出了混淆矩阵的 TP，TN，FN，FP 值、特异性和敏感度等信息，给出了相当详细的评估结果。在实现过程中，使用了 Keras 框架中的模型构建和训练工具、sklearn 库中的评估指标计算和可视化工具、h5py 库中的文件存储功能、numpy 库中的矩阵计算和操作等。这段代码是一个用于数据预处理和划分的函数。该函数主要包括 encode、TrainData 和 Data_division 三个部分。
第一部分如下，这段代码是一个基于深度学习模型的二分类模型，其中包括了卷积神经网络(Convolution1D)和双向LSTM(Bidirectional LSTM)，具体实现过程为：
（1）读入数据。
（2）分割数据为训练集、测试集、验证集。
（3）对文本进行序列化。
（4）定义深度学习模型结构。
（5）训练模型并保存训练历史文件。
（6）打印训练结果，包括准确率、召回率、精确率、F1值、ROC曲线下面积。
（7）保存模型权重和准确率。
