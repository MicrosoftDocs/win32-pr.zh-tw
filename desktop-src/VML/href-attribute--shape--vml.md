---
title: 'HRef 屬性 (圖形)  (VML) '
description: 'HRef 屬性 (圖形)  (VML) '
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024002"
---
# <a name="href-attribute-shapevml"></a>HRef 屬性 (圖形)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的 URL。 按一下圖形時，瀏覽器會載入 URL。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* href = " *expression* " >

**指令碼語法**

*元素* 。 href = "*expression*"

*運算式* =*元素* href

**備註**

**HRef** 屬性類似于錨點的標準 HTML **HRef** 屬性。

使用 **HRef** 可讓您輕鬆地在網頁上建立有趣的按鈕。

*VML 標準屬性*

**範例**

按一下矩形時，瀏覽器會載入 Microsoft Corporation 首頁。


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[HRef 屬性範例](/previous-versions/bb229672(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 