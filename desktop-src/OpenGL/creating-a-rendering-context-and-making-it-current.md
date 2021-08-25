---
title: 建立轉譯內容並使其成為最新的
description: 下列程式碼範例示範如何建立 OpenGL 轉譯內容，以回應 WM \_ 建立訊息。
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1768506eba506506a7198fbccc7dfefc0491adc96dd1e7bd03d2ec2aa5df8eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868788"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>建立轉譯內容並使其成為最新的

下列程式碼範例示範如何建立 OpenGL 轉譯內容，以回應 WM \_ 建立訊息。 請注意，您必須先設定像素格式，然後再建立轉譯內容。 另請注意，在此案例中，裝置內容不會在本機釋放;當視窗關閉時，您會在將轉譯內容設為最新狀態之後釋出它。 如需詳細資訊，請參閱 [刪除轉譯內容](deleting-a-rendering-context.md)。 最後，請注意，您可以使用本機變數作為裝置內容和轉譯內容控制碼，因為使用 [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) 和 [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) 函式時，您可以視需要取得這些內容的控制碼。

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

 

 




