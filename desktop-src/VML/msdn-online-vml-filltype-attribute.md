---
title: VML FillType 屬性
description: VML FillType 屬性
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933590"
---
# <a name="vml-filltype-attribute"></a>VML FillType 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義用於筆劃背景的填滿類型。 讀取/寫入 **VgFillType**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* filltype = " *expression* " >

**指令碼語法**

 filltype = "*expression*"

*運算式* =** filltype

**備註**

數值包括：



| DashStyle | Description                                    |
|-----------|------------------------------------------------|
| 實線     | 填滿模式是實心。 預設值。      |
| 磚      | 填滿影像會並排顯示。                       |
| 模式   | 填滿影像以形成一種模式。 |
| Frame     | 填滿影像會變成圖形的框線。 |



 

*VML 標準屬性*

**範例**

圖形的筆觸具有從 cylinder.gif 影像建立的磚材質。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 