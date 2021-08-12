---
title: VML Limo 屬性
description: VML Limo 屬性
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598308"
---
# <a name="vml-limo-attribute"></a>VML Limo 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義路徑上的延展點。 讀取/寫入 **Vector2D**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* limo = " *expression* " >

**指令碼語法**

 limo = "*expression*"

*運算式* =** limo

**備註**

預設值為 "0 0"。 Limo 伸展是指圖形邊緣上的點，可定義圖形在圖形化編輯器中的位置和方式。

*VML 標準屬性*

**範例**

Limo 延展點是定義于水平線的中間。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 