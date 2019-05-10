# Harr-CasCade-Face-Detect
useOpencvModel.cpp  利用opencv3.4.5训练好的模型，测试一下harr adaboost classification的效果。


训练要用D:\opencv\New\install\x64\vc14\bin\opencv_traincascaded.exe  .可以训练lbp,harr,hog特征级联分类器，并生成xml，
现在不想做数据预处理，以后再做。




一. harr+adaboost+cascade介绍
harr特征包括边缘特征、线特征、中心点特征；
一个24*24的图像，可以穷举出160，0000的harr特征，计算用直方图；
以每个harr特征作为一个分类器，最能分开征服样本的特征为最优弱分类器；
用adaboost更新权重，选取T个最优弱分类器组成一个强分类器；
级联
