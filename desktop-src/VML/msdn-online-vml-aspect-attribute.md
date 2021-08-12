---
title: VML 外觀屬性
description: VML 外觀屬性
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602895"
---
# <a name="vml-aspect-attribute"></a>VML 外觀屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定如何保留填滿影像的外觀比例。 讀取/寫入 **字串**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* 方位 = " *expression* " >

**指令碼語法**

*元素* 。外觀 = "*expression*"

*運算式* =*元素*。外觀

**備註**

數值包括：



| 值   | 描述                           |
|---------|---------------------------------------|
| ignore  | 略過外觀問題。 預設值。        |
| 至少 | 影像的大小至少會和 **大小** 一樣大。 |
| 有  | 影像的大小不會大於 **大小**。     |



 

*VML 標準屬性*

**範例**

組成填滿的影像大於或等於10點的10點大小。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 