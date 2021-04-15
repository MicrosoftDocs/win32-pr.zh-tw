---
title: 'AltHRef 屬性 (填滿)  (的 VML) '
description: 'AltHRef 屬性 (填滿)  (的 VML) '
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463309"
---
# <a name="althref-attribute-fillvml"></a>AltHRef 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義影像的替代參考。 讀取/寫入 **字串**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* o:althref = " *expression* " >

**指令碼語法**

 althref = "*expression*"

*運算式* =** althref

**備註**

支援透過 HTML roundtripping 保留 PICT 資料。 在 HTML 寫入時，如果已儲存來自 Apple Macintosh) 的檔案，則替代表示 (原始的 PICT 資料。 HTML 讀取時， **AltHRef** 優先于 **Src**。

*Microsoft Office Extensions 屬性*

**範例**

圖形的填滿具有指向名為 myimage.gif 之檔案的 **AltHRef** 。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 