---
title: 'Color2 屬性 (Shadow)  (VML) '
description: 'Color2 屬性 (Shadow)  (VML) '
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241c7e0a620b6b5f2f54a8849779dcc905d027781fe38a5121ca74b6acbeac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655698"
---
# <a name="color2-attribute-shadowvml"></a>Color2 屬性 (Shadow)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義陰影的第二個色彩。 讀取/寫入 **VgColor**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* color2 = " *expression* " >

**指令碼語法**

 color2 = "*expression*"

*運算式* =** color2

**備註**

使用第二種色彩來建立特殊的陰影效果。 如需第二個色彩的詳細資訊，請參閱 [Type](type-attribute--shadow--vml.md) 屬性。

*VML 標準屬性*

**範例**

陰影的第二個色彩有藍色。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 