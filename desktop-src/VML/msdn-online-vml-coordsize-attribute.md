---
title: VML CoordSize 屬性
description: VML CoordSize 屬性
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965649"
---
# <a name="vml-coordsize-attribute"></a>VML CoordSize 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定圍繞圖形之矩形的水準和垂直單位。 讀取/寫入 [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* coordsize = " *expression* " >

**指令碼語法**

 coordsize = "*expression*"

*運算式* =** coordsize

**備註**

如果未指定，座標大小與圖形的周框方塊相同。

請注意，此屬性是向量，而且單位是相對於周框矩形的長度和寬度。

另請注意， **coordsize** 和周框方塊之間的對應可設為非等的。 如果您不想要扭曲圖形，請確定 **coordsize 寬度** 和 **coordsize 高度** 與 **樣式寬度** 和 **高度** 相同。

在腳本中，因為這是2D 向量，所以您可以分別存取 x 和 y 值，也可以決定預期的單位類型。

*VML 標準屬性*

**範例**

圖形是100點高和100點寬，但座標空間中的每個水準和垂直單位都是點的1/10。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[CoordSize 屬性範例](/previous-versions/bb229665(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 