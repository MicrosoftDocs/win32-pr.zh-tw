---
title: 鑲嵌多邊形
description: 鑲嵌多邊形
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- OpenGL 公用程式 (X.GLU 隊) ，鑲嵌
- X.GLU 隊 (OpenGL 公用程式) ，鑲嵌
- OpenGL 公用程式 (X.GLU 隊) 、簡單的多邊形
- X.GLU 隊 (OpenGL 公用程式) ，簡單的多邊形
- 簡單的多邊形 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、複雜的多邊形
- X.GLU 隊 (OpenGL 公用程式) ，複雜的多邊形
- 複雜的多邊形 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e0669348404af763883f7ff713212d52f6f0d79312812552c0e5053041627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034510"
---
# <a name="tessellating-polygons"></a>鑲嵌多邊形

OpenGL 只能直接顯示簡單的凸形多邊形。 多邊形很簡單，如下所示：

-   邊緣只會在頂點上相交。
-   沒有重複的頂點。
-   正好有兩個邊緣符合任何頂點。

若要顯示包含孔洞的簡單 nonconvex 多邊形或簡單多邊形，您必須先分成三角形多邊形 (將它們細分成凸多邊形) 。 這類細分稱為 *鑲嵌* 式。 X.GLU 隊提供執行鑲嵌的函式集合。 請注意，X.GLU 隊鑲嵌函數無法處理簡單多邊形;沒有標準的 OpenGL 方法可處理這類多邊形。

因為鑲嵌通常是必要的，而且可能很難處理，所以本節會詳細說明 X.GLU 隊鑲嵌函數。 這些函式會採用輸入任意簡單的多邊形（其中可能包含洞），並傳回三角形、三角形網格和三角形風扇的組合。 如果您不想要處理網格或風扇，可以指定鑲嵌式函數只傳回三角形。 不過，網格和風扇資訊可提升效能。 多邊形鑲嵌式函數會分成三角形具有一或多個輪廓的凹多邊形。

**使用多邊形鑲嵌**

1.  使用 [**gluNewTess**](glunewtess.md)建立鑲嵌式物件。
2.  使用 [*gluTessCallBack*](glutess.md) 來定義回呼函式，您將使用這些函數來處理鑲嵌所產生的三角形。
3.  使用 [**gluBeginPolygon**](glubeginpolygon.md)、 [**gluTessVertex**](glutessvertex.md)、 [**gluNextContour**](glunextcontour.md)和 [**gluEndPolygon**](gluendpolygon.md)，指定具有洞的多邊形或要鑲嵌的凹陷多邊形。

    當多邊形描述完成時，鑲嵌式功能會視需要叫用您的回呼函式。

    您可以使用 [**gluDeleteTess**](gludeletetess.md)終結不必要的鑲嵌式物件。

如需儲存鑲嵌式資料的詳細資訊，請參閱 [使用回呼函數](using-callback-functions.md)。

 

 




