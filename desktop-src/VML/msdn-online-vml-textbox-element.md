---
title: VML TextBox 元素
description: VML TextBox 元素
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682424"
---
# <a name="vml-textbox-element"></a>VML TextBox 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的文字方塊。

下列屬性會修改文字方塊。



| 屬性                                                                    | 描述                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [方向]                         | 定義文字的方向。                         |
| [識別碼](id-attribute--textbox--vml.md)                                         | 定義文字方塊的唯一識別碼。               |
| [插圖](msdn-online-vml-inset-attribute.md)                                 | 指定 textbox 文字的內部邊界值。            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | 定義應用程式將如何允許自訂內凹值。 |
| [版面配置-流程](msdn-online-vml-layout-flow-attribute.md)                     | 決定文字方塊中文字的流程。            |
| [MSO 方向-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | 針對文字方塊中的文字定義替代的指示。        |
| [MSO-符合圖形-文字](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | 決定是否要將圖形延展成符合文字。       |
| [MSO-符合文字的形狀](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | 判斷文字是否會延展以符合圖形。       |
| [MSO-版面配置--Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | 定義文字方塊中文字的替代版面配置流程。   |
| [MSO-下一個文字方塊](msdn-online-vml-mso-next-textbox-attribute.md)           | 指定數列中的下一個文字方塊。                    |
| [MSO-旋轉](msdn-online-vml-mso-rotate-attribute.md)                       | 判斷文字是否以旋轉形狀旋轉。      |
| [MSO-文字-調整](msdn-online-vml-mso-text-scale-attribute.md)               | 定義將文字調整為圖形的調整比例。     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | 決定是否只要按一下就可以選取文字。 |
| [V-文字-錨點](msdn-online-vml-v-text-anchor-attribute.md)                 | 定義文字方塊中文字的垂直錨定。       |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

以下是產生 textbox 所需的最少程式碼。


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



請注意，文字方塊中顯示的文字是以 TextBox 標記括住。 標記內的文字可由一般 HTML 標籤修改。

**範例**

-   [簡易 TextBox 範例](/previous-versions/bb264075(v=vs.85))

 

 