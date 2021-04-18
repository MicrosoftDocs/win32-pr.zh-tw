---
title: VML 色彩屬性
description: VML 色彩屬性
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508032"
---
# <a name="vml-colors-attribute"></a>VML 色彩屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義漸層填滿的多種色彩。 讀取/寫入 **IVgGradientColorArray**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* colors = " *expression* " >

**指令碼語法**

*元素* 。 colors = "*expression*"

*運算式* =*元素*。色彩

**備註**

用來定義包含成對百分比值的陣列 ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) 和 Color ([VgColor](msdn-online-vml-ivgcolor.md)) 。 陣列會使用陣列中的每個點來建立混合填滿，從 0% (開始，) 由 **色彩** 定義，並在 **Color2**) 所定義的 100% (結束。 您可以藉由將色彩值指派為百分比來定義中間色彩。 百分比和色彩組不會以逗號分隔，但配對會以逗號分隔。

VML 標準屬性

**範例**

圖形具有由四種色彩組成的漸層填滿，開頭為紅色、混合成黃色、綠色和 finallyblue。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 