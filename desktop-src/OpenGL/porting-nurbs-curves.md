---
title: 移植 NURBS 曲線
description: 繪製 NURBS 曲線的 OpenGL 函式與鳶尾花 GL 函數非常類似。 您可以使用 gluNurbsCurve 函式指定節點序列和控制點，此函式必須包含在 gluBeginCurve/gluEndCurve 配對內。
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- 鳶尾花 GL 移植，NURBS 曲線
- 從鳶尾花 GL、NURBS 曲線移植
- 從鳶尾花 GL （NURBS 曲線）移植至 OpenGL
- 從鳶尾花 GL、NURBS 曲線移植的 OpenGL
- NURBS 曲線
- 曲線
- 鳶尾花 GL 移植，曲線
- 從鳶尾花 GL、曲線移植
- 從鳶尾花 GL （曲線）移植至 OpenGL
- 從鳶尾花 GL、曲線移植的 OpenGL
- 'NURBS (非統一的有理 B 曲線) '
- '非統一的有理 B 曲線 (NURBS) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372366"
---
# <a name="porting-nurbs-curves"></a>移植 NURBS 曲線

繪製 NURBS 曲線的 OpenGL 函式與鳶尾花 GL 函數非常類似。 您可以使用 [**gluNurbsCurve**](glunurbscurve.md)函式指定節點序列和控制點，此函數必須包含在 [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md)配對內。

下表列出用來繪製 NURBS 曲線的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                        | 意義                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | 開始曲線定義。  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | 指定曲線屬性。 |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | 結束曲線定義。    |



 

藉由將位置、材質和色彩座標呈現為開始/結束配對內的個別 **gluNurbsCurve** 來建立關聯。 您可以針對單一 **gluBeginCurve/gluEndCurve** 配對內的每個色彩、位置和材質資料片段，進行一個以上的 **gluNurbsCurve** 呼叫。 您必須確實進行一個呼叫，以描述曲線的位置 (GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4 描述) 。 當您呼叫 **gluEndCurve** 時，會將曲線鑲嵌成線段，然後轉譯。

下表列出鳶尾花 GL 和 OpenGL NURBS 曲線類型。



| 鳶尾花 GL 類型 | OpenGL 類型                  | 意義                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ 頂點 \_ 3          | 多項式曲線。                       |
| N \_ V3DR      | GL \_ MAP1 \_ 頂點 \_ 4          | 有理數曲線。                         |
|              | GL \_ MAP1 \_ 材質 \_ COORD\_\* | 控制點是材質座標。 |
|              | GL \_ MAP1 \_ 正常             | 控制點是法線。             |



 

如需可用評估工具類型的詳細資訊，請參閱 [**glMap1**](glmap1.md)。

??

 

 




