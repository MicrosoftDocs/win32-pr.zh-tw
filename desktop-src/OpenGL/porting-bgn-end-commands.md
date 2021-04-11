---
title: 移植 bgn/end 命令
description: 鳶尾花 GL 使用 begin/end 範例，但每個圖形基本功能各有不同的函式。
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- 鳶尾花 GL 移植、bgn/結束命令
- 從鳶尾花 GL、bgn/end 命令移植
- 從鳶尾花 GL 移植至 OpenGL、bgn/end 命令
- 鳶尾花 GL、bgn/end 命令的 OpenGL 移植
- 繪圖函數、bgn/end 命令
- bgn/end 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372512"
---
# <a name="porting-bgnend-commands"></a>移植 bgn/end 命令

鳶尾花 GL 使用 begin/end 範例，但每個圖形基本功能各有不同的函式。 例如，您可能會使用 **bgnpolygon** 和 **endpolygon** 來繪製多邊形，並使用 **bgnline** 和 **endline** 來繪製線條。 在 OpenGL 中，您可以使用 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)結構。 在 OpenGL 中，您可以藉由封入一系列的函式來繪製大部分的幾何物件，這些函式會指定 **glBegin** 與 **glEnd** 呼叫配對之間的頂點、法線、材質和色彩。 例如：

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

**GlBegin** 函式會採用指定繪圖模式的單一參數，也就是基本。 以下是一個可繪製多邊形和一行的 OpenGL 程式碼範例：

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

使用 OpenGL，您可以藉由指定不同的 [**glBegin**](glbegin.md)參數來繪製不同的幾何物件。 下表列出對應至相等鳶尾花 GL 函數的 OpenGL **glBegin** 參數。



| 鳶尾花 GL 函數  | GlBegin 模式的值 | 意義                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | GL \_ 點            | 個別的點。                                                                       |
| **bgnline**       | GL \_ 行 \_ 帶       | 一連串連接的線段。                                                       |
| **bgnclosedline** | GL \_ 線路 \_ 迴圈        | 一系列連接的直線線段，在第一個和最後一個頂點之間加入區段。 |
|                   | GL \_ 行             | 成對的頂點，會轉譯為個別的線段。                               |
| **bgnpolygon**    | GL \_ 多邊形           | 簡單凸邊的界限。                                                     |
|                   | GL \_ 三角形         | 被解釋為三角形的三倍頂點。                                            |
| **bgntmesh**      | GL \_ 三角形 \_ 條紋   | 三角形的連結去除。                                                              |
|                   | GL \_ 三角形 \_ 風扇     | 三角形的連結風扇。                                                                |
|                   | GL \_ 四邊形             | 解釋為 quadrilaterals 的頂點時。                                    |
| **bgnqstrip**     | GL \_ 四 \_ 條       | Quadrilaterals 的連結塊。                                                         |



 

如需三角形網格、條紋和風扇之間差異的詳細討論，請參閱 [移植三角形](porting-triangles.md)。

您可以在 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)配對之間指定的頂點數目沒有任何限制。

除了在 **glBegin**  /  **glEnd** 配對內指定頂點之外，您還可以指定目前的一般材質和目前的材質座標，以及目前的色彩。 下表列出 **glBegin**  /  **glEnd** 配對內的有效命令。



| 鳶尾花 GL 函數        | OpenGL 函數                                                      | 意義                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**、 **v3**、 **v4**  | [glVertex](glvertex-functions.md)                                   | 設定頂點座標。                         |
| **RGBcolor**、 **cpack** | [glColor](glcolor-functions.md)                                     | 設定目前的色彩。                              |
| **color**               | [glIndex](glindex-functions.md)                                     | 設定目前的色彩索引。                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | 設定一般向量座標。                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | 評估已啟用一維和二維的地圖。 |
| **callobj**             | [**glCallList**](glcalllist.md)、 [ **glCallLists**](glcalllists.md) |  (s) 執行顯示清單。                        |
| <bpt id="p1">**</bpt>t2<ept id="p1">**</ept>                  | [glTexCoord](gltexcoord-functions.md)                               | 設定材質座標。                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | 控制繪圖邊緣。                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | 設定材質屬性。                        |



 

> [!Note]
>
> 如果您使用上述表格中所列的任何 OpenGL 函式，而不是在 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)組內，您將會得到無法預期的結果，或可能發生錯誤。

 

 

 




