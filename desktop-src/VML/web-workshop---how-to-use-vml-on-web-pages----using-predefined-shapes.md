---
title: 使用預先定義的圖形
description: 本文說明如何在 VML 中使用預先定義的圖形，這項功能已在 Windows Internet Explorer 9 淘汰。
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- 網路研討會，預先定義的圖形
- 設計網頁、預先定義的圖形
- Vector Markup Language (VML) 、預先定義的圖形
- VML (Vector Markup Language) 、預先定義的圖形
- 向量圖形，預先定義的圖形
- 已預先定義的 VML 圖形
- 預先定義的圖形
- Vector Markup Language (VML) 、rect 元素
- VML (Vector Markup Language) ，rect 元素
- 向量圖形、rect 元素
- rect 元素
- VML 元素、rect
- Vector Markup Language (VML) 、roundrect 元素
- VML (Vector Markup Language) ，roundrect 元素
- 向量圖形，roundrect 元素
- roundrect 元素
- VML 元素，roundrect
- Vector Markup Language (VML) ，line 元素
- VML (Vector Markup Language) ，line 元素
- 向量圖形、線條元素
- line 元素
- VML 元素，行
- Vector Markup Language (VML) 、聚合線條元素
- VML (Vector Markup Language) 、聚合線條元素
- 向量圖形、折線元素
- 聚合線條元素
- VML 元素，折線
- Vector Markup Language (VML) 、曲線元素
- VML (Vector Markup Language) ，曲線元素
- 向量圖形、曲線元素
- 曲線元素
- VML 元素、曲線
- Vector Markup Language (VML) 、arc 元素
- VML (Vector Markup Language) ，arc 元素
- 向量圖形、弧線元素
- 弧線元素
- VML 元素、弧線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407681"
---
# <a name="using-predefined-shapes"></a>使用預先定義的圖形

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

如您所學到的，您可以使用 `<oval>` VML 的元素來建立簡單的橢圓形。 VML 提供數個其他預先定義的元素。 在本主題中，我們將說明如何使用這些元素繪製圖形。

本主題內容：

-   [矩形](#roundrect)
-   [roundrect](#roundrect)
-   [line](#polyline)
-   [折線](#polyline)
-   [曲線](#curve)
-   [弧](#arc)
-   [總結](#summary)

## <a name="rect"></a>rect

您可以使用 `<rect>` 元素來繪製矩形。 然後您可以藉由指定不同的屬性屬性來自訂矩形。

例如，您可以藉由指定 **fillcolor**= "blue" 來繪製以藍色填滿的矩形，並指定 **strokecolor**= "red" **strokeweight**= "3.5 pt" 來提供其3.5 點紅色外框，如下列 VML 標記法所示：

![rect1.gif (485 個位元組) ](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) 。  (附注： VML 規格沒有元素的書簽 `<rect>` 。 ) 

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="roundrect"></a>roundrect

您可以使用 `<roundrect>` 元素來繪製具有圓角的矩形。 然後，您可以藉由指定不同的屬性屬性來自訂圓角矩形。

例如，您可以藉由指定 **arcsize**= "0.3"、指定 **fillcolor**= "黃"，以黃色填滿矩形，然後指定 **strokecolor**= "red" **strokeweight**= "2pt"，為它提供雙點紅色外框，如下列 VML 標記法所示，繪製具有圓角的矩形：

![roundrect1.gif (622 個位元組) ](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="line"></a>line

您可以使用 `<line>` 元素來建立直線。 然後您可以藉由指定不同的屬性屬性來自訂這一行。

例如，您可以藉由指定 **from**= "20pt，20pt" to = "100pt，20pt" **來** 繪製水平線，然後藉由指定 **strokecolor**= "red" **strokeweight**= "2pt"，將其設為2點和紅色，如下列 VML 標記法所示：

![line1.gif (88 個位元組) ](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





您可以只針對 **from** 和 **to** 屬性屬性指定不同的值，以繪製垂直或對角線，如下列 VML 標記法所示：

![line2.gif (86 個位元組) ](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="polyline"></a>折線

您可以使用 `<polyline>` 元素來定義從連接的線段建立的圖形。 然後您可以藉由指定不同的屬性屬性來自訂圖形。

例如，若要繪製下圖中顯示的圖形，您可以輸入下列 VML 標記法：

![polyline1.gif (957 個位元組) ](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="curve"></a>曲線

您可以使用 `<curve>` 元素來繪製三次貝茲曲線。 然後您可以藉由指定不同的屬性屬性來自訂曲線。

例如，若要繪製如下圖所示的曲線，您可以輸入下列 VML 標記法：

![curve1.gif (992 個位元組) ](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="arc"></a>弧形

您可以使用專案 `<arc>` 來繪製定義為橢圓形區段的弧形。 弧線是由 oval 的交集所定義，以及角度所指定的開始和結束半徑向量。 角度的計算方式是使用圓形的屬性， (寬度等於高度) ，然後將 anisotropically 調整為所需的寬度和高度。

例如，您可以藉由指定 **>startangle**= "0" **endangle**= "90"，繪製從0度開始並以90度結束的弧線，如下列 VML 標記法所示：

![arc1.gif (410 個位元組) ](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





您可以藉由指定不同的 **>startangle** 和 **endangle** 值來變更弧線，如下列 VML 標記法所示：

![arc2.gif (608 個位元組) ](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 個位元組) ](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="summary"></a>總結

您可以使用 VML 預先定義的專案（例如 `<oval>` 、 `<line>` 、 `<polyline>` 、 `<curve>` 、 `<rect>` 、和）， `<roundrect>` `<arc>` 輕鬆地在網頁上繪製圖形，然後藉由只變更屬性屬性來自訂這些圖形。

 

 