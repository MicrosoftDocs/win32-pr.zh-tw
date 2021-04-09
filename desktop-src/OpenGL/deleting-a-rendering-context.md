---
title: 刪除轉譯內容
description: 下列程式碼範例示範如何在 OpenGL 視窗關閉時刪除 OpenGL 轉譯內容。 它是用來建立轉譯內容並使其成為最新的案例接續。
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621abd0de46c874f40568f8361191b25df329f0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839072"
---
# <a name="deleting-a-rendering-context"></a><span data-ttu-id="d0042-106">刪除轉譯內容</span><span class="sxs-lookup"><span data-stu-id="d0042-106">Deleting a Rendering Context</span></span>

<span data-ttu-id="d0042-107">下列程式碼範例示範如何在 OpenGL 視窗關閉時刪除 OpenGL 轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="d0042-107">The following code sample shows how to delete an OpenGL rendering context when an OpenGL window is closed.</span></span> <span data-ttu-id="d0042-108">它是用來 [建立轉譯內容並使其成為最新](creating-a-rendering-context-and-making-it-current.md)的案例接續。</span><span class="sxs-lookup"><span data-stu-id="d0042-108">It is a continuation of the scenario used in [Creating a Rendering Context and Making It Current](creating-a-rendering-context-and-making-it-current.md).</span></span>


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



 

 




