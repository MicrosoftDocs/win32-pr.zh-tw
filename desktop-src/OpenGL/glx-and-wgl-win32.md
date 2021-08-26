---
title: GLX 和 WGL/Windows
description: 某些 WGL 函式和 Windows 函式，類似于 GLX X 視窗函式的功能更多或更少。 下列清單顯示 GLX 函式及其對應的 WGL/Windows 函數（如果有的話）。
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- Windows 上的 OpenGL，GLX 函式
- GLX 函式 OpenGL
- WGL 函式（相較于 GLX 函數）
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24b88caeed9aea7bae8e38f73818ac180aad9117806508f40550b02eb8a4e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035380"
---
# <a name="glx-and-wglwindows"></a>GLX 和 WGL/Windows

某些 WGL 函式和 Windows 函式，類似于 GLX X 視窗函式的功能更多或更少。 下列清單顯示 GLX 函式及其對應的 WGL/Windows 函數（如果有的話）。



| GLX 函式             | WGL/Windows 函式                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                              |
| **glXCopyCoNtext**        |                                                                                                                                                             |
| **glXCreateCoNtext**      | [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                                |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)  / [ **CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                     |
| **glXDestroyCoNtext**     | [**wglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                                |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                        |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                          |
| **glXGetCurrentCoNtext**  | [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                        |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                                  |
| **glXIsDirect**           |                                                                                                                                                             |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                                    |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                          |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)  / [ **wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)                                                           |
| **glXWaitGL**             |                                                                                                                                                             |
| **glXWaitX**              |                                                                                                                                                             |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                                    |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)  / [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)和 [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)  /  [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                                |
|                           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                                    |
|                           | [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)                                                                                                              |
|                           | [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)                                                                                                                      |



 

如需詳細資訊，請參閱 *移植指南*。

 

 