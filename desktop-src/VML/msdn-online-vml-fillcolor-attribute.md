---
title: VML FillColor 屬性
description: VML FillColor 屬性
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601358"
---
# <a name="vml-fillcolor-attribute"></a>VML FillColor 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿形狀封閉路徑的筆刷色彩。 讀取/寫入 [IVgColor](msdn-online-vml-ivgcolor.md) 。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* fillcolor = " *expression* " >

**指令碼語法**

 fillcolor = "*expression*"

*運算式* =** fillcolor

**備註**

**FillColor** 值會從 **Fill** 元素的 **Color** 屬性複製而來。

*VML 標準屬性*

**另請參閱**

[Shape](shape-element--vml.md)、 [Fill](msdn-online-vml-fill-element.md)、 [IVgColor](msdn-online-vml-ivgcolor.md)

**範例**

矩形的填滿色彩為紅色。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[FillColor 屬性範例](/previous-versions/bb229668(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 