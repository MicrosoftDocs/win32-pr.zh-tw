---
title: VML TextBoxRect 屬性
description: VML TextBoxRect 屬性
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023544"
---
# <a name="vml-textboxrect-attribute"></a>VML TextBoxRect 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形內的一或多個文字方塊。 讀取/寫入 **字串**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* textboxrect = " *expression* " >

**指令碼語法**

 textboxrect = "*expression*"

*運算式* =** textboxrect

**備註**

Textbox 是由一或多組數位所定義，其中指定的 (順序) 矩形的左邊、頂端、右邊和底部點。 多個集合會以分號分隔。 預設值是與包含矩形相同的維度值。 如果定義了一個以上的 textbox，定義每個文字方塊的逗點分隔四組會以分號分隔。 文字方塊通常會在圖形上以1、2、3或6個矩形的組合來提供。

*VML 標準屬性*

**範例**

依95單位定義95單位的文字方塊會定義並放置在圖形左上角的5個單位。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 