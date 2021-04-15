---
title: " (筆觸)  (VML) 的不透明度屬性"
description: " (筆觸)  (VML) 的不透明度屬性"
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463665"
---
# <a name="opacity-attribute-strokevml"></a> (筆觸)  (VML) 的不透明度屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆觸的透明度。 讀取/寫入 **VgFraction**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* opacity = " *expression* " >

**指令碼語法**

*元素* 。不透明度 = "*expression*"

*運算式* =*元素*。不透明度

**備註**

預設值為 1.0。

*VML 標準屬性*

**範例**

筆劃為50% 透明。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 