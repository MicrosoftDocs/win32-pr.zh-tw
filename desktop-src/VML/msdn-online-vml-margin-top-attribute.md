---
title: VML Margin-Top 屬性
description: VML Margin-Top 屬性
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346394"
---
# <a name="vml-margin-top-attribute"></a>VML Margin-Top 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定相對於圖形錨點之圖形內含矩形的上邊緣。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* margin-top = " *expression* " >

**指令碼語法**

*元素* 。 margin-top = "*expression*"

*運算式* =*元素*。邊界-上方

**備註**

**上邊界** 屬性類似于標準 HTML 邊界-與樣式表單搭配使用的 **最上層** 屬性。

請注意， **margintop** 是用來取代 **最上層** 的腳本。 另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。

這個屬性是針對 Microsoft Word 中的圖形，而不是 **Top** ，而是在相對於錨點的位置中浮動的 Microsoft Excel。

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

上邊界設定為25圖元。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Margin-Top 屬性範例](/previous-versions/bb264087(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 