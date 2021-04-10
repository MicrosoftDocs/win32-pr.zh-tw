---
title: VML 邊邊屬性
description: VML 邊邊屬性
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093232"
---
# <a name="vml-stroked-attribute"></a>VML 邊邊屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義是否要將路徑繪製。 讀取/寫入 [VgTriState](msdn-online-vml-vgtristate.md) 。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *元素* 已邊邊 = " *expression* " >

**指令碼語法**

*元素* 。筆劃 = "*expression*"

*運算式* =*元素*。邊邊

**備註**

此值會從 [Stroke](msdn-online-vml-stroke-element.md)元素的 **On** 屬性複製。

*VML 標準屬性*

**範例**

圖形路徑會進行筆劃。


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[描邊屬性範例](/previous-versions/bb264094(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 