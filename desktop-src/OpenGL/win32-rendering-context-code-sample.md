---
title: Windows轉譯內容程式碼範例
description: 下列程式碼範例顯示在上一節中 GLX 轉譯內容程式碼已移植至 Windows 時的外觀。
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- 轉譯內容
- 移植至 OpenGL，轉譯內容
- OpenGL 移植，轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9693b140083210ce0865b18463f4595c2f1fc731c8fc1d837f61342ede50b9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794691"
---
# <a name="windows-rendering-context-code-sample"></a>Windows轉譯內容程式碼範例

下列程式碼範例顯示在上一節中 GLX 轉譯內容程式碼已移植至 Windows 時的外觀。


```C++
HGLRC hRC;           // rendering context variable  
 
/* Create and initialize a window */ 
        
/* Window message switch in a window procedure */ 
case WM_CREATE:      // Message when window is created  
{ 
    HDC hDC, hDCTemp;    // device context handles   
 
    /* Get the handle of the windows device context. */ 
    hDC = GetDC(hWnd); 
 
    /* Create a rendering context and make it the current context */  
    hRC = wglCreateContext(hDC); 
    if (!hRC)  
    { 
        MessageBox(NULL, "Cannot create context.", "Error", MB_OK); 
        return FALSE; 
    }  
    wglMakeCurrent(hDC, hRC); 
} 
break; 
        
        .    
case WM_DESTROYED:   // Message when window is destroyed  
{ 
    HGLRC hRC        // rendering context handle  
    HDC   hDC;       // device context handle  
 
    /* Release and free the device context and rendering context. */ 
    hDC = wglGetCurrentDC; 
    hRC = wglGetCurrentContext; 
 
    wglMakeCurrent(NULL, NULL); 
 
    if (hRC) 
        wglDeleteContext(hRC); 
 
    if (hDC) 
        ReleaseDC(hWnd, hDC); 
 
    PostQuitMessage (0); 
} 
break;
```



 

 




