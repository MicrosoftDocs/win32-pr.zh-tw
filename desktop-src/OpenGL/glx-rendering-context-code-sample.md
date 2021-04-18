---
title: GLX 轉譯內容程式碼範例
description: 下列程式碼範例會示範 X 視窗系統 OpenGL 程式如何使用 GLX 轉譯內容函數。
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- 轉譯內容
- 移植至 OpenGL，轉譯內容
- OpenGL 移植，轉譯內容
- X 視窗系統，轉譯內容
- GLX 函式，呈現內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03259cb9b540db3076a0baa4122906e5aeb3e8f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965773"
---
# <a name="glx-rendering-context-code-sample"></a>GLX 轉譯內容程式碼範例

下列程式碼範例會示範 X 視窗系統 OpenGL 程式如何使用 GLX 轉譯內容函數。


```C++
Display *dpy;             /* display variable */ 
XVisualInfo *vi;          /* visual variable */ 
Window win;               /* window variable */ 
GLXDrawable drawable;     /* drawable variable */ 
GLXContext cx, cxTemp;    /* rendering context variables */ 
 
/* Code to open a display and get a visual. */ 
        
/* Create a GLX context. */ 
cx = glXCreateContext(dpy, vi, 0, GL_FALSE); 
if (!cx) { 
    fprintf(stderr, "Cannot create context.\n"); 
    exit(-1); 
} 
        
        .    
/* Connect the context to the window. */ 
glXMakeCurrent(dpy, win, cx); 
        
        .    
/* When it's time to destroy the rendering context. . . */ 
cx = glXGetCurrentContext; 
glXDestroyContext(dpy, cx);
```



 

 




