---
title: VML 增益屬性
description: VML 增益屬性
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7b72f1588608f4988731111583e758b0207080eb3e02768a45b58c39071b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057826"
---
# <a name="vml-gain-attribute"></a>VML 增益屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義影像中所有色彩的濃度。 讀取/寫入 **VgNumber**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* 增益 = " *expression* " >

**指令碼語法**

*element* . 增益 = "*expression*"

*運算式* =*元素*。增益

**備註**

這個屬性會定義白色色彩的明暗程度，並影響所有其他色彩。 值的範圍是從0到無限大。 預設值為 1.0。 值為0時，不會顯示任何影像。 大於1的值會將圖片和小於1的值淡化，使圖片看似 grayer。

這個屬性可以用來建立有趣的效果。

*VML 標準屬性*

**範例**

影像將會顯示為灰色的所有色彩採用趨勢。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 