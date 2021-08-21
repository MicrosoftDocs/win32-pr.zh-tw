---
title: 使用 Path 元素
description: 使用 Path 元素
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- 網路研討會，path 元素
- 設計網頁、path 元素
- Vector Markup Language (VML) 、path 元素
- VML (Vector Markup Language) ，path 元素
- 向量圖形，path 元素
- path 元素
- VML 元素，路徑
- VML 圖形，path 元素
- Vector Markup Language (VML) 、自訂圖形大綱
- VML (Vector Markup Language) 、自訂圖形大綱
- 向量圖形，自訂圖形大綱
- VML 圖形，自訂大綱
- 自訂圖形大綱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cbb27dbc2b039478903f697b02cefb14464b71a96ab2165db124d0a0053a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057179"
---
# <a name="using-the-path-element"></a>使用 Path 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

您已瞭解您可以使用 VML 預先定義的圖形元素，例如、、 `<oval>` 、、、 `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` 和 `<arc>` --繪製圖形。 在本主題中，我們將說明如何使用 `<path>` 子項目自訂圖形的外框。

您可以將子專案放在 `<path>` `<shape>` 或元素內 `<shapetype>` 。 然後，您可以使用子項目的屬性屬性 `<path>` 來自訂圖形的外框。

例如，若要繪製下圖中所示的自訂圖形，您可以使用 `<path>` 子項目來定義圖形的外框，如下列 VML 標記法所示：

![shape1.gif (1301 個位元組) ](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   這些值 `m 8,65` 表示繪圖從 (8，65) 的點開始。
-   這些值 `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` 表示直線從目前的點開始 (8，65) ，結束于指定的點 (72，65) ，這會成為新的目前點。 新的一行會從目前的點開始 (72、65) ，並在給定的點結束，後者會成為新的目前點，依此類推，最後一個點 (60，100) 。
-   `x` 指出路徑會以從目前點開始 (60、100) 的直線來關閉，並在原始點 (8 65) 結束。
-   `e` 表示停止繪圖。

如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858391) 。

 

 