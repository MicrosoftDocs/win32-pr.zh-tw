---
title: '原始屬性 (填滿)  (的 VML) '
description: '原始屬性 (填滿)  (的 VML) '
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc33ae1f4cf7c588ae9b3f40ff8c445be88192bae1dfc86a3593eea931befb25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959218"
---
# <a name="origin-attribute-fillvml"></a>原始屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿影像的中心。 讀取/寫入 [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) 。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* 原點 = " *expression* " >

**指令碼語法**

*element* 。源 = "*expression*"

*運算式* =*元素*。來源

**備註**

指定相對於影像左上角的點;此點會被視為影像的來源。 預設值是影像的中心。 向量是影像寬度和高度的一小部分。

*VML 標準屬性*

**範例**

填滿的影像會向左移位至圖形寬度的點50%。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 