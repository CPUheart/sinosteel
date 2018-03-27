# 项目介绍

这是一个以spring boot和react/node.js为基础，UI采用<a href="https://ant.design/index-cn">ant design</a>的全栈传统web应用框架。原作者为[DimitriZhao](https://github.com/DimitriZhao)。

             
# 项目截图       
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework0.png" />      
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework1.png" />  
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework2.png" />  
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework3.png" />  
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework4.png" />       
<img src="https://github.com/DimitriZhao/screenshots/blob/master/sinosteel/framework5.png" />   
                          
# 项目特点

本项目中服务端/客户端完全分离。其中：

## 服务端（后端）
无状态应用
面向服务的结构
注解风格       
采用JSON格式传输信息         
提供面向对象的实体开发基类        
多ORM用于不同场景
具有功能权限和数据权限机制        
自定义的数据权限控制注解        
封装了消息，数据分页及缓存等机制          

## 客户端
采用ES6语法   
单页面应用    
面向对象的开发风格      
标签页为主的展示风格    
通用的实体模型展示      
公共的用于文件上传，请求和权限工具             
可进行热部署          

# 技术栈
## 服务端   
基础：spring boot    
ORM：spring data jpa 和 mybatis        
缓存：redis      
权限：apache shiro（无状态应用）    
项目构建：apache maven      

## 客户端
react
redux-thunk 
react-redux-router
ant design
webpack
nginx

# 使用说明
该仓库中包含两个文件夹：“server” 和 “client”。“server” 文件夹为服务端项目，“client” 文件夹为客户端项目。两者都可以独立运行

## 服务端
“server” 文件夹中包含 “framework” 和 “framework-example” 两个Java工程。“framework” 是 “framework-example” 的依赖工程  
“framework-example” 是一个基于该框架所开发的项目 

运行服务端：

首先，安装MySql数据库，端口号设为3306，用户名为root，密码为空     
其次，安装redis，端口号设为6379，用户名和密码都为空         
(以上两步，如果已经安装了MySql或者redis，或者设置不同的话，可以直接到framework-example/src/main/resources/config中找到对应的配置文件修改配置。既然都已经安装了数据库和redis，说明肯定是会后端的配置了的~)                  
然后，创建framework数据库，并导入framework.sql         
最后，运行以下命令（在有IDE的情况下就直接import一个maven工程就好）      
                     
```             
$ cd framework-example               
$ mvn package              
$ cd framework-example/target               
$ java -jar framework-example-1.0.0.jar       
```               

服务端将在9016端口上运行             
                   
## 客户端:
“client” 文件夹是一个可在nodejs环境下运行的react项目 

运行客户端开发模式:  

```            
$ cd framework-webclient
$ npm install             
$ npm run dev            
```           
               
客户端将在3000端口上运行，访问localhost:3000即可看到登录界面                  
                
部署生产环境:  

```                  
$ cd framework-webclient                 
$ npm install                     
$ npm run build         
```                       

生成的文件位于 dist 文件夹中, 可在nginx中部署                  

# 开发指南
如何使用框架开发，请参考<a href="https://github.com/caochun/sinosteel/blob/master/README-Dev_Guide.md">开发指南</a>

# 项目引用                 
https://github.com/OwlAford/easy-react-desktop                          
https://github.com/davezuko/react-redux-starter-kit                

**在此表示感谢！**        

# 项目许可
MIT许可证，就是随便用的意思             