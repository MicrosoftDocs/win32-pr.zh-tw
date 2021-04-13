---
title: 建立轉譯內容並使其成為最新的
description: 下列程式碼範例示範如何建立 OpenGL 轉譯內容，以回應 WM \_ 建立訊息。
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301460"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a><span data-ttu-id="f34d2-105">建立轉譯內容並使其成為最新的</span><span class="sxs-lookup"><span data-stu-id="f34d2-105">Creating a Rendering Context and Making It Current</span></span>

<span data-ttu-id="f34d2-106">下列程式碼範例示範如何建立 OpenGL 轉譯內容，以回應 WM \_ 建立訊息。</span><span class="sxs-lookup"><span data-stu-id="f34d2-106">The following code sample shows how to create an OpenGL rendering context in response to a WM\_CREATE message.</span></span> <span data-ttu-id="f34d2-107">請注意，您必須先設定像素格式，然後再建立轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="f34d2-107">Notice that you set up the pixel format before creating the rendering context.</span></span> <span data-ttu-id="f34d2-108">另請注意，在此案例中，裝置內容不會在本機釋放;當視窗關閉時，您會在將轉譯內容設為最新狀態之後釋出它。</span><span class="sxs-lookup"><span data-stu-id="f34d2-108">Also notice that in this scenario the device context is not released locally; you release it when the window is closed, after making the rendering context not current.</span></span> <span data-ttu-id="f34d2-109">如需詳細資訊，請參閱 [刪除轉譯內容](deleting-a-rendering-context.md)。</span><span class="sxs-lookup"><span data-stu-id="f34d2-109">For more information, see [Deleting a Rendering Context](deleting-a-rendering-context.md).</span></span> <span data-ttu-id="f34d2-110">最後，請注意，您可以使用本機變數作為裝置內容和轉譯內容控制碼，因為使用 [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) 和 [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) 函式時，您可以視需要取得這些內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f34d2-110">Finally, notice that you can use local variables for the device context and rendering context handles, because with the [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) and [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) functions you can obtain handles to those contexts as needed.</span></span>

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




