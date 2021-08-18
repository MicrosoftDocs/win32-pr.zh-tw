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
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012056"
---
# <a name="porting-glx-pixmap-code"></a>移植 GLX Pixmap 程式碼

X 視窗系統使用 *pixmaps*，這是以三維位陣列形式呈現的非螢幕虛擬繪圖表面。 您可以將 pixmap 視為一堆點陣圖：二維陣列，其中每個圖元的值都是從0到2N1，其中 N 是 pixmap 的深度。

針對 OpenGL 程式，您可以使用 GLX 函式（ **glXCreateGLXPixmap** 和 **glXDestroyGLXPixmap**）來建立和終結用於關閉螢幕轉譯的 GLX pixmaps。

Windows 使用與裝置無關的點陣圖，其提供與 X Window System pixmaps 相同的功能。 使用標準 Windows 點陣圖函數來建立和終結點陣圖。

下表列出 GLX pixmap 函式及其對等的 Windows 點陣圖函數。



| GLX pixmap 和 font-family 函數                                                          | Windows 點陣圖和字型函數                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap** ( Display *\* dpy*，XVisualInfo *\* vis*，Pixmap *Pixmap*)  | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) hdc *hdc*、LPBITMAPINFOHEADER *lpbmih*、DWORD *fdwInit*、CONST BYTE *\* lpbInit*、LPBITMAPINFO *lpbmi*、UINT * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) hdc *hdc*、LPBITMAPINFO *lpbmi*、dword *fInit*、dword *iUsage*) <br/> |
| void **glXDestroyGLXPixmap** ( 顯示 *\* dpy*、GLXPixmap *pix*)                         | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) ( HGDIOBJ *hObject*)                                                                                                                                                                                                                                   |



 

 

