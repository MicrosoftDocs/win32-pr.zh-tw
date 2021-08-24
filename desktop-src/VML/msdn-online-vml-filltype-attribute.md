---
title: VML FillType 屬性
description: VML FillType 屬性
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680798"
---
# <a name="vml-filltype-attribute"></a>VML FillType 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

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



| DashStyle | 描述                                    |
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



 

 