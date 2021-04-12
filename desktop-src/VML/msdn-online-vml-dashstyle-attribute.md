---
title: VML DashStyle 屬性
description: VML DashStyle 屬性
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315316"
---
# <a name="vml-dashstyle-attribute"></a>VML DashStyle 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定筆劃的點和虛線模式。 讀取/寫入 **VgLineDashStyle**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* dashstyle = " *expression* " >

**指令碼語法**

 dashstyle = "*expression*"

*運算式* =** dashstyle

**備註**

數值包括：

-   Solid (預設值)
-   ShortDash
-   ShortDot
-   ShortDashDot
-   ShortDashDotDot
-   點
-   虛線
-   LongDash
-   DashDot
-   LongDashDot
-   LongDashDotDot

**DashStyle** 屬性可讓使用者指定自訂定義的虛線模式。 這是使用一連串的數位來完成。 虛線樣式是以虛線的長度來定義， (筆觸的繪製部分) 和虛線之間的空間長度。 長度是相對於線條寬度： "1" 的長度等於線條的寬度。 **EndCap** 樣式會套用至每個虛線，而箭號樣式則不適用。 字串會先定義虛線的長度，然後再定義空間的長度。 這可能會重複形成複雜的虛線樣式。 字串應該一律包含成對的數位;如果它包含奇數數目的數位，則可能會忽略最後一個。

下表列出一些一般值和預期效果的描述。 「0」意指點應該是 epirus 對稱 (使用「迴圈結束」端點，其應為圓形) 。 如果行尾端點是「平面」，則檢視器應該選擇內建的作業系統虛線，可能的 (換句話說。 快速繪製的東西。 ) 。 下表顯示一些範例。



| DashStyle     | Description                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | 短破折號。 每個虛線和兩者之間的間距是線條寬度的兩倍。                        |
| "0 2"         | 點。 介於兩者之間的空格是線條寬度的兩倍。                                                  |
| "2 2 0 2"     | 短虛線。                                                                                      |
| "2 2 0 2 0 2" | 短虛線點。                                                                                  |
| "1 2"         | 點。 每個虛線都是線條的寬度，而每個空間都是線條寬度的兩倍。            |
| "4 2"         | 破折號。 每個虛線都是線條寬度的四倍，而每個空格是線條寬度的兩倍。 |
| "8 2"         | 長虛線。                                                                                           |
| "4 2 1 2"     | 虛線。                                                                                            |
| "8 2 1 2"     | 長虛線點。                                                                                       |
| "8 2 1 2 1 2" | 長虛線點。                                                                                   |



 

*VML 標準屬性*

**範例**

圖形具有虛線樣式的交替虛線和點。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 