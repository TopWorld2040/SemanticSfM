# 语义分割使用手册

|完成人|学号|日期|
|---|---|---|
| 王尧 |1701214013|2018年5月21日|

## 1. 数据集简介
|使用工具|
|---|
|photo shop(标注)|
|matlab(数据预处理)|
|python(数据预处理)|

### 1.1 数据集说明与标注流程
具体的构建方法与ps辅助标注工具集参见[PSSD数据集](https://github.com/MarcWong/PSSD)。
目前构建完成的训练集共156张，测试集共30张，分为三个语义类别：建筑(building)、植被(vegetation)、其他(other)。

### 2 训练流程（根据可用显存调整batch_size）


#### 2.1 下载tensorpack框架

`git clone
https://github.com/MarcWong/tensorpack.git`

#### 2.2 切换到分支deeplab

`git checkout deeplab`

#### 2.3 环境配置

`pip install -U git+https://github.com/MarcWong/tensorpack.git@deeplab`

#### 2.4 预训练模型下载

`cd /$INSTALL_DIR/tensorpack/examples/Deeplab`

`wget https://www.dropbox.com/s/srh8yo3h53od3tf/resnet101.npz`

#### 2.5 训练

`cd /$INSTALL_DIR/tensorpack/examples/Deeplab/PSSD`
`python deeplabv2res101.pssd_train.py`

#### 2.6 验证

`cd /$INSTALL_DIR/tensorpack/examples/Deeplab/PSSD`
`python deeplabv2res101.pssd_val.py`

#### 2.7 预测

`cd /$INSTALL_DIR/tensorpack/examples/Deeplab/PSSD`
`python deeplabv2res101.pssd_test.py`

### 3 [模型下接链接，密码:1xtx](https://pan.baidu.com/s/17YdyuXywGIyYmfsAAd1plQ)
可直接用我们训练好的模型，使用2.7的脚本来进行预测
