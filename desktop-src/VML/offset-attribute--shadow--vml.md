---
title: 'Offset 屬性 (Shadow)  (VML) '
description: 'Offset 屬性 (Shadow)  (VML) '
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933303"
---
# <a name="offset-attribute-shadowvml"></a>Offset 屬性 (Shadow)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義陰影延伸超過圖形的距離。 讀取/寫入 **VgVector2D**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* offset = " *expression* " >

**指令碼語法**

*element* 。 offset = "*expression*"

*運算式* =*element*。 offset

**備註**

X 值的預設位移是2pt，y 值的預設值是2pt。 值可以是絕對測量值，或是 shape 的小數值。 如果是小數，則範圍從50% 到-50%。

*VML 標準屬性*

**範例**

圖形具有陰影，其位移為5點，而10指向右邊。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 