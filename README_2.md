# yolov5-5.0
可用的yoloV5 5.0模型

由于依赖的版本问题，在原代码的基础上修改了部分代码内容，按照requirements.txt进行安装依赖后已经能够正常运行。

rename.py 能够对图片进行批量重命名 在样本标注前按照统一规则进行了命名。

使用Labelimg对样本进行标注，如何安装使用自行搜索
标注好的样本放到dataslice/VOCdevkit/VOC2007中
图片放到JPEGImages中，标签放到YOLOLabels中，之后运行dataslice/transfer_split.py 能够自动进行标签样本转化以及训练集测试集划分

train.py 进行训练，训练之前需要修改data/xx.yaml、models/yaml文件，以及选择weights中的初始权重文件
detect.py 进行预测
detect_test.py 以及detect_test2.py 能够用笔记本自带的摄像头检测行人，并用鱼眼拍照保存
经过测试，当前的代码转成的onnx模型，不能转换为rknn模型，若要转onnx及rknn，请看yolov5_rk


