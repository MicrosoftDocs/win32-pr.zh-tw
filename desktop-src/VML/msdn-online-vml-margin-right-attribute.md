---
title: VML Margin-Right 屬性
description: VML Margin-Right 屬性
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5569f4f89cbe5320cfc348f2e2929b986736412f4cb864a62dd4584bde43a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346456"
---
# <a name="vml-margin-right-attribute"></a>VML Margin-Right 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定相對於圖形錨點之圖形內含矩形的右邊緣。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "margin-right： *expression* " >

**指令碼語法**

 marginright = "*expression*"

*運算式* =** marginright

**備註**

右邊 **界** 屬性類似于樣式表單所使用的標準 HTML **Margin 右** 屬性。

請注意， **marginright** 是用來取代 **右邊** 的腳本。 另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。

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

右邊界設定為25圖元。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[右邊界屬性範例](/previous-versions/bb229677(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 