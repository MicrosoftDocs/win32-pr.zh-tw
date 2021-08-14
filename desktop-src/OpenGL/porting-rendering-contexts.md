---
title: 移植轉譯內容
description: 移植轉譯內容
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- 轉譯內容 OpenGL、移植
- Windows 上的 OpenGL，轉譯內容
- 移植至 OpenGL，轉譯內容
- OpenGL 移植，轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fcb6a70f6858ac9c11258c681345ee88a8807c91230f8d3d35fc579ab3371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358338"
---
# <a name="porting-rendering-contexts"></a>移植轉譯內容

X 視窗系統和 Windows 會透過轉譯內容呈現。 六個 GLX 函式會管理轉譯內容，其中有五個會有對等的 Windows 函式。

下表列出 GLX 轉譯函數及其對等的 Windows 函數。



| GLX 轉譯內容函式                                                                            | Windows 轉譯內容函式                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXCoNtext **glXCopyCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *src*、GLXCoNtext *dst*、GLuint *mask*)             | 不適用。                                                         |
| GLXCoNtext **glXCreateCoNtext** ( 顯示 *\* dpy*、XVisualInfo *\* vis*、GLXCoNtext *shareList*、Bool *direct*)  | HGLRC [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) ( HDC *hdc*)           |
| void **glXDeleteCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *ctx*)                                               | BOOL [**wglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) ( HGLRC *HGLRC*)        |
| GLXCoNtext **glXGetCurrentCoNtext** (*void*)                                                                | HGLRC [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) (*VOID*)       |
| GLXDrawable **glXGetCurrentDrawable** (*void*)                                                              | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) (*VOID*)                   |
| Bool **glXMakeCurrent** ( 顯示 *\* dpy*、GLXDrawable *draw*、GLXCoNtext *ctx*)                               | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) ( HDC *hdc*，HGLRC *HGLRC*)  |



 

傳回型別和其他型別在 X 視窗系統中具有不同于 Windows 的名稱。 您可以搜尋 GLXCoNtext 的出現位置，以協助找出需要移植的程式碼部分。

下列各節比較 X 視窗系統程式中的轉譯內容程式碼範例，以及將它移植到 Windows 之後的相同程式碼。

如需呈現內容的詳細資訊， [請參閱轉譯](rendering-contexts.md)內容。

 

 




