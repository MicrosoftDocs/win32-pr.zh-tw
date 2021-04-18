---
title: 'On 屬性 (筆觸)  (VML) '
description: 'On 屬性 (筆觸)  (VML) '
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968914"
---
# <a name="on-attribute-strokevml"></a>On 屬性 (筆觸)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否會顯示筆觸。 讀取/寫入 **VgTriState**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* on = " *expression* " >

**指令碼語法**

*element* . on = "*expression*"

*運算式* =*元素*。開啟

**備註**

如果 **為 False**，則不會顯示筆觸。 預設值為 **True**。

*VML 標準屬性*

**範例**

將不會顯示筆觸。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 