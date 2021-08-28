---
title: VML Stroke 元素
description: VML Stroke 元素
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fa3b8293c8d540af47578ac522ff1cde179d8858c4f1e16aa95a0cd6e635e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513208"
---
# <a name="vml-stroke-element"></a>VML Stroke 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的筆觸。

下列屬性會修改筆劃。



| 屬性                                                          | 描述                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | 指定筆劃的替代參考。                |
| [色彩](color-attribute--stroke--vml.md)                          | 定義筆劃的色彩。                                |
| [Color2](color2-attribute--stroke--vml.md)                        | 定義筆觸的第二個色彩。                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | 指定筆劃的點和虛線模式。              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | 定義筆觸結尾的箭頭樣式。           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | 定義筆觸結尾的箭頭長度。          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | 定義筆觸結尾的箭頭寬度。           |
| [EndCap](msdn-online-vml-endcap-attribute.md)                     | 定義筆劃結尾的端點樣式。                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | 定義用於筆劃背景的填滿類型。 |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | 定義筆觸原始影像的 URL。         |
| [識別碼](id-attribute--stroke--vml.md)                                | 定義筆觸的唯一識別碼。                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | 決定筆劃影像的對齊方式。                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | 定義筆觸影像的外觀比例的保留方式。  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | 定義筆觸影像的大小。                 |
| [JoinStyle](msdn-online-vml-joinstyle-attribute.md)               | 定義折線的聯結樣式。                         |
| [線條樣式](msdn-online-vml-linestyle-attribute.md)               | 定義筆觸的線條樣式。                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | 定義斜接接點的平滑。                      |
| [開啟](on-attribute--stroke--vml.md)                                | 決定是否會顯示筆觸。              |
| [不透明度](opacity-attribute--stroke--vml.md)                      | 定義筆觸的透明度。               |
| [Src](src-attribute--stroke--vml.md)                              | 定義要為筆觸填滿載入的來源影像。           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | 定義筆觸起點的箭頭。              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | 定義筆劃起點的箭頭長度。       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | 定義筆觸起點的箭頭寬度。        |
| [標題](title-attribute--stroke--vml.md)                          | 定義筆觸的標題。                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | 定義筆觸的粗細。                            |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

下列程式碼示範如何使用 **Stroke** 元素來修改線條。


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**範例**

-   [簡單筆劃範例](/previous-versions/bb229466(v=vs.85))
-   [筆觸影像範例](/previous-versions/bb229468(v=vs.85))

 

 