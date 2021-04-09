---
title: VML Bilevel 屬性
description: VML Bilevel 屬性
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682610"
---
# <a name="vml-bilevel-attribute"></a>VML Bilevel 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷影像是否會以黑色和白色顯示。 讀取/寫入 **VgTriState**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* bilevel = " *expression* " >

**指令碼語法**

 bilevel = "*expression*"

*運算式* =** bilevel

**備註**

若 **為 True**，則會使用兩種色彩來顯示影像 (黑色和白色) 。 預設值為 **False**。 這會建立類似于 posterization 的效果。

*VML 標準屬性*

**範例**

影像只會以黑色和白色顯示。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 