---
title: '不透明度屬性 (陰影)  (VML) '
description: '不透明度屬性 (陰影)  (VML) '
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680618"
---
# <a name="opacity-attribute-shadowvml"></a>不透明度屬性 (陰影)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定陰影的透明度。 讀取/寫入 [VgFraction](msdn-online-vml-vgfraction-data-type.md) 。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* opacity = " *expression* " >

**指令碼語法**

*元素* 。不透明度 = "*expression*"

*運算式* =*元素*。不透明度

**備註**

預設值為 1。 值為0會產生完全透明的陰影。

*VML 標準屬性*

**範例**

圖形的陰影有50% 的透明。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 