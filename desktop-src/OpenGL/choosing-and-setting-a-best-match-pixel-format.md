---
title: 選擇和設定 Best-Match 像素格式
description: 本主題說明將裝置內容符合像素格式的程式。
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- Windows 上的 OpenGL，圖元
- 最符合的像素格式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258364e18ff38cb67edd1315f261a55a91f58fe940b026e1fcb7b63ed2e12eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063298"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>選擇和設定 Best-Match 像素格式

本主題說明將裝置內容符合像素格式的程式。

**若要取得裝置內容與像素格式的最佳比對**

1.  在 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 結構中指定所需的像素格式。
2.  呼叫 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)。

    **ChoosePixelFormat** 函式會傳回像素格式索引，然後您可以將其傳遞至 [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) ，以將最佳像素格式比對設定為裝置內容的目前像素格式。

下列程式碼範例顯示如何執行上述步驟。


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



 

 




