---
title: VML Margin-Left 屬性
description: VML Margin-Left 屬性
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f403c19e617f8131886d3f4a862ff1ac0b878edbd2acf2fd0e27cb17b3406c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680818"
---
# <a name="vml-margin-left-attribute"></a>VML Margin-Left 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定相對於圖形錨點之圖形內含矩形的左邊緣。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "margin-left： *expression* " >

**指令碼語法**

 marginleft = "*expression*"

*運算式* =** marginleft

**備註**

**左邊界** 屬性類似于樣式表單所使用的標準 HTML **左邊界** 屬性。

請注意， **marginleft** 是用來取代腳本的 **左邊界** 。 另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。

針對 Microsoft Word 中的圖形，以及浮在相對於錨點之位置的 Microsoft Excel，則會使用這個屬性，而不是 **左方**。

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

左邊界設定為25圖元。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



[左邊界屬性範例](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples)。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 