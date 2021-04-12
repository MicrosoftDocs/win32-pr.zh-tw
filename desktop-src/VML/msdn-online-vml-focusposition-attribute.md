---
title: VML FocusPosition 屬性
description: VML FocusPosition 屬性
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093276"
---
# <a name="vml-focusposition-attribute"></a>VML FocusPosition 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義放射狀漸層的中心。 讀取/寫入 **VgVector2D**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* focusposition = " *expression* " >

**指令碼語法**

 focusposition = "*expression*"

*運算式* =** focusposition

**備註**

指定中央 positionfor 放射狀漸層。 向量是圖形寬度和高度的一小部分。 第一個是左邊緣填滿的百分比;第二個是填滿至頂端的百分比。 預設值為 0,0。 若要在圖形中央放置星形填滿，請使用 50% 50% 的值。

*VML 標準屬性*

**範例**

星形填滿將會置中，如此一來，藍色將會從中央開始，並從外進入，並在到達外緣和角落時逐漸變更為紅色。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 