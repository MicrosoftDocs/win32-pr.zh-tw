---
title: VML Flip 屬性
description: VML Flip 屬性
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346632"
---
# <a name="vml-flip-attribute"></a>VML Flip 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

切換圖形的方向。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "flip： *expression* " >

**指令碼語法**

*element* 。 style. flip = "*expression*"

*運算式* =*element*. style. flip

**備註**

數值包括：



| 值 | 描述                                           |
|-------|-------------------------------------------------------|
| x     | 沿著 y 軸翻轉，反轉 *x* 座標。 |
| y     | 沿著 *x* 軸翻轉，反轉 y 座標。 |
| xy    | 沿著 y 軸和 *x* 軸翻轉。                  |
| yx    | 沿著 *x* 軸和 *y* 軸翻轉。                |



 

*VML 標準屬性*

**另請參閱**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**範例**

圖形會反轉 *x* 座標，沿著 *y* 軸翻轉。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Flip 屬性範例](/previous-versions/bb229670(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 