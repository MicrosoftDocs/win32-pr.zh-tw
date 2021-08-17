---
title: 'Size 屬性 (填滿)  (的 VML) '
description: 'Size 屬性 (填滿)  (的 VML) '
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754143"
---
# <a name="size-attribute-fillvml"></a>Size 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿影像的大小。 讀取/寫入 [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) 。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* size = " *expression* " >

**指令碼語法**

*元素* 。 size = "*expression * * *"**

*運算式* =*元素*。大小

**備註**

預設值是原始影像的大小。 大於 shapewill 的大小會顯示放大但裁剪的影像版本。

*VML 標準屬性*

**範例**

即使影像的原始大小是 50 50 點，影像在填滿的中央會顯示為 10 10 10 的影像。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 