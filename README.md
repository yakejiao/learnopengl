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

learnopengl教程：https://learnopengl-cn.github.io/01%20Getting%20started/04%20Hello%20Triangle/#_3

## 创建macOs工程

## 创建main.cpp文件

## 添加依赖Header Search Paths

/usr/local/include
/usr/local/Cellar/glfw/3.3.4/lib
/usr/local/Cellar/glew/2.2.0/lib


## 添加Library Search Paths

/usr/local/Cellar/glew/2.2.0_1/lib
/usr/local/Cellar/glfw/3.3.4/lib


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


### 图形渲染管线
图形渲染管线可以被划分为两个主要部分：
* 第一部分把你的3D坐标转换为2D坐标
* 第二部分是把2D坐标转变为实际的有颜色的像素。


# 3. Shaders

着色器(Shader)是运行在GPU上的小程序。
这些小程序为图形渲染管线的某个特定部分而运行。从基本意义上来说，着色器只是一种把输入转化为输出的程序。着色器也是一种非常独立的程序，因为它们之间不能相互通信；它们之间唯一的沟通只有通过输入和输出。

## GLSL(着色器语言)

着色器是使用一种叫GLSL的类C语言写成的。

着色器是使用一种叫GLSL的类C语言写成的。GLSL是为图形计算量身定制的，它包含一些针对向量和矩阵操作的有用特性。着色器的开头总是要声明版本，接着是输入和输出变量、uniform和main函数。每个着色器的入口点都是main函数，在这个函数中我们处理所有的输入变量，并将结果输出到输出变量中。如果你不知道什么是uniform也不用担心，我们后面会进行讲解。

一个典型的着色器有下面的结构：

```
#version version_number
in type in_variable_name;
in type in_variable_name;

out type out_variable_name;

uniform type uniform_name;

int main()
{
  // 处理输入并进行一些图形操作
  ...
  // 输出处理过的结果到输出变量
  out_variable_name = weird_stuff_we_processed;
}
```


# 4.




# 中英对照

* Vector 向量。基本的定义就是一个方向，或者更正式的说，向量有一个方向(Direction)和大小(Magnitude，也叫做强度或长度)。
* Direction 方向 
* Magnitude 大小(也叫做强度或长度) 
* Dimension  维度
* Position Vector 位置向量
* Negate 向量取反

* Scalar 标量，只是一个数字（或者说是仅有一个分量的向量）。
* Unit Vector 单位向量， 单位向量有一个特别的性质——它的长度是1。可以用任意向量的每个分量除以向量的长度得到它的单位向量n̂ ：
n̂ =v¯||v¯||

我们把这种方法叫做一个向量的标准化(Normalizing)

* Normalizing 标准化

* Orthogonal 正交

* Pythagoras Theorem 勾股定理

* Identity Matrix 单位矩阵
* Scaling 缩放
* Translation 位移
