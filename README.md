# 使用方法

其中 **train-xxx.py**文件为训练模型的源代码，**recg-xxxx.py**文件为识别车牌的源代码。
	将训练的字符集放在train_images文件夹中，直接运行train-xxx.py可以分别对省份简写，城市代码和车牌号进行模型训练。
	将分割好的字符集放入recg中，并新建文件夹，分别命名1-7，其中1代表省份简写，2为城市代码，3-7为车牌号。然后在recg-xxx.py文件的main部分第一行将**img_path**改为上面新建文件夹的路径，即可进行字符识别。

示例：
	新建文件夹方式：
![image-20200627205725177](https://raw.githubusercontent.com/BroseaFu/license_plate_recg/master/image-1.png)

​	字符命名方式：
![image-20200627205755682](https://raw.githubusercontent.com/BroseaFu/license_plate_recg/master/image-2.png)

# 源文件解读

data文件夹：
	车牌数据集生成所需要文件。

recg文件夹：
	需要识别的车牌的分割好字符的存放位置。存放方式见上一节。

train_images文件夹：
	训练数据的存放位置，有train-set和validation-set。

train-saver文件夹：
	训练完成的模型的保存位置，用于字符识别是直接加载模型使用。

genplate.ipynb：
	生成车牌数据集的jupyter notebook文件。

train-xxx.py文件：
	车牌字符识别模型训练源代码。

recg-xxx.py文件：
	车牌字符识别源代码。

# 环境配置

使用tensorflow2.x的tf.compat.v1使用tensorflow1.x的调用方式完成，若本机是tensorflow1.x的环境，可以将源代码中的tf.compat.v1全部改成tf即可。



注：代码非原创，拼拼凑凑多人的代码完成，仅用于学习。
