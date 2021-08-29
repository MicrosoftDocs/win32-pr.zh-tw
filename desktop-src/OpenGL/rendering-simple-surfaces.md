---
title: 轉譯簡單的表面
description: X.GLU 隊程式庫包含一組用來繪製各種簡單表面的函式， (球體、圓柱圖、磁片和部分磁片) 以各種樣式和方向呈現。 這些函數會在 OpenGL 參考手冊中詳細說明。
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- OpenGL 公用程式 (X.GLU 隊) 、簡單表面
- X.GLU 隊 (OpenGL 公用程式) ，簡單表面
- 簡單表面 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、球體
- X.GLU 隊 (OpenGL 公用程式) 、球體
- 球體 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、圓柱
- X.GLU 隊 (OpenGL 公用程式) 、圓柱
- 圓柱的 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、磁片
- X.GLU 隊 (OpenGL 公用程式) ，磁片
- 磁片 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4010a9cc1c0cfac58f1a99572ebae43233dce552237c17f42d66cc1c50013986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776828"
---
# <a name="rendering-simple-surfaces"></a>轉譯簡單的表面

X.GLU 隊程式庫包含一組用來繪製各種簡單表面的函式， (球體、圓柱圖、磁片和部分磁片) 以各種樣式和方向呈現。 這些函數會在 *OpenGL 參考手冊* 中詳細說明。

**轉譯簡單的表面**

1.  使用 [**gluNewQuadric**](glunewquadric.md)建立 quadric 物件。

    若要在完成時終結這個物件，請使用 [**gluDeleteQuadric**](gludeletequadric.md)。

2.  指定所需的轉譯樣式（如下所示），並使用適當的函式 (除非您滿意) 的預設值：
    -   是否應該產生介面法線，若是如此，每個頂點上是否應該有一個法線，或每個臉部的一個法線： [ **gluQuadricNormals**](gluquadricnormals.md)
    -   是否應該產生材質座標： [ **gluQuadricTexture**](gluquadrictexture.md)
    -   應將 quadric 的哪個端視為外部，並將其置於： [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   是否應將 quadric 繪製成一組多邊形、線條或點： [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  指定轉譯樣式之後，針對所需的 quadric 物件類型叫用轉譯函數： [**gluSphere**](glusphere.md)、 [**gluCylinder**](glucylinder.md)、 [**gluDisk**](gludisk.md)或 [**gluPartialDisk**](glupartialdisk.md)。

    如果在轉譯期間發生錯誤，則會叫用您以 [*gluQuadricCallBack*](gluquadric.md) 指定的錯誤處理函式。

使用 *\* 半徑*、*高度* 和類似的引數（而不是 [**glScale**](glscale.md)函式）來調整 quadrics，如此您就不需要重新標準化為產生的任何單位長度法線。 若要以更精細的細微性來強制執行光源計算，尤其是當材質 specularity 很高時，請將 *迴圈* 和 *堆疊* 引數設定為1以外的值。

 

 




