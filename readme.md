# Task 1

## 简介

选取了自己设计的两个简化模型，用于将形式化的数据实体转化为HTML表单

首先是数据实体的元模型

![image-20231204033804806](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204033804806.png)

非常直观，一个实体有自己的名字，包含若干属性，属性有姓名和类型，实体归属于一种特定的datamodel

之后是简化的HTML表格

![image-20231204034525944](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204034525944.png)

就是简化的HTML表格，表格有若干表格元素，元素又分为三种

## metamodel建模  ecore文件

和上述建模类似

![image-20231204034745805](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204034745805.png)

![image-20231204034758238](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204034758238.png)

## TAL脚本

见图

![1](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/1.png)

## input&output

输入（部分）

![image-20231204035036254](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204035036254.png)

输出

![image-20231204035057859](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/image-20231204035057859.png)

# Task 2

## 简介

选取了完善Acceleo Tutorial的样例，为类添加了构造函数和setter，支持生成继承和接口实现关系，为接口也生成了单独文件。

## model.uml

未修改，使用视频中的样例

![2asdasdasd](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042242345.png)

## umlToBeans.mtl

运行的main入口部分

额外增加了对interface的代码生成，细节在generate.mtl中

![2](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/2.png)

## generate.mtl

在class的代码生成部分，除视频中的样例外，增加了setter和构造函数

![image-20231204224413247](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042245294.png)

定义了三个模板来帮助获取类的父类和接口

![image-20231204224432964](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042244012.png)

为每个类生成了其父类和接口的代码

![image-20231204224445220](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042245892.png)

为interface也提供了代码生成

仿照class的配置定义了一些query辅助

![image-20231204225444569](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042259726.png)

interface的代码生成部分

![image-20231204225607243](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042259510.png)

## 生成结果

全部生成的代码

![image-20231204225909720](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042259760.png)

Person类，展示其setter和构造函数

![image-20231204225937544](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042259603.png)

NeedALicense接口，展示接口实现

![image-20231204225954998](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042259040.png)

Car类，展示继承和接口

![image-20231204230009326](https://raw.githubusercontent.com/The-Sunspot/IMAGE/main/202312042300373.png)
