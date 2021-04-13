---
title: VML Alt 屬性
description: VML Alt 屬性
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186083"
---
# <a name="vml-alt-attribute"></a>VML Alt 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義要顯示的替代文字，而不是圖形。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* alt = " *expression* " >

**指令碼語法**

*element* 。 alt = "*expression*"

*運算式* =*元素*。 alt

**備註**

**Alt** 屬性類似于標準 HTML **Alt** 屬性。 這個屬性會提供一種方式，讓瀏覽器將文字轉換成語音，以描述頁面上的圖形元素。

*VML 標準屬性*

**另請參閱**

[形狀](shape-element--vml.md)

**範例**

下列 **Alt** 元素將會在瀏覽器中顯示將網頁轉換成說話片語的「紅色矩形」片語。


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Alt 屬性範例](/previous-versions/bb229663(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 