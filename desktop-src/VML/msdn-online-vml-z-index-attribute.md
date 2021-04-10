---
title: VML Z 索引屬性
description: VML Z 索引屬性
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933304"
---
# <a name="vml-z-index-attribute"></a>VML Z 索引屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定重迭圖形的顯示順序。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* style = "z-index： *expression* " >

**指令碼語法**

 zindex = "*expression*"

*運算式* =** zindex

**備註**

**Z 索引** 屬性類似于樣式的標準 HTML **Z 索引** 屬性。

數值包括：



| 值 | 描述                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 自動  | 圖形出現在 HTML 網頁中的順序將會使用，由下往上。                                                                                                                         |
| 順序 | 表示堆疊優先順序的數位。 具有較高數位的圖形會顯示為 wereoverlapping 在) 圖形的「前方」 (的數位較低的形狀。 您可以使用負數。 |



 

*VML 標準屬性*

**範例**

紅色圖形將會顯示在藍色圖形的「前方」中，因為它的 Z 軸索引較高。


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Z-索引屬性範例](/previous-versions/ms530275(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 