---
title: VML Fill 元素
description: VML Fill 元素
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b314e2d735b8b7800321eacffbd63c686b17e870fd136e086c52231ad801456e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346622"
---
# <a name="vml-fill-element"></a>VML Fill 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的填滿。

下列屬性會修改填滿。



| 屬性                                                          | 描述                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | 判斷影像是否要與圖形對齊。   |
| [AltHRef](althref-attribute--fill--vml.md)                        | 指定影像的替代參考。         |
| [角度](angle-attribute--fill--vml.md)                            | 定義漸層填滿的角度。                  |
| [層面](msdn-online-vml-aspect-attribute.md)                     | 指定如何保留填滿影像的外觀。 |
| [色彩](color-attribute--fill--vml.md)                            | 定義填滿的色彩。                           |
| [Color2](color2-attribute--fill--vml.md)                          | 定義填滿的第二個色彩。                   |
| [色彩](msdn-online-vml-colors-attribute.md)                     | 定義漸層填滿的多種色彩。           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | 決定是否偵測到滑鼠按一下。          |
| [焦點](msdn-online-vml-focus-attribute.md)                       | 定義線性漸層填滿的中心。          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | 定義放射狀漸層填滿的中心。          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | 定義星形填滿的焦點大小。              |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | 定義原始影像檔案的 URL。              |
| [識別碼](id-attribute--fill--vml.md)                                  | 定義填滿的唯一識別碼。              |
| [方法](msdn-online-vml-method-attribute.md)                     | 定義用來產生漸層填滿的方法。   |
| [開啟](on-attribute--fill--vml.md)                                  | 決定是否要顯示填滿。          |
| [不透明度](opacity-attribute--fill--vml.md)                        | 定義填滿的透明度。                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | 定義第二個填滿色彩的透明度。     |
| [起源](origin-attribute--fill--vml.md)                          | 定義影像的中心。                        |
| [位置](position-attribute--fill--vml.md)                      | 定義影像的位置。                      |
| [大小](size-attribute--fill--vml.md)                              | 定義影像的大小。                          |
| [Src](src-attribute--fill--vml.md)                                | 定義要載入填滿的影像。                  |
| [標題](title-attribute--fill--vml.md)                            | 定義填滿的標題。                           |
| [類型](type-attribute--fill--vml.md)                              | 定義填滿的類型。                              |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

下列程式碼顯示圖形的簡單漸層填滿。


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**範例**

-   [簡單漸層填滿](/previous-versions/bb229620(v=vs.85))
-   [動態填滿範例](/previous-versions/bb229621(v=vs.85))

 

 