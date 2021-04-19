---
title: Windows 轉譯內容程式碼範例
description: 下列程式碼範例顯示上一節中的 GLX 轉譯內容程式碼在移植到 Windows 時的外觀。
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- 轉譯內容
- 移植至 OpenGL，轉譯內容
- OpenGL 移植，轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0423f7458538f903a339f2f82dbff1c86c0626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966179"
---
# <a name="windows-rendering-context-code-sample"></a><span data-ttu-id="7a021-106">Windows 轉譯內容程式碼範例</span><span class="sxs-lookup"><span data-stu-id="7a021-106">Windows Rendering Context Code Sample</span></span>

<span data-ttu-id="7a021-107">下列程式碼範例顯示上一節中的 GLX 轉譯內容程式碼在移植到 Windows 時的外觀。</span><span class="sxs-lookup"><span data-stu-id="7a021-107">The following code sample shows how the GLX rendering context code in the previous section looks when it has been ported to Windows.</span></span>


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



 

 




