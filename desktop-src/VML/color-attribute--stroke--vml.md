---
title: 'Color 屬性 (筆觸)  (VML) '
description: 'Color 屬性 (筆觸)  (VML) '
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967491"
---
# <a name="color-attribute-strokevml"></a>Color 屬性 (筆觸)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆劃的色彩。 讀取/寫入 **VgColor**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* color = " *expression* " >

**指令碼語法**

*element* 。 color = "*expression*"

*運算式* =*元素*。色彩

**備註**

覆寫圖形的 **StrokeColor** 屬性。 預設值為 **黑色**。

*VML 標準屬性*

**範例**

圖形具有 **綠色** 的筆觸色彩，而不是 **紅色**。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 