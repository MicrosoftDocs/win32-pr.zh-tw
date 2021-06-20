---
title: 使用 Stroke 元素
description: 本文描述如何使用 VML 的 Stroke 元素，這是 Windows Internet Explorer 9 所淘汰的功能。
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- 網路研討會，筆劃元素
- 設計網頁，筆劃元素
- Vector Markup Language (VML) ，stroke 元素
- VML (Vector Markup Language) ，筆劃元素
- 向量圖形，筆劃元素
- stroke 元素
- VML 元素，筆劃
- VML 圖形，筆劃元素
- Vector Markup Language (VML) ，dashstyle 屬性屬性
- VML (Vector Markup Language) ，dashstyle 屬性屬性
- 向量圖形，dashstyle 屬性屬性
- dashstyle 屬性屬性
- Vector Markup Language (VML) 、不透明度屬性屬性
- VML (Vector Markup Language) ，不透明度屬性屬性
- 向量圖形、不透明度屬性屬性
- 不透明度屬性屬性
- Vector Markup Language (VML) ，linestyle 屬性屬性
- VML (Vector Markup Language) ，linestyle 屬性屬性
- 向量圖形，linestyle 屬性屬性
- linestyle 屬性屬性
- Vector Markup Language (VML) ，joinstyle 屬性屬性
- VML (Vector Markup Language) ，joinstyle 屬性屬性
- 向量圖形，joinstyle 屬性屬性
- joinstyle 屬性屬性
- Vector Markup Language (VML) ，filltype 屬性屬性
- VML (Vector Markup Language) ，filltype 屬性屬性
- 向量圖形，filltype 屬性屬性
- filltype 屬性屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407841"
---
# <a name="using-the-stroke-element"></a>使用 Stroke 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

使用 `<stroke>`

如您所學到的，您可以使用預先定義之圖形的 **strokecolor** 和 **strokeweight** 屬性屬性（例如，、、、、、 `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` --）來指定形狀輪廓的色彩和粗細。 在本主題中，我們將說明如何繪製具有更先進大綱的圖形。

