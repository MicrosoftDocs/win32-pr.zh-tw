---
title: 刪除轉譯內容
description: 下列程式碼範例示範如何在 OpenGL 視窗關閉時刪除 OpenGL 轉譯內容。 它是用來建立轉譯內容並使其成為最新的案例接續。
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6821e51ad2493bc2ec3ce1c3ce9b448faee1079ae3771cf3290874fcb9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889238"
---
# <a name="deleting-a-rendering-context"></a>刪除轉譯內容

下列程式碼範例示範如何在 OpenGL 視窗關閉時刪除 OpenGL 轉譯內容。 它是用來 [建立轉譯內容並使其成為最新](creating-a-rendering-context-and-making-it-current.md)的案例接續。


```C++
// a window is about to be destroyed  
case WM_DESTROY: 
    { 
    // local variables  
    HGLRC    hglrc; 
    HDC      hdc ; 
 
    // if the thread has a current rendering context ...  
    if(hglrc = wglGetCurrentContext()) { 
 
        // obtain its associated device context  
        hdc = wglGetCurrentDC() ; 
 
        // make the rendering context not current  
        wglMakeCurrent(NULL, NULL) ; 
 
        // release the device context  
        ReleaseDC (hwnd, hdc) ; 
 
        // delete the rendering context  
        wglDeleteContext(hglrc); 
 
        }
```



 

 




