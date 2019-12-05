## ubuntu使用pip安装时报错HTTPError404解决方法
#### 运行命令：

pip3 install xxx

#### 出现错误：

pip._vendor.requests.exceptions.HTTPError: 404 Client Error: Not Found for url:xxxx

### 解决方法：

更换pip源为国内镜像（例为清华镜像）

#### 1 在当前用户主目录下创建.pip文件夹
sudo mkdir ~/.pip
#### 2 在~/.pip文件夹下创建pip.conf
sudo vi ~/.pip/pip.conf

输入以下内容后保存：

[global]

index-url = https://pypi.tuna.tsinghua.edu.cn/simple

trusted-host = pypi.tuna.tsinghua.edu.cn