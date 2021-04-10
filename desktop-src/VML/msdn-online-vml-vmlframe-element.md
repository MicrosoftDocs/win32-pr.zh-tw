---
title: VML VMLFrame 元素
description: VML VMLFrame 元素
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092785"
---
# <a name="vml-vmlframe-element"></a>VML VMLFrame 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義外部形狀的框架。

下列屬性會修改框架。



| 屬性                                     | 描述                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [剪輯](msdn-online-vml-clip-attribute.md)    | 判斷是否會裁剪影像。                         |
| [識別碼](id-attribute--vmlframe--vml.md)         | 定義框架的唯一識別碼。                            |
| [起源](origin-attribute--vmlframe--vml.md) | 指定框架的原點。                                    |
| [大小](size-attribute--vmlframe.md)          | 指定框架的大小。                                      |
| [Src](src-attribute--vmlframe--vml.md)       | 指定要顯示在框架中的資料來源。 |
| [Style](msdn-online-vml-style-attribute.md)  | 定義可以用來放置框架的一般 CSS 樣式。 |



 

**備註**

要顯示在框架中的來源資料可以包含在相同的網頁中，也可以是另一個頁面的一部分。 透過腳本，可以動態變更來源，並可修改顯示特性。

**VMLFrame** 內的物件為「縮放比例」。 亦即，它們會像中繼檔一樣調整，其中線條粗細、陰影位移和文字區域都會按星號調整。 這與群組不同，其中的物件大小和位置會依比例調整，但是線條、陰影等則不會。

以下是將影像載入框架所需的最少程式碼。


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



如果檔案是外部檔案，它必須是 XML 檔。 下列程式碼是指定必須包含可識別之圖形的外部原始程式檔時所需的最少程式碼。 此範例包含顯示點陣圖的影像圖形。


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> 在 VML 的發行前版本中，這個元素稱為 **VMLCanvas** 。

 

**範例**

-   [簡單 VMLFrame 範例](/previous-versions/bb263920(v=vs.85))
-   [動態 VMLFrame 範例](/previous-versions/bb263902(v=vs.85))

 

 