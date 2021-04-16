---
title: 使用 Fill 元素
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- 網路研討會，填滿元素
- 設計網頁，填滿元素
- Vector Markup Language (VML) 、fill 元素
- VML (Vector Markup Language) ，fill 元素
- 向量圖形、填滿元素
- fill 元素
- VML 元素，填滿
- VML 圖形，填滿元素
- Vector Markup Language (VML) 、漸層填滿
- VML (Vector Markup Language) 、漸層填滿
- 向量圖形，漸層填滿
- VML 圖形，漸層填滿
- 漸層填滿形狀
- Vector Markup Language (VML) 、模式填滿
- VML (Vector Markup Language) ，模式填滿
- 向量圖形，模式填滿
- VML 圖形，模式填滿
- 模式填滿圖形
- Vector Markup Language (VML) 、圖片填滿
- VML (Vector Markup Language) ，圖片填滿
- 向量圖形，圖片填滿
- VML 圖形，圖片填滿
- 圖片填滿的形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568419"
---
# <a name="using-the-fill-element"></a>使用 Fill 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

如您所學到的，您可以使用預先定義之圖形元素的 **fillcolor** 屬性屬性（例如，、、、、、 `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` --）來指定用來填滿圖形的色彩。 在本主題中，我們將說明如何繪製填滿更先進效果的圖形。

您可以將子專案放在 `<fill>` `<shape>` 、或或 `<shapetype>` 任何預先定義的 shape 元素內，以描述如何填滿圖形。 然後，您可以使用子項目的屬性屬性 `<fill>` 來自訂填滿效果，例如漸層 [填滿](#gradient-fill)、 [圖樣填滿](#pattern-fill)、 [圖片填滿](#picture-fill)。

本主題內容：

-   [漸層填滿](#gradient-fill)
-   [模式填滿](#pattern-fill)
-   [圖片填滿](#picture-fill)

## <a name="gradient-fill"></a>漸層填滿

若要繪製漸層填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "漸層" 或 "gradientRadial"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **method**、 **color2**、 **focus** 和 **angle**。

**範例：**

若要建立水準漸層填滿的形狀，您可以將 **type** 屬性屬性（property）設定為「漸層」（property），如下列 VML 標記法所示：

![horizontal1.gif (3055 個位元組) ](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




如果您變更圖形的 **fillcolor** 屬性屬性，圖形就會以不同的色彩填滿。 您可以指定子項目的 **color2** 屬性屬性，以新增第二個色彩 `<fill>` 。 例如，若要建立以兩種色彩填滿的形狀，您可以指定子項目的 **color2** 屬性屬性來加入第二個色彩 `<fill>` ，如下列 VML 標記法所示：

![horizontal2.gif (3127 個位元組) ](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




您可以將 **method** 屬性屬性（property）設定為 "線性" 或 "sigma" 或 "any" 或 "none"。 漸層的效果稍微不同。 此外，您也可以使用 **angle**、**focus**、**focussize** 或 **focusposition** 屬性屬性來變更漸層的效果。

**範例：**

 

若要建立垂直填滿漸層的圖形，您可以將 angle 屬性屬性設定為 angle = "-90"，如下列 VML 標記法所示：

![vertical1.gif (3836 個位元組) ](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




若要建立從對角移動的漸層填滿的形狀，您可以將 **angle** 屬性屬性設定為 angle = "-135"，如下列 VML 標記法所示：

![dialgonalup1.gif (5816 個位元組) ](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




若要建立從對角線移動漸層填滿的圖形，您可以將 **angle** 屬性屬性設定為 angle = "-45"，如下列 VML 標記法所示：

![diagonaldown1.gif (5753 個位元組) ](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




若要建立從中央填滿漸層的圖形，您可以指定 `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` ，如下列 VML 標記法所示：

![fromcenter1.gif (4598 個位元組) ](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="pattern-fill"></a>模式填滿

若要繪製模式填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "pattern"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **src** 和 **color2**。

**範例：**

若要建立填滿模式影像的圖形，您可以將 **type** 屬性屬性指定為 "pattern"，然後將 **src** 屬性屬性指向模式影像檔案的位置，如下列 VML 標記法所示：

![pattern1.gif (872 個位元組) ](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




如果您將 **src** 屬性屬性指向不同的模式檔案，您可以建立以不同模式填滿的圖形。 此外，您可以為 **fillcolor** 或 **color2** 屬性屬性指定不同的值，以變更色彩，如下列 VML 標記法所示：

![pattern2.gif (831 個位元組) ](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="picture-fill"></a>圖片填滿

若要繪製圖片填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "frame"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **src** 和 **color2**。

**範例：**

若要建立填滿圖片檔案的圖形，您可以將 **type** 屬性屬性指定為「frame」，然後將 **src** 屬性屬性（attribute）指向圖片檔的位置，如下列 VML 標記法所示：

![picture1.gif (8496 個位元組) ](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




您可以藉由將 **src** 屬性屬性指向另一個檔案，輕鬆地建立填滿不同圖片的圖形。

如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858394) 。

 

 