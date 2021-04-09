---
title: '若要將 (曲線屬性)  (VML) '
description: '若要將 (曲線屬性)  (VML) '
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842711"
---
# <a name="to-attribute-curvevml"></a>若要將 (曲線屬性)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義曲線的結束點。 讀取/寫入 **VgVector2D**。

**適用於**

[曲線](msdn-online-vml-curve-element.md)

**標記語法**

<v： *element* to = " *expression* " >

**指令碼語法**

*element* 。 to = "*expression*"

*運算式* =*元素*。

**備註**

在父元素的座標空間中定義三次方貝茲曲線的結束點。 如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。 預設值為30、20。

**VML 標準屬性**

**範例**

曲線是微笑的。 它會從左邊開始，並在右側結束。 這兩個控制點的位置是以拉下曲線來提供笑臉的外觀。


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 