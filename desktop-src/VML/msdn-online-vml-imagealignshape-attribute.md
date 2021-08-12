---
title: VML ImageAlignShape 屬性
description: VML ImageAlignShape 屬性
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600466"
---
# <a name="vml-imagealignshape-attribute"></a>VML ImageAlignShape 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定筆觸影像的對齊方式。 讀取/寫入 **VgTriState**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v：

element *imagealignshape = "* expression *" >*

**指令碼語法**

*imagealignshape = "* expression *"*

expression *=* 元素 *. imagealignshape*

**備註**

若 **為 True**，則會將影像與圖形對齊，否則會將影像與視窗對齊。 預設值為 **True**。

*VML 標準屬性*

**範例**

影像會與視窗對齊。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 