---
title: 鳶尾花 GL 球體程式庫
description: OpenGL 不支援鳶尾花 GL 球體程式庫。 您可以使用 X.GLU 隊程式庫中的 quadrics 常式來取代球體程式庫呼叫。 如需 X.GLU 隊程式庫的詳細資訊，請參閱 Open GL 程式設計指南和 OpenGL 公用程式程式庫。
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- 鳶尾花 GL 移植，球體程式庫
- 從鳶尾花 GL、球體程式庫移植
- 從鳶尾花 GL、球體程式庫移植至 OpenGL
- 從鳶尾花 GL、球體程式庫移植的 OpenGL
- 繪圖函數、球體程式庫
- 球體程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301199"
---
# <a name="the-iris-gl-sphere-library"></a>鳶尾花 GL 球體程式庫

OpenGL 不支援鳶尾花 GL 球體程式庫。 您可以使用 X.GLU 隊程式庫中的 quadrics 常式來取代球體程式庫呼叫。 如需 X.GLU 隊程式庫的詳細資訊，請參閱 *OPEN GL 程式設計指南* 和 [OpenGL 公用程式程式庫](opengl-utility-library.md)。

下表列出 OpenGL quadrics 函數。



| OpenGL 函數                                        | 意義                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | 建立新的 quadric 物件。                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | 刪除 quadric 物件。                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | 將回呼與 quadric 物件產生關聯，以進行錯誤處理。 |
| [**gluQuadricNormals**](gluquadricnormals.md)         | 指定法線：無法線，每個臉部各一個，或每個頂點一個。  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | 指定法線的方向：向外或向外。               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | 開啟或關閉材質座標產生。                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | 指定繪製樣式：多邊形、線條、點等等。     |
| [**gluSphere**](glusphere.md)                         | 繪製球體。                                                  |
| [**gluCylinder**](glucylinder.md)                     | 繪製圓柱圖或圓錐圖。                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | 繪製弧形。                                                    |
| [**gluDisk**](gludisk.md)                             | 繪製圓形或磁片。                                          |



 

您可以針對想要以類似方式轉譯的所有 quadrics 使用一個 quadric 物件。 下列程式碼範例會使用兩個 quadric 物件來繪製四個 quadrics，兩個都有紋理。


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




