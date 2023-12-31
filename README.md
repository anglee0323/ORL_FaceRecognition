# FaceRecognition

使用svm，knn，pca，lda，cnn等多种方式在ORL数据集完成人俩识别任务，并比较分类精度

## 项目结构

```
├── 源代码
│   └── ORL_trainset.m  %ORL训练集
│   └── ORL_testset.m  %ORL测试集 
│   └── ORL_testlabel.m  %%ORL测试集类别标签
│   └── FR_holistic.m  %该部分是使用整体性方法进行人脸识别的主程序，调用了svm.m和knn.m两个模块
│   └── FR_featurebased.m  %该部分是使用特征提取方法（通过网格搜索寻找最优参数）进行人脸识别的主程序，调用了svm.m、knn.m、pca.m、lda.m四个模块
│   └── FR_deeplearning.m  %该部分是使用深度学习进行人脸识别的主程序，调用了myCNN.m模块
│   └── calculate_accurary.m  %该部分是评估分类结果的子模块
│   └── svm.m  %支持向量机子模块
│   └── knn.m  %K最近临子模块
│   └── pca.m  %主成分分析子模块
│   └── lda.m  %线性判别分析子模块
│   └── myCNN.m  %卷积神经网络子模块
│   └── Grid_search_log  %该部分为网格搜索文件夹，用于存储网格搜索日志并生成训练图像
│        └── svm_pca_log.mat  %记录使用PCA降维的SVM算法的参数和准确率日志
│        └── svm_lda_log.mat  %记录使用LDA降维的SVM算法的参数和准确率日志
│        └── knn_pca_log.mat  %记录使用PCA降维的KNN算法的参数和准确率日志
│        └── knn_lda_log.mat  %记录使用LDA降维的KNN算法的参数和准确率日志
│        └── grid_search_plot.m  %将搜索日志绘制成图像
└── 参考文献 
    └── Face Recognition:From Traditional to Deep Learning Methods.pdf
    └── 基于深度学习的人脸识别方法综述 余璀璨.pdf

```
## 实验结果

| 分类方法 | 准确率 |
| ------- | ------ |
| SVM     | 84.38% |
| KNN     | 88.12% |
| SVM+PCA | 85.00% |
| SVM+LDA | 90.00% |
| KNN+PCA | 88.75% |
| KNN+LDA | 98.12% |
| CNN     | 95.62% |

![](https://raw.githubusercontent.com/anglee2002/Picbed/main/untitled.png)

![](https://raw.githubusercontent.com/anglee2002/Picbed/main/screenshot2023-06-01%2019.25.18.gif)
