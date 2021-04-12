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
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372362"
---
# <a name="porting-rendering-contexts"></a>移植轉譯內容

X 視窗系統和 Windows 會透過轉譯內容呈現。 六個 GLX 函式會管理轉譯內容，其中有五個都有對等的 Windows 函數。

下表列出 GLX 轉譯函數及其對等的 Windows 函數。



| GLX 轉譯內容函式                                                                            | Windows 轉譯內容函式                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXCoNtext **glXCopyCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *src*、GLXCoNtext *dst*、GLuint *mask*)             | 不適用。                                                         |
| GLXCoNtext **glXCreateCoNtext** ( 顯示 *\* dpy*、XVisualInfo *\* vis*、GLXCoNtext *shareList*、Bool *direct*)  | HGLRC [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) ( HDC *hdc*)           |
| void **glXDeleteCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *ctx*)                                               | BOOL [**wglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) ( HGLRC *HGLRC*)        |
| GLXCoNtext **glXGetCurrentCoNtext** (*void*)                                                                | HGLRC [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) (*VOID*)       |
| GLXDrawable **glXGetCurrentDrawable** (*void*)                                                              | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) (*VOID*)                   |
| Bool **glXMakeCurrent** ( 顯示 *\* dpy*、GLXDrawable *draw*、GLXCoNtext *ctx*)                               | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) ( HDC *hdc*，HGLRC *HGLRC*)  |



 

傳回型別和其他類型在 X 視窗系統中的名稱與 Windows 中的名稱不同。 您可以搜尋 GLXCoNtext 的出現位置，以協助找出需要移植的程式碼部分。

下列各節比較 X 視窗系統程式中的轉譯內容程式碼範例，以及將程式碼移植到 Windows 之後的相同程式碼。

如需呈現內容的詳細資訊， [請參閱轉譯](rendering-contexts.md)內容。

 

 




