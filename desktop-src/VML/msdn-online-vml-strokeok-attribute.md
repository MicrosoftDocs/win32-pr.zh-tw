---
title: VML StrokeOK 屬性
description: VML StrokeOK 屬性
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5051f3a2d5e7ac8e4d509d8b8f65182f86799db41bbd8a4d71741961c3a1e406
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475218"
---
# <a name="vml-strokeok-attribute"></a>VML StrokeOK 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否會顯示筆觸。 讀取/寫入 **VgTriState**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* strokeok = " *expression* " >

**指令碼語法**

 strokeok = "*expression*"

*運算式* =** strokeok

**備註**

如果 **為 False**，則表示路徑無法繪製。 預設值為 **True**。 這個屬性會覆寫父元素或 **筆劃** 元素中的所有其他筆觸屬性。

*VML 標準屬性*

**範例**

將不會對路徑進行筆劃。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 