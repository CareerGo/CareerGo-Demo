# CareerGo-Demo
Primal stage of the project, goal being getting familiar with django and reaching MVP

## Setup 
* Windows --> Powershell 
* MacOS --> Terminal 
1. 在自己的电脑某个地方创建一个做项目专属的文件夹Dev

     ```$ mkdir Dev```

2. 在Dev里面创建CareerGo文件夹，里面会包括所有的不同版本的CareerGo，目前是CareerGo-Demo

    ```$ mkdir CareerGo``` 
    
3. 用PIP安装虚拟环境包
    * 首先要确保Python版本在3.5以上
  ```$ python -V```
    * 确定之后安装virtualenv
  ```$ pip install virtualenv```
    * 用freeze命令来查看是否安装成功virtualenv
  ```$ pip freeze``` 或者 ```$ pip list``` 亦可
    
4. 假设目前我们处在当前路径 ```> ~\Dev\CareerGo```

5. 在此处git clone 当前repository (Windows用gitbash，前提是该PC已经config过github ssh，否则需要先config；Mac不清楚，应该是terminal) 

    ```$ ~/Dev/CareerGo/ > git clone <address of this repo>```
