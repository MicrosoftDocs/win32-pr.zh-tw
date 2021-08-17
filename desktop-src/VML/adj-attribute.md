---
title: 形容詞屬性
description: 形容詞屬性
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137141"
---
# <a name="adj-attribute"></a>形容詞屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定用來定義公式值的調整值。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* 形容詞 = " *expression* " >

**指令碼語法**

*element* 。形容詞 = "*expression*"

*運算式* =*元素*。形容詞

**備註**

調整 **是用** 來提供公式的可調式點。 如果用於標記中，則 **形容詞** 是以逗號分隔的字串，最多8個值。 可能會省略部分值。 例如，"0，1，2，，4，5，，7" 會是有效的字串，但第四個和第七個專案將不會有值 (從 0) 開始計算的專案。

針對腳本， **形容詞** 會使用 [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) 資料類型。

*VML 標準屬性*

**另請參閱**

[Formula](msdn-online-vml-formulas-element.md)

**範例**

使用調整來建立簡單的正方形。 首先，會建立 **形容詞** 字串來定義八個調整值。 然後每個調整值都是由八個公式的其中一個所參考，其中每個調整值前面加數位記號 (\#) 符號。 最後，會使用參考公式的字串來定義路徑，並以 "at" 正負號 ( @ ) 符號來前面加每個公式。


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



 (需要 Microsoft Internet Explorer 5 或更高版本的[形容詞屬性範例](/previous-versions/bb229662(v=vs.85))。 ) 

 

 