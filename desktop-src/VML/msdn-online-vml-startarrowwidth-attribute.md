---
title: VML StartArrowWidth 屬性
description: VML StartArrowWidth 屬性
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513238"
---
# <a name="vml-startarrowwidth-attribute"></a>VML StartArrowWidth 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線條開頭的箭頭寬度。 讀取/寫入 **VgArrowheadWidth**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* startarrowwidth = " *expression* " >

**指令碼語法**

 startarrowwidth = "*expression*"

*運算式* =** startarrowwidth

**備註**

數值包括：

-   狹窄
-   中 (預設)
-   寬

VML 標準屬性

**範例**

在筆劃的開頭，以寬型的箭頭繪製線條。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 