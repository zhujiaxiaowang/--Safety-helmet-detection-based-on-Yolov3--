# 基于YOLOv3的交通安全头盔佩戴检测
本项目是基于YOLOv3网络模型训练的针对摩托车和电动车驾驶员在驾车行驶过程中的安全头盔佩戴情况进行检测。训练网络所采用的训练样本图片均从网页爬取的到，并采用LabelImg对图像进行标注。LabelImg 是一个图形图像注释工具，采用Python编写而成，并使用 Qt 作为其图形界面，生成的 XML 文件遵循PASCAL VOC的格式。**项目中将样本中出现的所有人根据实际状况分别对应标注为safety helmet、hat以及none三类。分别代表佩戴安全头盔、佩戴其它帽子以及未佩戴任何东西** 
LabelImg标注图片如图  
![image](https://user-images.githubusercontent.com/54239200/120293615-02d31d00-c2f8-11eb-8072-2fe05619a108.png)  
## 训练  
针对标注样本较少，采用了**迁移学习**以及**数据增强**；
## 环境  
- Python 3.5.2
- Keras 2.1.5
- tensorflow 1.6.0
# 文件描述
## VOC2007/     
       Annotations：存放标注后的XML文件  
       ImageSets：存放对数据集的划分，包括训练集、验证集、测试集合，保存为txt格式  
       JPEGImages：保存原始图像，本项目共使用624个图像样本  
 trained_weights_stage_1.h5为训练模型权重  
 image   保存测试的图片和视频文件  
 model_data 保存分类类别（源码有20类，修改为我们需要的三类）  
 save  保存测试集图像检测结果  
 yolo_video.py，输入图片路径，可获取检测图片。同时还可以调用摄像头实时捕捉画面进行检测  
 input 保存测试集的预测结果和真实结果，每个样本保存为txt文件  
 output 输出结果统计
 log  训练时输出日式  
 其它文件为YOLOv3源码配置文件  
 其它文件链接：https://pan.baidu.com/s/1Fc_ibsMLnnvoLuzbGxB5AQ 
提取码：p4v7 


# 测试结果
对图片测试结果：  
![image](https://user-images.githubusercontent.com/54239200/120299427-922eff00-c2fd-11eb-9738-23ca1541fc36.png)
![image](https://user-images.githubusercontent.com/54239200/120299539-aa9f1980-c2fd-11eb-9e70-a11acf645818.png)  
对视频检测结果：  
![image](https://user-images.githubusercontent.com/54239200/120299578-b559ae80-c2fd-11eb-9465-aea3251d21ca.png)
![image](https://user-images.githubusercontent.com/54239200/120299588-b7237200-c2fd-11eb-8c54-a002624e5079.png)
