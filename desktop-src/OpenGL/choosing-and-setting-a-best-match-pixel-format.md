---
title: 選擇和設定 Best-Match 像素格式
description: 本主題說明將裝置內容符合像素格式的程式。
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- Windows 上的 OpenGL，圖元
- 最符合的像素格式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966797"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a><span data-ttu-id="3d48e-105">選擇和設定 Best-Match 像素格式</span><span class="sxs-lookup"><span data-stu-id="3d48e-105">Choosing and Setting a Best-Match Pixel Format</span></span>

<span data-ttu-id="3d48e-106">本主題說明將裝置內容符合像素格式的程式。</span><span class="sxs-lookup"><span data-stu-id="3d48e-106">This topic explains the procedure for matching a device context to a pixel format.</span></span>

<span data-ttu-id="3d48e-107">**若要取得裝置內容與像素格式的最佳比對**</span><span class="sxs-lookup"><span data-stu-id="3d48e-107">**To obtain a device context's best match to a pixel format**</span></span>

1.  <span data-ttu-id="3d48e-108">在 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 結構中指定所需的像素格式。</span><span class="sxs-lookup"><span data-stu-id="3d48e-108">Specify the desired pixel format in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure.</span></span>
2.  <span data-ttu-id="3d48e-109">呼叫 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)。</span><span class="sxs-lookup"><span data-stu-id="3d48e-109">Call [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

    <span data-ttu-id="3d48e-110">**ChoosePixelFormat** 函式會傳回像素格式索引，然後您可以將其傳遞至 [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) ，以將最佳像素格式比對設定為裝置內容的目前像素格式。</span><span class="sxs-lookup"><span data-stu-id="3d48e-110">The **ChoosePixelFormat** function returns a pixel format index, which you can then pass to [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) to set the best pixel format match as the device context's current pixel format.</span></span>

<span data-ttu-id="3d48e-111">下列程式碼範例顯示如何執行上述步驟。</span><span class="sxs-lookup"><span data-stu-id="3d48e-111">The following code sample shows how to carry out the above steps.</span></span>


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




