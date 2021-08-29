---
title: VML StartArrow 屬性
description: VML StartArrow 屬性
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b0d1ce8d352ef119e2745d0f7768332ad074d134877b03433aa788f1bb2e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754480"
---
# <a name="vml-startarrow-attribute"></a>VML StartArrow 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線條開頭的箭頭。 讀取/寫入 **字串**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* startarrow = " *expression* " >

**指令碼語法**

 startarrow = "*expression*"

*運算式* =** startarrow

**備註**

數值包括：

-   [無] (預設值)
-   封鎖
-   傳統
-   菱形
-   橢圓形
-   開啟

VML 標準屬性

**範例**

在筆劃的開頭繪製一條線，並使用傳統箭頭。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 