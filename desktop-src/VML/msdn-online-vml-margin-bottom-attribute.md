---
title: VML Margin-Bottom 屬性
description: VML Margin-Bottom 屬性
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682738"
---
# <a name="vml-margin-bottom-attribute"></a>VML Margin-Bottom 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定相對於圖形錨點之圖形內含矩形的下邊緣。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* margin-下 = " *expression* " >

**指令碼語法**

 marginbottom = "*expression*"

*運算式* =** marginbottom

**備註**

上 **邊界** 屬性類似于樣式表單所使用的標準 HTML **邊界-下** 一個屬性。

請注意，會使用 **marginbottom** ，而不是使用 **邊界** 來進行腳本處理。 另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。

數值包括：



| 值      | 描述                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 自動       | 頁面流程中專案的預設位置。                                                                                                                                           |
| units      | 預設值。 具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。 如果未指定任何單位，則會假設為圖元 (px) 。 預設值為 0。 |
| percentage | 以父物件高度的百分比表示的值。                                                                                                                                    |



 

*VML 標準屬性*

**另請參閱**

[單位](msdn-online-vml-units.md)

**範例**

下邊界設定為25圖元。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[毛利率-底端屬性範例](/previous-versions/bb229675(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 