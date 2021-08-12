---
title: 'Type 屬性 (Fill)  (VML) '
description: 'Type 屬性 (Fill)  (VML) '
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596139"
---
# <a name="type-attribute-fillvml"></a>Type 屬性 (Fill)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定填滿的型別。 讀取/寫入 **VgFillType**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* type = " *expression* " >

**指令碼語法**

*element* 。 type = "*expression*"

*運算式* =*元素*。類型

**備註**

數值包括：



| 類型           | 描述                                                             |
|----------------|-------------------------------------------------------------------------|
| 固體          | 填滿模式是實心。 預設值。                                     |
| 漸層       | 填滿色彩會以線性漸層（從下到上）混合在一起。 |
| gradientradial | 填滿色彩會在放射狀漸層中一起混合。                    |
| 磚           | 填滿影像會並排顯示。                                                |
| 模式        | 影像可用來建立使用填滿色彩的模式。            |
| 框架          | 影像會伸展以填滿形狀。                               |



 

**VML 標準屬性**

**範例**

紅色的前景和藍色背景填滿是使用影像 myimage.gif 的模式所建立。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 