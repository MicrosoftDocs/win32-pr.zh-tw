---
title: '若要 (行的屬性)  (VML) '
description: '若要 (行的屬性)  (VML) '
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683065"
---
# <a name="to-attribute-linevml"></a>若要 (行的屬性)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義線條的結束點。 讀取/寫入 **VgVector2D**。

**適用於**

[線條](msdn-online-vml-line-element.md)

**標記語法**

<v： *element* to = " *expression* " >

**指令碼語法**

*element* 。 to = "*expression*"

*運算式* =*元素*。

**備註**

在父元素的座標空間中，定義線條的結束點。如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。 預設值為10、10。

**VML 標準屬性**

**範例**

該行會以位置100點向下和100指向父空間左上角的右邊。


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 