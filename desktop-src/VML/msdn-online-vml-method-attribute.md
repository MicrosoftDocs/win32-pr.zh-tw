---
title: VML 方法屬性
description: VML 方法屬性
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6b5ae67f94a2fc6e27451fb1a947c8341d1f77c08a721ca7946250cee3b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124761"
---
# <a name="vml-method-attribute"></a>VML 方法屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義用來產生漸層填滿的方法。 讀取/寫入 **VgSigmaType**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* method = " *expression* " >

**指令碼語法**

*元素* . method = "*expression*"

*運算式* =*element*。方法

**備註**

數值包括：



| 值  | 描述          |
|--------|----------------------|
| 無   | 沒有 sigma 填滿。       |
| 線性 | 線性 sigma 填滿。   |
| Sigma  | Sigma 填滿。 預設值。 |
| 任意    | 任何 sigma 填滿。      |



 

*VML 標準屬性*

**範例**

圖形會有紅色的線性漸層填滿。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 