---
title: 移植裝置內容和像素格式
description: 移植裝置內容和像素格式
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- 移植至 OpenGL，圖元
- OpenGL 移植，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969842"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>移植裝置內容和像素格式

Microsoft 適用于 Windows 之 OpenGL 的每個視窗都有自己目前的像素格式。 像素格式是由 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構所定義。 因為每個視窗都有自己的像素格式，所以您會取得裝置內容、設定裝置內容的像素格式，然後建立裝置內容的 OpenGL 轉譯內容。 轉譯內容會自動使用其裝置內容的像素格式。

X 視窗系統也會使用資料結構 **XVisualInfo**，在視窗中指定圖元的屬性。 **XVisualInfo** 結構包含 **視覺化** 資料結構，描述如何在特定螢幕中使用色彩資源。

在 X 視窗系統中， **XVisualInfo** 是用來建立視窗，方法是將視窗設定為您想要的像素格式。 傳回的結構會用來建立視窗和轉譯內容。 在 Windows 中，您會先建立一個視窗，並取得視窗的控制碼 (HDC) 。 然後，會使用 HDC 來設定視窗的像素格式。 轉譯內容會使用視窗的像素格式。

下表比較 X 視窗系統和 GLX 視覺化函式與其對等的 Windows 像素格式函數。



| X 視窗/GLX 視覺化函式                                                                                     | Windows 像素格式函數                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **GlXChooseVisual** ( 顯示 *\* dpy*、int *screen*、int *\* attribList*)                                | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) ( HDC *hdc*，PIXELFORMATDESCRIPTOR *\* ppfd*)                                       |
| int **glXGetConfig** ( 顯示 *\* dpy*、XVisualInfo *\* vis*、int *\* attribList*、int *\* 值*)                       | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) ( HDC *Hdc*、Int *iPixelFormat*、UINT *n*、LPPIXELFORMATDESCRIPTOR *ppfd*)  |
| XVisualInfo \* **XGetVisualInfo** ( 顯示 *\* dpy*、long *vinfo \_ mask*、XVisualInfo *\* vinfo \_ templ*、int *\* nitems*)  | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) ( HDC *hdc*)                                                                            |
| 建立視窗時，會使用 **glxChooseVisual** 所傳回的 *視覺效果*。                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) ( HDC *Hdc*、int *iPixelFormat*、PIXELFORMATDESCRIPTOR *\* ppfd*)                         |



 

下列各節提供 X 視窗系統程式的像素格式程式碼片段範例，以及將程式碼移植到 Windows 之後的相同程式碼。

-   [GLX 像素格式的程式碼範例](glx-pixel-format-code-sample.md)
-   [Windows 像素格式的程式碼範例](win32-pixel-format-code-sample.md)

如需像素格式的詳細資訊，請參閱 [像素格式](pixel-formats.md)。

 

 




