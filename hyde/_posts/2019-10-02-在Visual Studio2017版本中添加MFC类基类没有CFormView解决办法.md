## 在Visual Studio2017版本中添加MFC类基类没有CFormView解决办法

[TOC]



#### 问题描述：

![](https://raw.githubusercontent.com/Zhangyueee/Storage/master/VS2017添加类1.jpg)

在VS2017版本添加MFC类基类是没有CFormView的

#### 解决办法：手动添加

既然使用IDE添加没有这个基类，我们可以自己手动添加

我们需要自己写两个文件添加到工程

文件命名：***ClassName***.h       ***ClassName***.cpp

文件内容：

***ClassName***.h 

```c++
#pragma once
#include <afxext.h>
#include <afxext.h>



// 类窗体视图

class ClassName : public CFormView
{
	DECLARE_DYNCREATE(ClassName)

protected:
	ClassName(); // protected constructor used by dynamic creation

public:
	enum
	{
		IDD = IDD_YourDialog
	};

protected:

public:
	afx_msg int OnCreate(LPCREATESTRUCT lpCreateStruct);
};
```

 ***ClassName***.cpp

```c++
// ClassName.cpp : 实现文件
//

#include "stdafx.h"
#include "cg2019ZYCircle.h"
#include "cg2019ZYCircleDoc.h"
#include "CCgInPutControl.h"

// ClassName

IMPLEMENT_DYNCREATE(ClassName, CFormView)

ClassName::ClassName()
	: CFormView(ClassName::IDD)
{
}
```

添加方法：

![](https://raw.githubusercontent.com/Zhangyueee/Storage/master/VS2017添加类2.png)

