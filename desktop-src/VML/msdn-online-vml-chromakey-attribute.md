---
title: VML Chromakey 屬性
description: VML Chromakey 屬性
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315634"
---
# <a name="vml-chromakey-attribute"></a>VML Chromakey 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義將被視為透明影像的色彩值。 讀取/寫入 **VgColor**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* chromakey = " *expression* " >

**指令碼語法**

 chromakey = "*expression*"

*運算式* =** chromakey

**備註**

您可以使用此屬性，藉由將透明度加密為特定色彩，讓影像的部分變成透明。 例如，如果您將 **Chromakey** 值設為 **黑色**，則影像中任何黑色的部分將會是透明的，填滿色彩將會「顯示」影像的該部分。

*VML 標準屬性*

**範例**

實心黑色影像的區域會變成透明的，允許綠色填滿色彩改為顯示在這些區域中。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 