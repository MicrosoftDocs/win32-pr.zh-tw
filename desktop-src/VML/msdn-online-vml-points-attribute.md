---
title: VML 點屬性
description: VML 點屬性
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023571"
---
# <a name="vml-points-attribute"></a>VML 點屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義組成折線的一組點。 讀取/寫入 [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) 。

**適用於**

[聚合線條](msdn-online-vml-polyline-element.md)

**標記語法**

<v： *element* points = " *expression* " >

**指令碼語法**

*元素* 。 points = "*expression * * *"**

*運算式* =*元素*。點

**備註**

定義一組由一連串的點組成的直線線段。 如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。 預設值為 "0，0 10，10"。 請注意，逗號並非必要，但可讓您更容易閱讀。

*VML 標準屬性*

**範例**

聚合線條從點10、10開始到100100，並以值點開始。


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 