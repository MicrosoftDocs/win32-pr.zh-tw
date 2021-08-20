---
title: VML 寬度屬性
description: VML 寬度屬性
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385aee5c45f68d039bc1bcf6bd3b0c52db0871640bc8a2df3a7f25e9e2bdc205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938955"
---
# <a name="vml-width-attribute"></a>VML 寬度屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的寬度。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "width： *expression* " >

**指令碼語法**

*元素* 。 style. width = "*expression*"

*運算式* =style *. width*

**備註**

**寬度** 屬性類似于樣式的標準 HTML **寬度** 屬性。

單位可以對應至父元素，或可能是絕對單位。

數值包括：



| 值      | 描述                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 自動       | 頁面流程中專案的預設位置。                                                                                                          |
| units      | 具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。 如果未指定任何單位，則會假設為圖元 (px) 。 |
| percentage | 以父物件寬度的百分比表示的值。                                                                                                    |



 

*VML 標準屬性*

**另請參閱**

[單位](msdn-online-vml-units.md)

**範例**

圖形的寬度為25。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Width 屬性範例](/previous-versions/bb264101(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 