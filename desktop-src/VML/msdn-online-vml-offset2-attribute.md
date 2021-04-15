---
title: VML Offset2 屬性
description: VML Offset2 屬性
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508091"
---
# <a name="vml-offset2-attribute"></a>VML Offset2 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定第二個位移。 讀取/寫入 **VgVector2D**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* offset2 = " *expression* " >

**指令碼語法**

 offset2 = "*expression*"

*運算式* =** offset2

**備註**

X 值的第二個位移預設值為0，而 y 值的預設值為0。 值可以是絕對測量值，或是 shape 的小數值。 如果是小數，則值的範圍是從50% 到-50%。

使用第二個位移來建立特殊的陰影效果。 如需第二個位移的詳細資訊，請參閱 [Type](type-attribute--shadow--vml.md) 屬性。

*VML 標準屬性*

**範例**

為圖形建立雙重陰影。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 