---
title: VML StrokeWeight 屬性
description: VML StrokeWeight 屬性
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682550"
---
# <a name="vml-strokeweight-attribute"></a>VML StrokeWeight 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆觸形狀路徑的筆刷厚度。 讀取/寫入 **VGLength**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* strokeweight = " *expression* " >

**指令碼語法**

 strokeweight = "*expression*"

*運算式* =** strokeweight

**備註**

此值會從 **Stroke** 元素的 **權數** 屬性複製。 如果指定了數位，但未加入任何單位，則預設度量單位是 Emu。 如果未指定任何值，預設值為1圖元 (1px) 。

不過，針對腳本，預設測量單位是以點為單位。

*VML 標準屬性*

**另請參閱**

[Stroke](msdn-online-vml-stroke-element.md)、 [IVgLength](msdn-online-vml-vglength.md)、 [單位](msdn-online-vml-units.md)

**範例**

圖形的筆觸粗細為1點。


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[StrokeWeight 屬性範例](/previous-versions/bb264095(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 