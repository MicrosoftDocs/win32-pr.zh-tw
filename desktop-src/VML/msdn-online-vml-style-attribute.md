---
title: VML 樣式屬性
description: VML 樣式屬性
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475188"
---
# <a name="vml-style-attribute"></a>VML 樣式屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義框架的樣式。 讀取/寫入 **字串**。

**適用於**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**標記語法**

<v： *element* style = " *expression* " >

**指令碼語法**

*元素* 。 style = "*expression*"

*運算式* =*element*。 style

**備註**

這個屬性會使用一般 CSS 樣式屬性來進行定位。

*VML 標準屬性*

**範例**

樣式會定義框架的實際位置。


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 