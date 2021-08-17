---
title: VML ArcSize 屬性
description: VML ArcSize 屬性
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715440f56625d16ed5b4386120dbf50588ce861c1ba59772e3ec8f35a077dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755122"
---
# <a name="vml-arcsize-attribute"></a>VML ArcSize 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圓角矩形的圓度量。 讀取/寫入 [VgFraction](msdn-online-vml-vgfraction-data-type.md) 。

**適用於**

[RoundRect](msdn-online-vml-roundrect-element.md)

**標記語法**

<v： *element* arcsize = " *expression* " >

**指令碼語法**

 arcSize = "*expression*"

*運算式* =** arcSize

**備註**

將圓角矩形的圓角定義為矩形長度和寬度的一半寬度的百分比。 0% 的邊角，100% 會形成圓形角落。 **ArcSize** 值為1.0 的正方形會是一個圓形。 預設值為 0.2 (20% ) 。

*VML 標準屬性*

**範例**

圓角矩形會以緊密但圓角繪製。


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 