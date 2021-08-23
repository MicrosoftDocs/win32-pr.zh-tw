---
title: 'Type 屬性 (Shadow)  (VML) '
description: 'Type 屬性 (Shadow)  (VML) '
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513158"
---
# <a name="type-attribute-shadowvml"></a>Type 屬性 (Shadow)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定陰影的類型。 讀取/寫入 **字串**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* type = " *expression* " >

**指令碼語法**

*element* 。 type = "*expression*"

*運算式* =*元素*。類型

**備註**

數值包括：



| 值           | 描述                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | 單一陰影。 預設值。                                                                                                                                                                              |
| double          | 雙陰影。 [Color2](color2-attribute--shadow--vml.md) 用於第二個陰影的色彩，而 [Offset2](msdn-online-vml-offset2-attribute.md) 則用於第二個陰影的位移。 |
| 檢視方塊     | 觀點陰影。                                                                                                                                                                                |
| shapeRelative   | 相對於圖形，會建立陰影。                                                                                                                                                         |
| drawingRelative | 相對於繪圖，會建立陰影。                                                                                                                                                       |
| 浮雕          | 陰影具有浮凸外觀。                                                                                                                                                                     |



 

**VML 標準屬性**

**範例**

以第二個陰影綠色和位移5點向下和向右點建立雙重陰影。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 