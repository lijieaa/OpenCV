# 1.新建Win32空项目![](/assets/1.3.1.png)![](/assets/1.3.2.png)![](/assets/1.3.3.png)![](/assets/1.3.4.png)

# 2.引用OpenCV SDK

## 2.1 新建属性管理文件，以便后续工程引用OpenCV SDK![](/assets/1.3.5.png)

## 2.2双击OpenCV属性管理器文件,添加附加包含目录和链接库

![](/assets/1.3.6.png)![](/assets/1.3.7.png)![](/assets/1.3.8.png)**为什么选择opencv\_world320d.lib，不选择opencv\_world320.lib？原因是opencv以d结束的库代表调试版本。**

## 2.3 新建main.cpp，加入如下代码，开始我们的程序

\#include&lt;iostream&gt;

\#include &lt;opencv2/core/core.hpp&gt;

\#include &lt;opencv2/highgui/highgui.hpp&gt;

using namespace cv;

int main\(\)

{

```
// 读入一张图片

Mat img = imread("1.jpg");

// 创建一个名为 "HelloWorld"窗口  

namedWindow("HelloWorld");

// 在窗口中显示一个美女

imshow("HelloWorld", img);

// 等待输入任意键退出

waitKey();
```

}

**注意运行的时候选择X64,因为前面所做的配置是针对X64的。如果在运行时出现如下问题，请拷贝OpenCV SDK下面的opencv\_world320.dll到程序生成目录。**

![](/assets/1.3.9.png)



# 3.见证奇迹时刻



![](/assets/1.3.10png)

