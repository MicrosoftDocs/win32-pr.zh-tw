---
title: 移植球體
description: 將球體移植至 OpenGL 時，請記住下列幾點
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- 鳶尾花 GL 移植，球體
- 從鳶尾花 GL、球體進行移植
- 從鳶尾花 GL （球體）移植至 OpenGL
- 從鳶尾花 GL （球體）進行 OpenGL 移植
- 繪圖函數，球體
- 領域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358307"
---
# <a name="porting-spheres"></a>移植球體

將球體移植至 OpenGL 時，請記住下列幾點：

-   您無法控制用來繪製球體的基本類型。 您可以用另一種方式控制繪圖精確度：使用配量和堆疊參數。 配量為 longitudinal;堆疊為 latitudinal。
-   球體繪製于原點中央。 與其使用鳶尾花 GL **sphdraw** 函式來指定位置，請在 x.glu 隊 [**gluSphere**](glusphere.md) 函式的呼叫之前加上翻譯。
-   此球體程式庫尚未適用于 OpenGL。

下表列出用來繪製球體的鳶尾花 GL 函式，以及其對等的 X.GLU 隊函式（如果有的話）。



| 鳶尾花 GL 函數 | X.GLU 隊函式                                 | 意義                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | 建立新的球體物件。                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | 刪除球體物件和使用的可用記憶體。   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | 繪製球體。                               |
| **sphmode**      |                                              | 設定球體屬性。                       |
| **sphrotmatrix** |                                              | 控制球體方向。                  |
| **sphgnpolys**   |                                              | 傳回目前球體中的多邊形數目。 |



 

??

 

 




