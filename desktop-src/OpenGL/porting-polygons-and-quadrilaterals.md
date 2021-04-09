---
title: 移植多邊形和 Quadrilaterals
description: 移植多邊形和 quadrilaterals 時，請記住下列幾點
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- 鳶尾花 GL 移植，quadrilaterals
- 從鳶尾花 GL、quadrilaterals 移植
- 從鳶尾花 GL （quadrilaterals）移植至 OpenGL
- 從鳶尾花 GL quadrilaterals 的 OpenGL 移植
- 繪圖函數，quadrilaterals
- quadrilaterals
- 鳶尾花 GL 移植，多邊形
- 從鳶尾花 GL、多邊形進行移植
- 從鳶尾花 GL、多邊形移植至 OpenGL
- 從鳶尾花 GL、多邊形的 OpenGL 移植
- 繪圖函數、多邊形
- 多邊形，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674535"
---
# <a name="porting-polygons-and-quadrilaterals"></a>移植多邊形和 Quadrilaterals

移植多邊形和 quadrilaterals 時，請記住下列幾點：

-   **凹** (**TRUE**) 沒有直接對等專案。 相反地，您可以使用 X.GLU 隊中的鑲嵌式常式，如 [鑲嵌多邊形](tessellating-polygons.md)所述。
-   多邊形模式的設定方式不同。
-   這些多邊形繪圖函式在 OpenGL 中沒有直接對等專案： **poly** 系列的常式; **polf** 系列的常式; **pmv**、 **寮國** 和 **pclos**; **rpmv** 和 **rpdr**; **splf**;和 **spclos**。

如果您的鳶尾花 GL 程式碼使用這些功能，您必須使用 [**glBegin**](glbegin.md) ( GL 多邊形 ) 來重寫程式碼 \_ 。

下表列出鳶尾花 GL 多邊形繪圖函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數         | OpenGL 函數                                                    | 意義                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( GL \_ 多邊形 ) [ **glEnd**](glend.md)   | 頂點：定義簡單凸邊的界限。    |
|                          | **glBegin** ( GL \_ 四邊形 ) **glEnd**<br/>                       | 將頂點的時解讀為 quadrilaterals。    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) ( GL \_ QUAD \_ ) **glEnd**<br/> | 將頂點解釋為 quadrilaterals 的連結塊。 |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **polymode**             | [**glPolygonMode**](glpolygonmode.md)                             | 設定多邊形繪圖模式。                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | 繪製矩形。                                      |
| **sboxsboxf**<br/> |                                                                    | 繪製螢幕對齊的矩形。                       |



 

??

## <a name="porting-polygon-modes"></a>移植多邊形模式

[OpenGL 函數 [**glPolygonMode**](glpolygonmode.md) ] 可讓您指定多邊形的哪一端 (要套用至哪一側的背景) 。 其語法如下：

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

其中的臉部是下列其中一項：



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| GL \_ FRONT            | 適用于正面多邊形的模式                |
| GL \_ 回             | 適用于後置多邊形的模式                 |
| GL \_ 正面 \_ 和 \_ 背面 | 適用于 front 和 back 多邊形的模式 |



 

GL \_ 前端 \_ 和 \_ 後端模式相當於鳶尾花 GL **polymode** 函數。 下表列出鳶尾花 GL 多邊形模式及其對等的 OpenGL 模式。



| 鳶尾花 GL 模式 | OpenGL 模式 | 意義                                       |
|--------------|-------------|-----------------------------------------------|
| PYM \_ 點   | GL \_ 點   | 將頂點繪製成點。                     |
| PYM \_ 行    | GL \_ 線    | 將邊界邊緣繪製為線段。        |
| PYM \_ 填滿    | GL \_ 填滿    | 繪製填滿的多邊形內部。                |
| PYM \_ 空心  |             | 只填滿界限的內部圖元。 |



 

## <a name="porting-polygon-stipples"></a>移植多邊形 Stipples

移植鳶尾花 GL 多邊形 stipples 時，請記住下列幾點：

-   OpenGL 不會使用資料表進行多邊形 stipples;只保留一個 stipple 模式。 您可以使用顯示清單來儲存不同的 stipple 模式。
-   OpenGL 多邊形 stipple 點陣圖大小一律為32x32 位模式。
-   Stipple 編碼會受到 [**glPixelStore**](glpixelstore-functions.md)的影響。

如需移植多邊形 stipples 的詳細資訊，請參閱 [移植圖元作業](porting-pixel-operations.md)。

下表列出鳶尾花 GL 多邊形 stipple 函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                                    | 意義                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | 設定 stipple 模式。                             |
| **setpattern**   |                                                    | OpenGL 只保留一個多邊形 stipple 模式。        |
| **system.windows.automation.peers.uielementautomationpeer.getpattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | 傳回 stipple 點陣圖 (用來傳回索引) 。 |



 

在 OpenGL 中，您可以藉由 \_ 將 GL 多邊形 STIPPLE 傳遞 \_ 為 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的參數，來啟用和停用多邊形 stippling。

下列 OpenGL 程式碼範例示範多邊形 stippling：


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>移植鑲嵌多邊形

在鳶尾花 GL 中，您會使用 **凹** (**TRUE**) 然後 **bgnpolygon** 來繪製凹形多邊形。 OpenGL X.GLU 隊包含您可以用來繪製凹形多邊形的函式。

**使用 OpenGL 繪製凹形多邊形**

1.  建立鑲嵌式物件。
2.  定義將用來處理鑲嵌所產生之三角形的回呼。
3.  指定要鑲嵌的凹陷多邊形。

下表列出繪圖鑲嵌多邊形的 OpenGL 函數。



| OpenGL X.GLU 隊函式                        | 意義                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | 建立新的鑲嵌式物件。                                 |
| [**gluDeleteTess**](gludeletetess.md)     | 刪除鑲嵌式物件。                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | 開始多邊形規格。                                  |
| [**gluTessVertex**](glutessvertex.md)     | 指定輪廓中的多邊形頂點。                           |
| [**gluNextContour**](glunextcontour.md)   | 表示下一系列頂點描述新的輪廓。 |
| [**gluEndPolygon**](gluendpolygon.md)     | 結束多邊形規格。                                    |



 

 

 





