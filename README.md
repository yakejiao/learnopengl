# learnopengl

learnopengl

## 1.glTest1

本节介绍opengl开发环境搭建

### 流行库：

* glfw  
* glad  

### 问题参考:  

glxinfo not found： http://www.mshah.io/comp/Spring18/graphics/Lab/1/mac.html

### 参考资料：
* （1）https://learnopengl-cn.github.io/01%20Getting%20started/03%20Hello%20Window/  
* （2）https://www.jianshu.com/p/891d630e30af

# 2.glTriangle

## 创建macOs工程

## 创建main.cpp文件

## 添加依赖header

/usr/local/include
/usr/local/Cellar/glfw/3.3.4/lib
/usr/local/Cellar/glew/2.2.0/lib

## Build Phases -> Link Binary With Libraries

### Add libGLEW2.2.0.dylib

* open Terminal.
* `find / -name libGLEW*`
* Find Real file, but link file is not available.
* `open /usr/local/Cellar/glew/2.2.0_1/lib`
* drag libGLEw.2.2.0.dylib to Frameworks.

### Add libglfw.3.3.dylib

* open Terminal.
*  `find / -name libglfw.*`
* Find Real file, but link file is not available.
* `open /usr/local/Cellar/glfw/3.3.4/lib`
* drag libglfw.3.3.dylib to Frameworks.

### 关于 search paths

#### 注意这个$(inherited)

这个是target在设置自己路径的时候如果加了这个，那么就是继承project里设置的路径。如果不需要继承就不加，要不然乱加有可能整混导致路径错误。

#### 带引号的路径和不带引号的路径 

带引号主要是预防路径里有空格导致本来一个路径变成了两个路径，因为空格分开就被解析位两个路径了。

#### recursive和non-recursive区别，就是是否在你设置的路径下递归搜索




# 3. glRectangle


# 4.
