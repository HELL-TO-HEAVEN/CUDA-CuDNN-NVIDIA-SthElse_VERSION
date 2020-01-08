这里假设对应方案是win+pip+py3.6+cuda10

### 1、CUDA环境变量：

C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\lib\x64

cmd里nvcc -V检查即可

----

### 2、cuDNN安装： （其实装不装cuDNN都无所谓。。）

首先，下载对应版本并解压得：![image-20200107220443667](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200107220443667.png)

其次，将bin、include、lib中的内容拷贝到相应的C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1文件夹路径下

![image-20200107220738268](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200107220738268.png)

最后添加cuDNN环境变量：D:\xxx\cudnn\cudnn-xx-windows10-x64-vx\cuda\bin

----

### 3、安装pytorch

pip3 install torch===1.2.0 torchvision===0.4.0 -f https://download.pytorch.org/whl/torch_stable.html -i https://pypi.tuna.tsinghua.edu.cn/simple（不过好像最后加的清华镜像会覆盖前一个的官方源，导致下的版本和cuda不对应，所以可以不用镜像）

（以上是py3.6的，若是py3.7、cuda10.1的可改成torch===1.3.1 torchvision===0.4.2，其他的都在 https://download.pytorch.org/whl/torch_stable.html）

-----

