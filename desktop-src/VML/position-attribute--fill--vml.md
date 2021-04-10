---
title: 'Position 屬性 (填滿)  (的 VML) '
description: 'Position 屬性 (填滿)  (的 VML) '
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093228"
---
# <a name="position-attribute-fillvml"></a>Position 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿影像的位置。 讀取/寫入 [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) 。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* position = " *expression* " >

**指令碼語法**

*element* 。 position = "*expression*"

*運算式* =*元素*。位置

**備註**

指定圖形中放置影像來源的點。 預設值為容器矩形的中心。 向量是影像寬度和高度的一小部分。

*VML 標準屬性*

**範例**

填滿的影像會右移至圖形寬度的點50%。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 