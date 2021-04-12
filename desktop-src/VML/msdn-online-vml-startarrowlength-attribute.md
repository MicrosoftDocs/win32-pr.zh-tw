---
title: VML StartArrowLength 屬性
description: VML StartArrowLength 屬性
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375853"
---
# <a name="vml-startarrowlength-attribute"></a>VML StartArrowLength 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線條開頭的箭頭長度。 讀取/寫入 **VgArrowheadLength**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* startarrowlength = " *expression* " >

**指令碼語法**

 startarrowlength = "*expression*"

*運算式* =** startarrowlength

**備註**

數值包括：

-   Short
-   中 (預設)
-   long

VML 標準屬性

**範例**

在筆劃的開頭，以簡短的傳統箭頭繪製線條。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 