您可以將子專案放在 `<stroke>` `<shape>` 、或或 `<shapetype>` 任何預先定義的 shape 元素內，以描述如何繪製圖案的外框。 然後，您可以使用子項目的屬性屬性（例如 [dashstyle](#dashstyle)、 [不透明度](#opacity)、 [linestyle](#linestyle)、 [joinstyle](#joinstyle)、 [filltype](#filltype) ） `<stroke>` 來自訂大綱。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="dashstyle"></a>dashstyle

您可以使用子專案的 **dashstyle** 屬性屬性 `<stroke>` ，以各種虛線樣式來繪製大綱。

**範例：**

如果您在 `<v:stroke dashstyle="solid" />` 元素內指定 `<line>` ，您可以建立實線，如下列 VML 標記法所示：

![solid.gif (96 個位元組) ](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





如果您將 **dashstyle** 屬性屬性變更為「點」，就可以建立虛線，如下列 VML 標記法所示：

![dot.gif (144 個位元組) ](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





如果您將 **dashstyle** 屬性屬性變更為 "虛線"，就可以建立虛線，如下列 VML 標記法所示：

![dash.gif (137 個位元組) ](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





如果您將 **dashstyle** 屬性屬性變更為 "點"，就可以建立具有虛線和虛線樣式的線條，如下列 VML 標記法所示：

![dashdot.gif (145 個位元組) ](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





如果您將 **dashstyle** 屬性屬性變更為 "longdash"，就可以建立具有長虛線樣式的行，如下列 VML 標記法所示：

![longdash.gif (123 個位元組) ](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





如果您將 **dashstyle** 屬性屬性變更為 "longdashdot"，則可以使用長虛線和虛線樣式來建立一行，如下列 VML 標記法所示：

![longdashdot.gif (135 個位元組) ](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





如果您在專案 `<v:stroke dashstyle="dashdot" />` 內放置 `<rect>` ，您可以建立具有虛線和點外框的矩形，如下列 VML 標記法所示：

![rect.gif (615 個位元組) ](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="opacity"></a>不透明度

您可以使用子項目的 **不透明度** 屬性屬性 `<stroke>` ，以不同的不透明度樣式來繪製外框。 **不透明度** 屬性屬性的值可以是介於0到1之間的任何數位。 依預設，它是1，表示完全不透明。

**範例：**

下列 VML 表示會建立具有完整不透明度的行：

![line1.gif (96 個位元組) ](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





如果您在專案 `<v:stroke opacity="0.5" />` 內加入 `<line>` ，您可以建立具有50% 不透明度的行，如下列 VML 標記法所示：

![line2.gif (108 個位元組) ](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="linestyle"></a>linestyle

您可以使用子項目的 **linestyle** 屬性屬性 `<stroke>` ，以各種線條樣式來繪製外框。

**範例：**

如果您在 `<v:stroke linestyle="single" />` 元素內指定 `<rect>` ，您可以使用單一大綱建立矩形，如下列 VML 標記法所示：

![single.gif (537 個位元組) ](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





如果您將 **linestyle** 屬性屬性變更為 "thinthin"，則可以使用 (1:1:1) 的大綱建立矩形，如下列 VML 標記法所示：

![thinthin.gif (642 個位元組) ](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





如果您將 **linestyle** 屬性屬性變更為 "thinthick"，則可以使用 (1:1:2) 的大綱建立矩形，如下列 VML 標記法所示：

![thinthick.gif (646 個位元組) ](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





如果您將 **linestyle** 屬性屬性變更為 "thickthin"，則可以使用 (2:1:1) 的大綱建立矩形，如下列 VML 標記法所示：

![thickthin.gif (676 個位元組) ](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





如果您將 **linestyle** 屬性屬性變更為 "thickbetweenthin"，則可以使用 (1:1:2:1:1) 的大綱建立矩形，如下列 VML 標記法所示：

![thickbthin.gif (669 個位元組) ](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="joinstyle"></a>joinstyle

您可以使用子專案的 **joinstyle** 屬性 `<stroke>` ，來定義如何將線條聯結在一起。

例如，若要建立具有圓形聯結大綱的圖形（如下圖所示），您可以在專案中指定 `<v:stroke joinstyle="round" />` `<polyline>` ，如下列 VML 標記法所示：

![round.gif (660 個位元組) ](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





如果您將 **joinstyle** 屬性屬性變更為「斜面」，則可以建立具有斜面聯結大綱的圖形，如下列 VML 標記法所示：

![bevel.gif (650 個位元組) ](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





如果您將 **joinstyle** 屬性屬性變更為「斜接角」，則可以建立具有「斜接聯結」大綱的圖形，如下列 VML 標記法所示：

![miter.gif (702 個位元組) ](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="filltype"></a>filltype

您可以使用子項目的 **filltype** 屬性屬性 `<stroke>` 來繪製具有各種填滿效果的大綱。

**範例：**

如果您在專案 `<v:stroke filltype="solid" />` 內指定 `<roundrect>` ，您可以使用實心填滿輪廓來建立圓角矩形，如下列 VML 標記法所示：

![solid.gif (701 個位元組) ](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





如果您將 **filltype** 屬性屬性變更為 "pattern"，請將 **src** 屬性屬性指向模式影像檔案的位置，並將 [ **color2** 屬性] 屬性設定為第二個模式色彩，您可以建立具有模式外框的圓角矩形，如下列 VML 標記法所示：

![pattern.gif (1055 個位元組) ](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





如果您將 [ **filltype** 屬性] 屬性變更為 [磚]，並將 **src** 屬性屬性指向影像檔的位置，您就可以建立具有並排顯示的圓角矩形，如下列 VML 標記法所示：

![tile.gif (6617 個位元組) ](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





如果您將 [ **filltype** 屬性] 屬性變更為 [frame]，並將 **src** 屬性屬性指向影像檔的位置，則可以使用圖片大綱來建立圓角矩形，如下列 VML 標記法所示：

![frame.gif (6203 個位元組) ](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858395) 。

 

 