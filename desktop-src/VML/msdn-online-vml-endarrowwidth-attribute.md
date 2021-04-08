---
title: VML EndArrowWidth 屬性
description: VML EndArrowWidth 屬性
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683071"
---
# <a name="vml-endarrowwidth-attribute"></a>VML EndArrowWidth 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

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



 

 