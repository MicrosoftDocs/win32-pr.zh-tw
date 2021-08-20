---
title: '色彩屬性 (填滿)  (的 VML) '
description: '色彩屬性 (填滿)  (的 VML) '
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ec72cab0562ae675ca2e22992369a7c0ad6534207cd2a6f6141f56c64e2f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125378"
---
# <a name="color-attribute-fillvml"></a>色彩屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿的色彩。 讀取/寫入 **VgColor**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* color = " *expression* " >

**指令碼語法**

*element* 。 color = "*expression*"

*運算式* =*元素*。色彩

**備註**

覆寫圖形的 **FillColor** 屬性。 預設值為 **白色**。

*VML 標準屬性*

**範例**

圖形的填滿色彩為綠色。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 