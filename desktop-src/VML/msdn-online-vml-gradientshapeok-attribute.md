---
title: VML GradientShapeOK 屬性
description: VML GradientShapeOK 屬性
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124771"
---
# <a name="vml-gradientshapeok-attribute"></a>VML GradientShapeOK 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷漸層路徑是否會由重複的同心圓路徑組成。 讀取/寫入 **VgTriState**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* gradientshapeok = " *expression* " >

**指令碼語法**

 gradientshapeok = "*expression*"

*運算式* =** gradientshapeok

**備註**

若 **為 True**，則會使用路徑作為漸層的重複圖形來填滿路徑，並以同心圓漸層填滿。預設值為 **False**。

*VML 標準屬性*

**範例**

路徑將會填入由重複矩形組成的同心圓漸層填滿。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 