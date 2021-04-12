---
title: VML ImageAspect 屬性
description: VML ImageAspect 屬性
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315616"
---
# <a name="vml-imageaspect-attribute"></a>VML ImageAspect 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆觸影像的外觀比例的保留方式。 讀取/寫入 **字串**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v：

element *imageaspect = "* expression *" >*

**指令碼語法**

*imageaspect = "* expression *"*

expression *=* 元素 *. imageaspect*

**備註**

數值包括：



| 值   | 描述                                |
|---------|--------------------------------------------|
| 忽略  | 略過外觀問題。                      |
| 至少 | 影像的大小至少與 **ImageSize** 相同。 |
| 有  | 影像已不大於 **ImageSize**。     |



 

在每個案例中， **ImageSize** 屬性將會調整以保持影像的外觀。

*VML 標準屬性*

**範例**

筆劃影像的大小至少會和影像大小一樣大。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 