---
title: VML BlackLevel 屬性
description: VML BlackLevel 屬性
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057906"
---
# <a name="vml-blacklevel-attribute"></a>VML BlackLevel 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義影像中的黑色濃度。 讀取/寫入 **VgNumber**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* blacklevel = " *expression* " >

**指令碼語法**

 blacklevel = "*expression*"

*運算式* =** blacklevel

**備註**

允許修改色彩層級，讓黑色顯示為 true 黑色，而其他所有色彩則會顯示為黑色以上的陰影。 預設值為 0。 雖然允許正和負無限大之間的任何數位，但小於-0.5 的值會顯示為所有的黑色，而大於0.5 的值會顯示為全部白色。

*VML 標準屬性*

**範例**

影像將會顯示為非常深的色調。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 