---
title: VML FocusSize 屬性
description: VML FocusSize 屬性
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024069"
---
# <a name="vml-focussize-attribute"></a>VML FocusSize 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義星形填滿的焦點大小。 讀取/寫入 **VgVector2D**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* focussize = " *expression* " >

**指令碼語法**

 focussize = "*expression*"

*運算式* =** focussize

**備註**

這些值是圖形寬度和高度的分數。 第一個是圖形右邊緣填滿的百分比，而第二個則是圖形底部填滿的百分比。 預設值為 0,0。 **FocusSize** 值為100%、100% 且 **FocusPosition** 為0，0會讓 Color2 完全在 blend 中佔據。 如果有大約10% 的小值，建議將10% 用於平衡的混合。

*VML 標準屬性*

**範例**

星形填滿會在中間以藍色開始建立 blend，並在所有四個邊緣變成紅色。 Blend 的中心是由 **FocusPosition** 所定義，而內部開始色彩的大小是由 **FocusSize** 所決定。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 