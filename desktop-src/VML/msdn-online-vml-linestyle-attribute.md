---
title: VML LineStyle 屬性
description: VML LineStyle 屬性
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682389"
---
# <a name="vml-linestyle-attribute"></a>VML LineStyle 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義筆觸的線條樣式。 讀取/寫入 **字串**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* linestyle = " *expression* " >

**指令碼語法**

 linestyle = "*expression*"

*運算式* =** linestyle

**備註**

數值包括：

-   單一 (預設) 
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*VML 標準屬性*

**範例**

以兩個細筆觸繪製雙線。


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 