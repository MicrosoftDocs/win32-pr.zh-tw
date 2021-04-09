---
title: 'HRef 屬性 (ImageData)  (VML) '
description: 'HRef 屬性 (ImageData)  (VML) '
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682390"
---
# <a name="href-attribute-imagedatavml"></a>HRef 屬性 (ImageData)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義影像的 URL。 讀取/寫入 **字串**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* o:href = " *expression* " >

**指令碼語法**

*元素* 。 href = "*expression*"

*運算式* =*元素* href

**備註**

按一下圖形時，瀏覽器會載入 URL。 **HRef** 屬性類似于錨點的標準 HTML **HRef** 屬性。

使用這個屬性可讓您輕鬆地在網頁上建立 buttonswith 影像。

只有在已連結和內嵌圖片時，Microsoft Office 才會使用這個屬性。Microsoft Word 具有以這種方式插入圖片的使用者介面。

*Microsoft Office Extensions 屬性*

**範例**

按一下影像時，瀏覽器會載入 Microsoft Corporation 首頁。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 