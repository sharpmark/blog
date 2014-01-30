SIMPLE: Sharpmark IMage Processing Library Experience
Sharpmark图像处理库(体验版)

项目说明：平台无关的图像处理库。
最新版本：0.0.1
开发语言：ISO-C++
软件平台：Windows, Linux(未在WinVista下实验)
编写目的：这个框架是为了本科毕业设计而开发的。同时也为研究生阶段的图像处理和模式识别打一些基础。也希望可以在这个框架上，建立一些实用的程序。
软件说明：本程序库是建立在Philip Romanik和Amy Muntz的图像处理框架基础上的。虽然几乎是完全重写的，但是因为在很大程度上借鉴了其软件架构和一些思路，所以随后也附上他们的版权声明。
项目地址：Sharpmark-Simple at google Code
参考资料：Applied C++
版权声明：
Copyright (c) 2003 Philip Romanik, Amy Muntz

Permission to use, copy, modify, distribute, and sell this software and its documentation for any purpose is hereby granted without fee, provided that (i) the above copyright notices and this permission notice appear in all copies of the software and related documentation, and (ii) the names of Philip Romanik and Amy Muntz may not be used in any advertising or publicity relating to the software without the specific, prior written permission of Philip Romanik and Amy Muntz.

Copyright(c) 2007 Sharp Mark(Liu Jiong)

Permission to use, copy, modify, distribute and sell this software and its documentation for any purpose is hereby granted without fee, provided that the above copyright notice appear in all copies and that both that copyright notice and this permission notice appear in supporting documentation. Sharp Mark makes no representations about the suitability of this software for any purpose. It is provided "as is" without express or implied warranty.

## 单元测试和一些公共组件 
0. 前期准备好之后，今天正式开始了simple的开发。规划为正式程序文件在namespace simple下，namespace simple_test下为测试程序。版本定为0.0.1。

1. 作了单元测试部分(Unit Test)。设计了UnitTestFunction, UnitTest类，以及辅助类ElapsedTime。

2. 开始编写公共组件部分的类。完成了Point, Rect, BString类。并完成了三个类的单元测试。以及单元测试实例。

## 主要图像组件
0. 这两天写了图像储存和现实的主要组件。(部分类是模板类，不过没有标出)。写崩溃了，明天去爷爷家打扫卫生，顺便休息一下，然后做一些其它部分的设计。

1. 内存管理部分，设计了_AllocatorBase, _Allocator, Alloc类。

2. 图像储存组件部分，完成了ImageSotrageBase, RectImageStorage, ImageStorage类。并完成了三个类的迭代器Row_Iterator, PixelIterator，线程锁定工具RectImageStorageLocker和ImageStorageLocker。


3. 图像类。Image也写完了。

4. 异常处理类Exception以及其子类BoundsException, UnsupportedException。