---
title: '旋轉屬性 (圖形)  (VML) '
description: '旋轉屬性 (圖形)  (VML) '
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024042"
---
# <a name="rotation-attribute-shapevml"></a>旋轉屬性 (圖形)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義形狀旋轉的角度。 讀取/寫入 [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* style = "旋轉： *expression* " >

**指令碼語法**

*元素* 。旋轉 = "*expression*"

*運算式* =*元素*。旋轉

**備註**

以度為單位的值可以是正數或負數，而大於360的值則會被模組化至360度的圓形。 正面角度是順時針的。 預設值為 0。

請注意，圖形會在旋轉之後重新置放，以反映新的周框方塊座標。

也請注意，在撰寫腳本時，不會使用 **樣式** 屬性，而會將 **旋轉** 視為圖形的直接屬性。

**旋轉** 屬性類似于樣式的標準 HTML **旋轉** 屬性。

*VML 標準屬性*

**另請參閱**

**範例**

矩形將會傾斜45度。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[旋轉屬性範例](/previous-versions/bb264091(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 