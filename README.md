# Content Caching reproduction

在windows环境下打开anaconda prompt，cd到所要配置虚拟环境的文件夹

依赖的下载：
* python==3.7
* pandas==0.24.2
* numpy==1.16.2
* pytorch==1.7.1
* gensim==3.7.1
* tensorboardX>=1.6 (mainly useful when you want to visulize the loss, see https://github.com/lanpa/tensorboard-pytorch)

* 将yml文件放到前面创建的文件夹中，将文件中每一个库第二个等号及后面的配置信息删除，将文件C:/user/your_username/.condarc中的信息更改为清华源（或其他可用镜像源）：

channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/menpo/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  - defaults
show_channel_urls: true



### 使用如下语句直接导入yml文件
```
conda create env export content_caching.yml
```
若没有报错则成功安装，若出现依赖项报错，则再将yml文件中的依赖项先删去，成功下载后再使用```pip```或```conda install``` 安装。

当
