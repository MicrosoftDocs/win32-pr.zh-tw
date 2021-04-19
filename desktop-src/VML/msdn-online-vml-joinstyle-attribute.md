---
title: VML JoinStyle 屬性
description: VML JoinStyle 屬性
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968908"
---
# <a name="vml-joinstyle-attribute"></a>VML JoinStyle 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義折線的聯結樣式。 讀取/寫入 字串。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* joinstyle = " *expression* " >

**指令碼語法**

 joinstyle = "*expression*"

*運算式* =** joinstyle

**備註**

數值包括：

-   四捨五入 (預設值) 
-   錐
-   長度

*VML 標準屬性*

**範例**

折線上的接點是斜邊。


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 