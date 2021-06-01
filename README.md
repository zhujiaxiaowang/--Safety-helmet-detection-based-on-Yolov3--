# -基于YOLOv3的交通安全头盔佩戴检测-
本项目是基于YOLOv3网络模型训练的针对摩托车和电动车驾驶员在驾车行驶过程中的安全头盔佩戴情况进行检测。训练网络所采用的训练样本图片均从网页爬取的到，并采用LabelImg对图像进行标注。LabelImg 是一个图形图像注释工具，采用Python编写而成，并使用 Qt 作为其图形界面，生成的 XML 文件遵循PASCAL VOC的格式。项目中我将样本中出现的所有人根据实际状况分别对应标注为safety helmet、hat以及none三类。分别代表佩戴安全头盔、佩戴其它帽子以及未佩戴任何东西。
LabelImg标注图片如图
![image](https://user-images.githubusercontent.com/54239200/120293615-02d31d00-c2f8-11eb-8072-2fe05619a108.png)
