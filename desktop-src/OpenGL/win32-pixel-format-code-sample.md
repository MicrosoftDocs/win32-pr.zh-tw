---
title: Windows 像素格式的程式碼範例
description: 下列程式碼範例顯示使用 Windows 函式設定像素格式的函式。
ms.assetid: fa863999-72f1-4280-b278-d9336f62108d
keywords:
- 圖元 OpenGL、Windows 範例
- 移植至 OpenGL，圖元
- OpenGL 移植，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4328976a3622d19c3482aa2845c2094975dd7f74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301028"
---
# <a name="windows-pixel-format-code-sample"></a><span data-ttu-id="4fe55-106">Windows 像素格式的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="4fe55-106">Windows Pixel Format Code Sample</span></span>

<span data-ttu-id="4fe55-107">下列程式碼範例顯示使用 Windows 函式設定像素格式的函式：</span><span class="sxs-lookup"><span data-stu-id="4fe55-107">The following code sample shows a function that sets the pixel format using Windows functions:</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX; 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




