---
title: 定點陣圖形
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- 網路研討會，定點陣圖形
- 設計網頁，定點陣圖形
- Vector Markup Language (VML) ，定點陣圖形
- VML (Vector Markup Language) ，定點陣圖形
- 向量圖形，定點陣圖形
- VML 圖形，定位
- 定點陣圖形
- Vector Markup Language (VML) 、靜態位置樣式
- VML (Vector Markup Language) 、靜態位置樣式
- 向量圖形，靜態位置樣式
- 靜態位置樣式
- Vector Markup Language (VML) 、相對位置樣式
- VML (Vector Markup Language) 、相對位置樣式
- 向量圖形、相對位置樣式
- 相對位置樣式
- Vector Markup Language (VML) 、絕對位置樣式
- VML (Vector Markup Language) ，絕對位置樣式
- 向量圖形，絕對位置樣式
- 絕對位置樣式
- Vector Markup Language (VML) ，z 索引位置樣式
- VML (Vector Markup Language) ，z 索引位置樣式
- 向量圖形，z-索引位置樣式
- z-索引位置樣式
- Vector Markup Language (VML) 、旋轉位置樣式
- VML (Vector Markup Language) ，旋轉位置樣式
- 向量圖形，旋轉位置樣式
- 旋轉位置樣式
- Vector Markup Language (VML) 、翻轉位置樣式
- VML (Vector Markup Language) 、翻轉位置樣式
- 向量圖形，翻轉位置樣式
- 翻轉位置樣式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023633"
---
# <a name="positioning-shapes"></a>定點陣圖形

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

您已瞭解如何使用 VML 在網頁上繪製和上色圖形。 在本主題中，您將使用 VML 在網頁上精確地放置圖形。

VML 使用方塊[模型](https://www.w3.org/TR/PR-CSS2/box.mdl)中所定義的相同語法和以[CSS2](https://www.w3.org/TR/PR-CSS2/) [呈現的視覺呈現模型](https://www.w3.org/TR/PR-CSS2/visuren.mdl)區段，來將圖形放在網頁上。 您可以使用 [ [靜態](#static)]、[ [相對](#relative)] 或 [ [絕對](#absolute) ] 來判斷基底點在網頁上的所在位置。 然後，您可以使用 [ **上** ] 和 [ **左方** ] 樣式屬性來指定基底點的位移，該基底點會放置圖形的包含方塊。

您也可以使用 [z 索引](#z-index) 來指定網頁上圖形的迭置順序。

此外，VML 還提供旋轉和[翻轉](#flip)[來旋轉或](#rotation)翻轉圖形。

本主題內容：

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [z-索引](#z-index)
-   [旋轉](#rotation)
-   [flip](#flip)
-   [總結](#summary)

## <a name="static"></a>static

預設位置樣式是靜態的，它會指示瀏覽器將圖形放置在文字流程中 (基礎點) 的目前點，並忽略 **top** 和 **left** 樣式屬性中的設定。

例如，在下列的 VML 標記法中，紅色橢圓形會緊接在「圖形開頭：」的文字後面，如下圖所示：

![shape1 \-ps.gif (2123 個位元組) ](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="relative"></a>relative

將 [位置樣式] 屬性設定為 [相對]，可讓您將包含的方塊與目前點之間的位移放 (文字流程中的基底點) 。 位移是由 **top** 和 **left** 樣式屬性中的設定所決定。 請注意，定位為相對的內含方塊會佔用文字流程中的空間。

例如，在下列的 VML 標記法中，紅色橢圓的位置是從左邊開始的20點，以及從頂端相對於文字流程中目前點的10點，如下圖所示：

![shape3.gif (2048 個位元組) ](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="absolute"></a>絕對

將 [位置樣式] 屬性設定為 [絕對]，可讓您將包含的方塊放置於左上角， (其父元素的基底點) ， (包含) 圖形的定位元素。 請注意，定位為絕對的包含方塊並不會佔用文字流程的空間。

例如，在下列 VML 標記法中，紅色的橢圓會包含在 `<body>` 整個) 網頁 (的元素內，因此，基底點位於網頁的左上角。 Oval 的 [包含] 方塊是放置在從左上角到左上角（相對於網頁左上角）的最左邊20個點，如下圖所示：

![shape2.gif (2006 個位元組) ](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="z-index"></a>圖層索引

您可以定位與另一個圖形重迭的圖形。 一般來說，HTML 程式碼中最後列出的圖形會顯示在最上方。

在 VML 中，您可以使用 **z 索引** 樣式屬性來控制迭置順序。 這個屬性的值可以是零、正整數或負整數。 具有較大 z 索引值的圖形會顯示在具有較小 z 索引值的圖形上方。 當兩個圖形都有相同的 Z 軸索引值時，HTML 程式碼中最後列出的圖形會出現在頂端。

例如，在下列 VML 標記法中，紅色橢圓形會顯示在藍色矩形的上方。 這是因為紅色橢圓形的 z-索引值大於藍色矩形的 z-索引值。

![shape4.gif (572 個位元組) ](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





如果您變更 z 索引（如下列 VML 標記法所示），紅色橢圓將會移到藍色矩形後方。

![shape5.gif (469 個位元組) ](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





如果您提供負整數，則可以使用 z 索引將圖形放置在一般文字流程後方，如下列 VML 標記法所示。

![shape6.gif (2125 個位元組) ](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="rotation"></a>旋轉

您可以使用 [ **旋轉** 樣式] 屬性來指定要讓圖形開啟其軸的度數。 正值表示順時針旋轉;負數值表示逆時針旋轉。

例如，如果您指定 **style**= ' .。。旋轉： 90 '，您可以順時針旋轉形狀90度。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="flip"></a>flip

您可以使用 [ **翻轉** 樣式] 屬性，根據下表，在其 x 或 y 軸上翻轉圖形：



| 值 | 描述                                                  |
|-------|--------------------------------------------------------------|
| x     | 翻轉 y 軸的旋轉圖形 (反轉 x 座標)  |
| y     | 翻轉 X 軸的旋轉圖形 (反轉 y 座標)  |



 

可以在 flip 屬性中指定 x 和 y。

例如，如果您輸入 **style**= ' .。。翻轉： x y '，您將會在其 x 和 y 軸上翻轉圖形。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="summary"></a>總結

根據您學到的內容，您可以依照下列步驟，精確地將圖形放在網頁上：

1.  決定您希望圖形出現在網頁上的位置，以及圖形的大小。
2.  請指定 **style**= ' position：相對 (或相對) '，以判斷基底點。
3.  使用 **左邊** 和 **頂端** 來指定基底點的位移。
4.  使用 [ **寬度** ] 和 [ **高度** ] 來指定圖形的包含方塊大小。
5.  使用 **z-索引** 來指定圖形的迭置順序。

 

 