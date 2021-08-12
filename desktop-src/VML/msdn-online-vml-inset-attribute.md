---
title: VML 內凹屬性
description: VML 內凹屬性
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1d4b44756034a3ebc7e46e1cdda43042f347e58cb87c02b00c90a14320a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600234"
---
# <a name="vml-inset-attribute"></a>VML 內凹屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定 textbox 文字的內部邊界值。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* 內凹 = " *expression* " >

**指令碼語法**

*元素* . 內陷 = "*expression*"

*運算式* =*元素*。內凹

**備註**

內部文字邊界值會指定為包含四個值的字串，每個值都以逗號或空格分隔。 值會從 **Path** 的 [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)屬性所指定方塊的左邊、上、右和下邊緣測量內凹。 遺漏值會設定為預設值，也就是「0.1 in、0.05 in、0.1 in、0.05 in」。

如果是瀏覽器中不支援旋轉的旋轉圖形，周框方塊會貼齊最接近90度的倍數。

*VML 標準屬性*

**範例**

Textbox 會有10圖元的內凹邊界。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 