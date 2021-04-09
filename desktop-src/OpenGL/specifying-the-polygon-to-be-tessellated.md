---
title: 指定要鑲嵌的多邊形
description: '您可以指定多邊形 (可能包含要使用鑲嵌的漏洞) '
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932531"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>指定要鑲嵌的多邊形

您可以使用下列內容指定多邊形 (可能包含要鑲嵌的漏洞) ：

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

針對沒有孔洞的多邊形，規格程式與 OpenGL 相同：

1.  從 [**gluBeginPolygon**](glubeginpolygon.md)開始。
2.  針對界限中的每個頂點呼叫 [**gluTessVertex**](glutessvertex.md) 。
3.  使用 [**gluEndPolygon**](gluendpolygon.md)的呼叫來結束多邊形。

如果多邊形包含多個輪廓（包括孔內的孔和孔），您可以指定一個後面接著 [**gluNextContour**](glunextcontour.md)的輪廓。 當您呼叫 [**gluEndPolygon**](gluendpolygon.md)時，它會發出最後輪廓的結尾，並開始鑲嵌。 您可以在第一個輪廓之前省略 **gluNextContour** 的呼叫。 [**GluBeginPolygon**](glubeginpolygon.md)函式會開始鑲嵌多邊形的規格，並將鑲嵌式物件 **tessobj** 與其產生關聯。 要使用的回呼函式是您使用 [*gluTessCallback*](glutess.md)系結至鑲嵌式物件的函數。

[**GluTessVertex**](glutessvertex.md)函式會指定要鑲嵌的多邊形頂點。 針對多邊形中的每個頂點呼叫 **gluTessVertex** 。 函式的 *tessobj* 參數是要使用的鑲嵌式物件、 *v* 包含三維頂點座標，而 *資料* 是傳送至與 **x.glu 隊 \_ 頂點** 相關聯之回呼的任意指標。 一般而言， *資料* 報含頂點資料、材質座標、色彩資訊，或應用程式可能需要的任何其他內容。

當多個輪廓組成要鑲嵌的多邊形界限時， [**gluNextContour**](glunextcontour.md) 函式會標示下一個輪廓的開頭。 函數的 *型* 別參數可以是 **X.glu 隊 \_ 外部**、 **X.glu 隊 \_ 內部**、 **x.glu 隊 \_ CCW**、 **x.glu 隊 \_ CW** 或 **x.glu 隊 \_ 未知**。 這些常數僅作為鑲嵌式的提示。 如果您得到適當的方式，鑲嵌可能會更快。 如果您遇到錯誤，這些錯誤會被忽略，而且鑲嵌仍能運作。

對於具有孔洞的多邊形，有一個輪廓是外部輪廓，其他則是內部。 如果您未在 [**gluBeginPolygon**](glubeginpolygon.md)後立即呼叫 **gluNextContour** ，則會假設第一個輪廓的類型為 **x.glu 隊 \_ 外部**。

**X.glu 隊 \_CW** 和 **x.glu 隊 \_ CCW** 指出順時針和逆時針方向的多邊形。 選擇的是順時針的，而這些是逆時針的，但在任何平面中，都有兩種不同的方向：以一致的方式使用 **x.glu 隊的 \_ CW** 和 **x.glu 隊 \_ CCW** 類型。 如果您不知道要使用哪一個，請使用 **X.glu 隊 \_ UNKNOWN** 。

[**GluEndPolygon**](gluendpolygon.md)函數表示多邊形規格的結尾。 這也表示鑲嵌可以開始使用鑲嵌式物件 *tessobj*。

 

 




