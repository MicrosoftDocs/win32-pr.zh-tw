---
title: GLX 像素格式的程式碼範例
description: 下列程式碼範例顯示 X 視窗系統 OpenGL 程式如何使用 GLX 的視覺化/像素格式函式。
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- 移植至 OpenGL，圖元
- OpenGL 移植，圖元
- X 視窗系統（圖元）
- GLX 函式，圖元
- 圖元、GLX 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035382"
---
# <a name="glx-pixel-format-code-sample"></a>GLX 像素格式的程式碼範例

下列程式碼範例顯示 X 視窗系統 OpenGL 程式如何使用 GLX 的視覺化/像素格式函式。


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



視覺效果可以用來建立視窗和轉譯內容。

 

 




