---
title: VML 填滿屬性
description: VML 填滿屬性
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7053263f989dbbef163e04ca19e28afa882d20347b103c97cf2db3be4b8d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346602"
---
# <a name="vml-filled-attribute"></a>VML 填滿屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷是否會填滿關閉的路徑。 讀取/寫入 **VgTriState**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* 填入 = " *expression* " >

**指令碼語法**

*元素* . 填滿 = "*expression*"

*運算式* =*元素*。已填滿

**備註**

此值會從 [Fill](msdn-online-vml-fill-element.md)元素的 **On** 屬性複製。

*VML 標準屬性*

**範例**

圖形路徑會填滿。


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[填滿屬性範例](/previous-versions/bb229669(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 