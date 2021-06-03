# qt_ui_static_lib
qt界面静态库
===============
 
## 运行环境
 
>+ Qt版本：5.12
>+ vs版本：2017 enterprise 15.9.36
>+ QtCreator：4.8.0
>+ 操作系统：win10
 
 
### 功能
~~~
1.    将Qt界面封装成静态库，供其他qt程序调用
2.    本例子只是个简单的测试，功能自行在此基础上开发
~~~
 
### 主要步骤
+（1） qt ui静态库：在QtCreator中创建一个Qt界面设计类项目，然后修改.pro文件:
+   TEMPLATE = lib
+   CONFIGS += staticlib
+ 静态库头文件中需要将方法导出__declspec(dllexport)、Q_DECL_EXPORT（这部分不详，自行百度补习）
+   
+（2） 测试应用程序：在vs中新建一个QGuiApplication项目，并在.pro中加入上述生成的lib库:
+   LIBS += -L./lib
+   LIBS += -ltestWidget
 
 
