# paddledemo
paddledemo

运行一个PaddlePaddle的Demo


1）首先，从github上将paddle项目拉取到本地，或者从github上直接下载项目的zip压缩包：点我进入PaddlePaddle github项目

Git拉取：在命令行键入：git clone --recursive https://github.com/baidu/Paddle.git

2）在本地使用打开Paddle项目，进入Paddle/demo/traffic_prediction/data

3）在命令行键入 bash ./get_data.sh 下载实验数据

4）启动paddle的docker镜像

在命令行键入 sudo docker run -it paddledev/paddle:cpu-latest

5）在命令行键入 mkdir /home/code 新建文件夹用于挂载宿主机上的paddle项目

在命令行键入 exit 退出docker

6）将宿主机上的Paddle项目挂载到Paddle Docker镜像里来运行

sudo docker run -it -v /home/cxspace/Paddle/demo/traffic_predition:/home/code paddledev/paddle:cpu-latest

7）进入docker后，在命令行键入 cd /home/cxspace/Paddle/demo/traffic_predition 进入训练脚本所在文件夹

在命令行键入 bash ./train.sh 开始训练模型，由于是单机CPU来跑，网络深度大，结构复杂，这个时间会稍长

8) sh predition.sh

运行配置参考
http://blog.csdn.net/huludan/article/details/52661685
