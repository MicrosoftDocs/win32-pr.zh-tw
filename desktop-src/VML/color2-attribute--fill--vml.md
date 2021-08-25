---
title: 'Color2 屬性 (填滿)  (的 VML) '
description: 'Color2 屬性 (填滿)  (的 VML) '
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007888"
---
# <a name="color2-attribute-fillvml"></a>Color2 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿的第二個色彩。 讀取/寫入 [VgColor](msdn-online-vml-ivgcolor.md) 。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* color2 = " *expression* " >

**指令碼語法**

 color2 = "*expression*"

*運算式* =** color2

**備註**

當填滿型別是模式或漸層時，就會使用第二個色彩。 預設值為 **白色**。

*VML 標準屬性*

**範例**

圖形的填滿型別是一種模式，其前景填滿是由來源影像所定義，但透明背景則是以第二種色彩來定義。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 