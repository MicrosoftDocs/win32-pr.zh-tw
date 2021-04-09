---
title: 在 Double-Buffered OpenGL 視窗中繪製文字
description: 您可以藉由為字型中的選定字元建立顯示清單，然後針對您想要繪製的每個字元，執行適當的顯示清單，以在雙重緩衝的 OpenGL 視窗中繪製文字。
ms.assetid: 59ac0414-a845-4f40-be9c-9962fd1585f6
keywords:
- Windows 上的 OpenGL，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0bf4cc99a1806d734ccde5cfae98f4d367da13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675496"
---
# <a name="drawing-text-in-a-double-buffered-opengl-window"></a>在 Double-Buffered OpenGL 視窗中繪製文字

您可以藉由為字型中的選定字元建立顯示清單，然後針對您想要繪製的每個字元，執行適當的顯示清單，以在雙重緩衝的 OpenGL 視窗中繪製文字。 下列程式碼範例會建立轉譯內容、繪製紅色三角形，然後加上文字的標籤。 在此範例程式碼中，我們假設有一個具有字型和像素格式的裝置內容。


```C++
// create an OpenGL rendering context  
hglrc = wglCreateContext(hdc); 
 
// make it this thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// make the color a deep blue hue  
glClearColor(0.0F, 0.0F, 0.4F, 1.0F); 
 
// make the shading smooth 
glShadeModel(GL_SMOOTH); 
 
// clear the color buffers  
glClear(GL_COLOR_BUFFER_BIT); 
 
// specify a red triangle  
glBegin(GL_TRIANGLES); 
    glColor3f(1.0F, 0.0F, 0.0F); 
    glVertex2f(10.0F, 10.0F); 
    glVertex2f(250.0F, 50.0F); 
    glVertex2f(105.0F, 280.0F); 
glEnd(); 
 
// create bitmaps for the device context font's first 256 glyphs  
wglUseFontBitmaps(hdc, 0, 256, 1000); 
 
// move bottom left, southwest of the red triangle  
glRasterPos2f(30.0F, 300.0F); 
 
// set up for a string-drawing display list call  
glListBase(1000); 
 
// draw a string using font display lists  
glCallLists(12, GL_UNSIGNED_BYTE, "Red Triangle"); 
 
// get all those commands to execute  
glFlush(); 
 
// delete our 256 glyph display lists  
glDeleteLists(1000, 256) ; 
 
// make the rendering context not current  
wglMakeCurrent (NULL, NULL) ; 
 
// release the device context  
ReleaseDC(hdc) ; 
 
// delete the rendering context  
wglDeleteContext(hglrc);
```



 

 




