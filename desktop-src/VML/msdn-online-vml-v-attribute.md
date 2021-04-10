---
title: VML V 屬性
description: VML V 屬性
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092827"
---
# <a name="vml-v-attribute"></a>VML V 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義組成路徑的命令。 讀取/寫入 **字串**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* v = " *expression* " >

**指令碼語法**

*元素* . v = "*expression*"

*運算式* =*元素*. v

**備註**

覆寫圖形的 **Path** 屬性。 座標可以是固定數位、相對值或公式的參考 (使用 "" 格式， @n 其中 n 是公式編號，例如，" @2 " 代表公式陣列中的第二個公式) 。

*VML 標準屬性*

**範例**

使用 **V** 屬性來建立矩形。 請注意，在第一組以逗號分隔的座標之後，會使用小寫字母 L (**lineto** 命令) 。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 