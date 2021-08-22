---
title: VML EndArrowWidth 屬性
description: VML EndArrowWidth 屬性
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90270cfc554d7e2dea70b313507fd7f61bf3a073c0e27c03c82d8a696f2939a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396078"
---
# <a name="vml-endarrowwidth-attribute"></a>VML EndArrowWidth 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線條結尾的箭頭寬度。 讀取/寫入 **VgArrowheadWidth**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* endarrowwidth = " *expression* " >

**指令碼語法**

 endarrowwidth = "*expression*"

*運算式* =** endarrowwidth

**備註**

數值包括：

-   狹窄
-   中 (預設)
-   寬

*VML 標準屬性*

**範例**

在筆劃末端以寬型的箭頭繪製線條。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 