---
title: VML EndCap 屬性
description: VML EndCap 屬性
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b2d36eb76b840ca8f89aebf3dadefaa68093394a07bd78db0e8fa0b18ed555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346713"
---
# <a name="vml-endcap-attribute"></a>VML EndCap 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆劃結尾的端點樣式。 讀取/寫入 **VgLineEndCapStyle**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* endcap = " *expression* " >

**指令碼語法**

 endcap = "*expression*"

*運算式* =** endcap

**備註**

數值包括：

-   一般 (預設) 
-   Square
-   Round

*VML 標準屬性*

**範例**

線條會以水準端點在筆劃的結尾繪製。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 