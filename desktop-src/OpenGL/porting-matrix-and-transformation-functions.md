---
title: 移植矩陣和轉換函數
description: 鳶尾花 GL 和 OpenGL 以類似的方式處理矩陣和轉換。
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- 鳶尾花 GL 移植，矩陣
- 從鳶尾花 GL （矩陣）移植
- 從鳶尾花 GL （矩陣）移植至 OpenGL
- 從鳶尾花 GL （矩陣）進行 OpenGL 移植
- 矩陣
- 鳶尾花 GL 移植，轉換
- 從鳶尾花 GL 進行移植，轉換
- 從鳶尾花 GL 移植至 OpenGL，轉換
- 從鳶尾花 GL 的 OpenGL 移植，轉換
- 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301387"
---
# <a name="porting-matrix-and-transformation-functions"></a>移植矩陣和轉換函數

鳶尾花 GL 和 OpenGL 以類似的方式處理矩陣和轉換。 但是從鳶尾花 GL 移植程式碼時，有幾個差異要記住：

-   在 OpenGL 中，一律採用雙矩陣模式;沒有單一矩陣模式。
-   角度是以度為單位，而不是十分之一度。
-   投射矩陣呼叫（例如 [**glFrustum**](glfrustum.md) 和 [**glOrtho**](glortho.md)）現在會乘以目前的矩陣，而不是載入到目前的矩陣上。
-   OpenGL 函數 [**glRotate**](glrotate.md)與 **旋轉** 非常不同。 您可以繞著任意軸旋轉，而不是限制為 X 軸、y 軸和 Z 軸。 例如，您可以翻譯：

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    變更為：

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    從 **旋轉** 轉譯為 **glRotate** 時，您會切換至十分之一度的角度，並以 Z 軸的向量取代 ' z '。

-   OpenGL 沒有 **polarview** 函式的相等專案。 您可以輕鬆地使用轉譯和三個旋轉來取代它。 例如，您可以翻譯：

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    變更為：

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

下表列出 OpenGL 矩陣函數及其對等的鳶尾花 GL 函數。



| 鳶尾花 GL 函數              | OpenGL 函數                                                                        | 意義                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | 設定目前的矩陣模式。                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | 將目前的矩陣取代為識別矩陣。                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md)、[**glLoadMatrixd**](glloadmatrix.md)<br/> | 以指定的矩陣取代目前的矩陣。                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md)、[**glMultMatrixd**](glmultmatrix.md)<br/> | 將目前的矩陣與指定的矩陣相乘 (請注意， **multmatrix** 會預先相乘) 。                                                                            |
| **mapw**、 **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | 專案世界-空間與物件空間的座標 (另請參閱 [**gluProject**](gluproject.md)) 。                                                                                  |
| **鄰**                     | [**glOrtho**](glortho.md)                                                             | 將目前的矩陣與正向投射矩陣相乘。                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | 定義二維正射投射矩陣。                                                                                                                      |
| **視角**               | [**gluPerspective**](gluperspective.md)                                               | 定義透視圖投影矩陣。                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | 定義挑選區域。                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Pop 目前的矩陣堆疊，以其下的矩陣來取代目前的矩陣。                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | 將目前的矩陣堆疊向下推一，以複製目前的矩陣。                                                                                                       |
| **旋轉**，**rot**<br/> | [**glRotated**](glrotate.md)、[**glRotatef**](glrotate.md)<br/>                 | 透過指定的點，將目前座標系統與原點的向量旋轉。 請注意，只 **旋轉** X 軸、y 軸和 Z 軸的旋轉。 |
| **scale**                     | [**glScaled**](glscale.md)、[**glScalef**](glscale.md)<br/>                     | 將目前的矩陣乘以縮放矩陣。                                                                                                                                 |
| **翻譯**                 | [**glTranslatef**](gltranslate.md)、[**glTranslated**](gltranslate.md)<br/>     | 將目前的矩陣乘以平移矩陣，將座標系統原點移至指定的點。                                                              |
| **視窗**                    | [**glFrustum**](glfrustum.md)                                                         | 指定裁剪平面的座標，將目前的矩陣乘以透視圖矩陣。                                                                                  |



 

OpenGL 有三個矩陣模式，以 [**glMatrixMode**](glmatrixmode.md)設定。 下表列出可做為 **glMatrixMode** 參數的模式。



| 鳶尾花 GL 矩陣模式 | OpenGL 模式    | 意義                                  | 最小堆疊深度 |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | GL \_ 材質    | 在紋理矩陣堆疊上運作。    | 2               |
| **MVIEWING**        | GL \_ 模型  | 在模型視圖矩陣堆疊上運作。 | 32              |
| **MPROJECTION**     | GL \_ 投射 | 在投射矩陣堆疊上運作。 | 2               |



 

 

 





