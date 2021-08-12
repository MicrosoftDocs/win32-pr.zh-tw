---
title: VML CoordOrigin 屬性
description: VML CoordOrigin 屬性
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf568f2c305108a651d56a891a96890154f9493cbadd80a9c5610414c88f4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601940"
---
# <a name="vml-coordorigin-attribute"></a>VML CoordOrigin 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定將圖形系結之矩形的座標單位原點。 讀取/寫入 [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* coordorigin = " *expression* " >

**指令碼語法**

 coordorigin = "*expression*"

*運算式* =** coordorigin

**備註**

如果未指定，則原始座標為圖形周框方塊左上角的 (0，0) 。

**CoordSize** 的 x 值會加入至 **CoordOrigin** 的 x 值，以判斷水準值的範圍。 例如，如果 **CoordOrigin** 的 x 值為-100，而 **CoordSize** 的 x 值為200，則水準單位的範圍將從-100 到 + 100。 如果 **CoordOrigin** 的 x 值為100，而 **CoordSize** 的 x 值為200，則水準單位的範圍將從100到300，全都在周框方塊內。 Y 值也是如此。

請注意，此屬性是向量，而且單位與 [CoordSize](msdn-online-vml-coordsize-attribute.md) 的單位類型相同。

在腳本中，因為這是2D 向量，所以您可以分別存取 x 和 y 值，也可以決定預期的單位類型。

*VML 標準屬性*

**範例**

周框方塊的中心將會是圖形路徑的原點 (0、0) 。 因為 **CoordOrigin** 是 "-500-500" 且 **CoordSize** 為 "1000 1000"，所以水準和垂直單位的範圍將從-500 到 + 500。 路徑的左邊和左上角將位於左邊和頂端點所定義的周框方塊中央，如 **樣式** 所定義。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[CoordOrigin 屬性範例](/previous-versions/bb229664(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 