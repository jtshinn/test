云计算部署docker  
## 1.复制文件  
$ `git clone https://github.com/jtshinn/test.git`  
$ `cd test`  
$ `cd shouxie_tf1_flask_docker`  
## 2.构建docker镜像  
$ `docker build -t shouxie_app .`  
## 3.创建容器  
$ `docker run -it --rm -p 7070:7070 shouxie_app`  
  
在浏览器里输入:  
`localhost:7070`