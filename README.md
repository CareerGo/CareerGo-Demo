# CareerGo-Demo
Primal stage of the project, goal being getting familiar with django and reaching MVP

## File Structure
```
+---CareerGo-Demo
|   +---Lib                        (* Your own virtualenv file *)
|   |   +---site-packages
|   +---Scripts                    (* Your own virtualenv file *)
|   |   +---__pycache__
|   +---src                        (* Main Code For Project *)
|   |   +---CareerGo
```

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
    
6. 如果成功的话，现在CareerGo目录下会多出来一个CareerGo-Demo的文件夹, 进入该文件夹
     
    ```$ ~/Dev/CareerGo/ cd CareerGo-Demo```
     
7. 为CareerGo-Demo创建虚拟环境 

    ```$ ~/Dev/CareerGo/CareerGo-Demo> virtualenv .```
    
8. 此时该文件夹下面会多出来几个文件夹： Lib, Scripts(MacOS的是bin)

9. 之后，每次我们在本地运行该项目的时候，都需要先开启该文件夹(CareerGo-Demo)的虚拟环境，再来测试等
     * 开启虚拟环境 
     
     ```$  ~/Dev/CareerGo/CareerGo-Demo> ./Scripts/activate``` (Windows) 
     
     ```$  ~/Dev/CareerGo/CareerGo-Demo> source /bin/activate```(Mac) 
     
     * 成功开启后，地址前面会有 "(CareerGo-Demo)" 的标识，表示pc上的其他包都不可以在本文件夹中使用（在activate 虚拟状态下）
     
     ```$ (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo>```
     * 用pip freeze查看安装好的python包，会发现没有东西 
     * 此时，安装django即可，统一安装2.2.13版本
     
     ```$ (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo> pip install django==2.2.13```
     * 当你不打算继续写代码了，想退出虚拟环境，则在虚拟环境内打```> deactivate```即可
     
10. 注意， 在git push的时候请不要直接在CareerGo-Demo目录下```$ git add .```， 因为这样会把你的virtualenv文件也一起commit上来，而我不知道不同的系统的virtualenv代码是不是一样的，因此最好不要这样。反之，我们的所有项目相关的代码都放在src文件夹下，因此只需要```git add src/.```就好了。

11. 所有的django projects只要activate好了，就可以直接startserver来查看了，而你从github上clone的src文件夹里面就已经是一个初始化完成了的django project，我们现在可以去看看能不能跑了。输入以下命令之后命令行会返回你localhost的地址，把那个copy进浏览器就能看到"The install worked successfully! Congratulations!"字段，说明你的django已经设置完成并且server能成功运行了

    ```$ (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo> python manage.py runserver  ```
    
