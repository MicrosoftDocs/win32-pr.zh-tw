---
title: 翻譯 GLX 程式庫
description: 翻譯 GLX 程式庫
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- Windows 上的 OpenGL、GLX 程式庫
- 移植至 OpenGL、GLX 程式庫
- OpenGL 移植，GLX 程式庫
- GLX 程式庫 OpenGL
- Xlib 函式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6864173cf85e0db24e77c53a7627a90e6110a1ff3ec3d94a7c85e456f98ffd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034448"
---
# <a name="translating-the-glx-library"></a>翻譯 GLX 程式庫

OpenGL X Window 系統程式會使用 OpenGL 擴充功能搭配 X 視窗系統 (GLX) 程式庫。 此程式庫是一組函式和常式，可初始化像素格式、控制項轉譯，以及執行其他 OpenGL 特定的工作。 它會藉由管理視窗控制碼和轉譯內容，將 OpenGL 程式庫連接到 X 視窗系統。 您必須將這些函數轉譯為其對等的 Windows 函式。 下表列出 X 視窗系統 GLX 函式及其對等的 Windows 函數。



| GLX/Xlib 函式         | Windows 函式                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyCoNtext**        | 不適用。                                                                                                                                        |
| **glXCreateCoNtext**      | [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyCoNtext**     | [**wglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentCoNtext**  | [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | 不適用。                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)、 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)、 [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)、 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| 不適用。           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

某些 GLX 函式沒有相等的 Windows 函數。 若要將這些函式移植至 Windows，請重寫您的程式碼以達成相同的功能。 例如， **glXWaitGL** 沒有對等的 Windows 函式，但是您可以藉由呼叫 [**glFinish**](glfinish.md)來達到相同的結果，執行任何擱置中的 OpenGL 命令。

下列主題描述如何移植設定像素格式的 GLX 函式，以及管理轉譯內容、pixmaps 和點陣圖。

 

 