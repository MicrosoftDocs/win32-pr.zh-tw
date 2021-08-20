---
title: VML StrokeColor 屬性
description: VML StrokeColor 屬性
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124231"
---
# <a name="vml-strokecolor-attribute"></a>VML StrokeColor 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆觸形狀路徑的筆刷色彩。 讀取/寫入 [IVgColor](msdn-online-vml-ivgcolor.md)。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* strokecolor = " *expression* " >

**指令碼語法**

 strokecolor = "*expression*"

*運算式* =** strokecolor

**備註**

此值會從 [Stroke](msdn-online-vml-stroke-element.md)元素的 **Color** 屬性複製。

*VML 標準屬性*

**範例**

矩形筆劃的色彩為紅色。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[StrokeColor 屬性範例](/previous-versions/bb264093(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 