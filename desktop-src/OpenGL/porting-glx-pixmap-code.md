---
title: 移植 GLX Pixmap 程式碼
description: 移植 GLX Pixmap 程式碼
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- Windows 上的 OpenGL、pixmaps
- 移植至 OpenGL、pixmaps
- OpenGL 移植，pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024015"
---
# <a name="porting-glx-pixmap-code"></a>移植 GLX Pixmap 程式碼

X 視窗系統使用 *pixmaps*，這是以三維位陣列形式呈現的非螢幕虛擬繪圖表面。 您可以將 pixmap 視為一堆點陣圖：二維陣列，其中每個圖元的值都是從0到2N1，其中 N 是 pixmap 的深度。

針對 OpenGL 程式，您可以使用 GLX 函式（ **glXCreateGLXPixmap** 和 **glXDestroyGLXPixmap**）來建立和終結用於關閉螢幕轉譯的 GLX pixmaps。

Windows 使用與裝置無關的點陣圖，其提供與 X 視窗系統 pixmaps 相同的功能。 使用標準的 Windows 點陣圖函式來建立和終結點陣圖。

下表列出 GLX pixmap 函數及其對等的 Windows 點陣圖函數。



| GLX pixmap 和 font-family 函數                                                          | Windows 點陣圖和字型函數                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap** ( Display *\* dpy*，XVisualInfo *\* vis*，Pixmap *Pixmap*)  | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) hdc *hdc*、LPBITMAPINFOHEADER *lpbmih*、DWORD *fdwInit*、CONST BYTE *\* lpbInit*、LPBITMAPINFO *lpbmi*、UINT * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) hdc *hdc*、LPBITMAPINFO *lpbmi*、dword *fInit*、dword *iUsage*) <br/> |
| void **glXDestroyGLXPixmap** ( 顯示 *\* dpy*、GLXPixmap *pix*)                         | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) ( HGDIOBJ *hObject*)                                                                                                                                                                                                                                   |



 

 

