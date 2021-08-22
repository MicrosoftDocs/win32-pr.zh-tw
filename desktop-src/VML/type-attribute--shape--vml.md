---
title: '類型屬性 (圖形)  (VML) '
description: '類型屬性 (圖形)  (VML) '
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513148"
---
# <a name="type-attribute-shapevml"></a>類型屬性 (圖形)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義 [ShapeType](msdn-online-vml-shapetype-element.md) 元素之識別碼的參考。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

``` syntax
<v:
          element 
          type=" expression ">
```

**指令碼語法**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**備註**

如果 **Type** 屬性參考 **SHAPETYPE** 元素的識別碼，則會使用 **ShapeType** 的填滿、路徑和筆劃做為範本來建立圖形。 衍生自 **ShapeType** 的值可以由個別圖形值覆寫。

如果用於標記中，字串值的開頭必須是數位記號 (\#) 符號。

**VML 標準屬性**

**範例**

使用 "mytype" 做為識別碼來建立 **ShapeType** 圖形。


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



然後，如果您使用 **ShapeType** 值建立圖形，此圖形將會有 "Mytype" **ShapeType** 的屬性;亦即，"shape01" 會有藍色筆劃的紅色填滿。


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



您可以覆寫繼承的值，例如，將色彩變更為綠色。


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Type 屬性範例](/previous-versions/bb264099(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 