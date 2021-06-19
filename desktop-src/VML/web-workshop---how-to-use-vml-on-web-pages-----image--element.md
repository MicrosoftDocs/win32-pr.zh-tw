---
title: 使用 Image 元素
description: 本文說明如何使用 VML 中的 Image 元素，這是 Windows Internet Explorer 9 所淘汰的功能。
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- 網路研討會，image 元素
- 設計網頁、影像元素
- Vector Markup Language (VML) 、image 元素
- VML (Vector Markup Language) ，image 元素
- 向量圖形、image 元素
- 影像元素
- VML 元素、影像
- VML 圖形、image 元素
- Vector Markup Language (VML) ，裁剪屬性屬性
- VML (Vector Markup Language) ，裁剪屬性屬性
- 向量圖形，裁剪屬性屬性
- VML 圖形，裁剪屬性屬性
- 裁剪屬性屬性
- Vector Markup Language (VML) 、增益屬性屬性
- VML (Vector Markup Language) ，增益屬性屬性
- 向量圖形，增益屬性屬性
- VML 圖形，增益屬性屬性
- 增益屬性屬性
- Vector Markup Language (VML) 、對比
- VML (Vector Markup Language) ，對比
- 向量圖形，對比
- VML 圖形，對比
- Vector Markup Language (VML) ，blacklevel 屬性屬性
- VML (Vector Markup Language) ，blacklevel 屬性屬性
- 向量圖形，blacklevel 屬性屬性
- VML 圖形，blacklevel 屬性屬性
- blacklevel 屬性屬性
- Vector Markup Language (VML) 、亮度
- VML (Vector Markup Language) 、亮度
- 向量圖形，亮度
- VML 圖形，亮度
- Vector Markup Language (VML) 、灰階屬性屬性
- VML (Vector Markup Language) 、灰階屬性屬性
- 向量圖形、灰階屬性屬性
- VML 圖形，灰階屬性屬性
- 灰階屬性屬性
- Vector Markup Language (VML) 、gamma 屬性屬性
- VML (Vector Markup Language) ，gamma 屬性屬性
- 向量圖形、gamma 屬性屬性
- VML 圖形、gamma 屬性屬性
- gamma 屬性屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407801"
---
# <a name="using-the-image-element"></a>使用 Image 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

使用 `<image>`

在本主題中，我們將說明如何使用 `<image>` 元素來顯示具有各種特殊效果的圖片。

如果您想要顯示從外部來源載入的圖片，通常會使用 `<img>` HTML 中提供的元素，然後將 **src** 屬性屬性指向影像檔案的位置。

或者，您也可以使用 `<image>` VML 中提供的元素。 當您使用專案時 `<image>` ，您只能建立一個影像檔案，然後藉由改變專案的屬性屬性，以不同的方式來顯示影像 `<image>` 。 此外，專案也會 `<image>` 提供幾個特殊效果，您只需要使用 `<img>` HTML 的元素（例如 [裁剪](#crop)、 [對比](#contrast)、 [亮度](#brightness)、 [gamma](#gamma)和 [灰階](#grayscale)）就能達到這個目的。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="crop"></a>裁切

您可以使用專案的 **cropbottom**、 **croptop**、 **cropleft** 和 **cropright** 屬性屬性， `<image>` 顯示從相同影像檔裁剪的不同圖片。

這些裁剪屬性的值代表從圖片邊緣剪下的百分比。 值可以是介於0到1之間的任何數位。 根據預設，值會設定為0，表示沒有從邊緣裁剪。 值0.1 表示從邊緣裁剪10%，值0.15 表示從邊緣裁剪15%，依此類推。

例如，若要顯示全部從相同影像檔案裁剪的五張圖片，您可以使用專案 `<image>` 並指定不同的裁剪值，如下列 VML 標記法所示：

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image1 \-2.jpg (1969 個位元組) ](images/image1-2.jpg)![image1 \-3.jpg (1148 個位元組) ](images/image1-3.jpg)![image1 \-4.jpg (1686 個位元組) ](images/image1-4.jpg)![image1 \-5.jpg (1364 個位元組) ](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





第一個影像 `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` 沒有任何裁剪值。 因此，100% 的原始影像會依80點以100點的大小顯示。

第二個影像 `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` 有一些裁剪值。 `cropbottom="0.2"` 指出將從底部裁剪20% 的圖片; `cropright="0.15"` 指出將從右邊緣裁剪15% 的圖片。 剩餘的圖片接著會以85點的大小顯示64點。

同樣地，第三個、第四個和第五個影像有一些裁剪值。 原始圖片會根據裁剪值裁剪，然後根據寬度和高度的值來顯示。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="contrast"></a>對比

您可以使用專案的 [ **增益** ] 屬性屬性 `<image>` ，顯示具有不同對比設定的各種圖片。

**增益** 屬性屬性的值可以是任何數位。 根據預設，此值為1，表示使用與原始影像相同的對比。 0值表示無對比。 數位愈大，對比愈高。

例如，若要顯示具有不同對比設定的五張圖片，可以使用 `<image>` 元素並為 **增益** 屬性屬性設定不同的值，如下列 VML 標記法所示：

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image2 \-2.jpg (270 個位元組) ](images/image2-2.jpg)![image2 \-3.jpg (1919 個位元組) ](images/image2-3.jpg)![image2 \-4.jpg (3143 個位元組) ](images/image2-4.jpg)![image2 \-5.jpg (1724 個位元組) ](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





當 **增益** 屬性屬性設定為0時，整個影像都會變成灰色，因為沒有任何對比。 當 **增益** 屬性屬性設定為3，而不是設定為0.5 時，對比會更明顯。 當 **增益** 屬性屬性設定為負數值（例如-0.4）時，就會反轉對比。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="brightness"></a>亮度

您可以使用專案的 **blacklevel** 屬性屬性 `<image>` 來顯示各種不同的亮度設定的圖片。

**Blacklevel** 屬性屬性的值可以是介於0到1之間的任何值。 根據預設，此值為0，表示保留原始影像中的亮度等級。 值1表示最高層級的亮度。

例如，若要顯示具有不同亮度設定的五張圖片，可以使用 `<image>` 元素並為 **blacklevel** 屬性屬性設定不同的值，如下列 VML 標記法所示：

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image3 \-2.jpg (2579 個位元組) ](images/image3-2.jpg)![image3 \-3.jpg (2330 個位元組) ](images/image3-3.jpg)![image3 \-4.jpg (2727 個位元組) ](images/image3-4.jpg)![image3 \-5.jpg (2435 個位元組) ](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="grayscale"></a>灰階

您可以使用專案的 [ **灰階** ] 屬性屬性 `<image>` 來顯示包含或不含灰階的圖片。

**灰階** 屬性屬性的值可以是 true 或 false。 依預設，此值會設為 false，因此影像將會以色彩顯示。 如果值設定為 true，則影像會以灰階顯示。

例如，如下圖所示，第一個影像會使用灰階屬性的預設設定 (false)  (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ) 。 因此，圖片會以色彩顯示。

第二個影像會將 [灰階] 屬性設定為 [true] (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ) 。 因此，圖片會以灰階顯示，如下列 VML 標記法所示：

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image4.jpg \-2.jpg (2138 個位元組) ](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="gamma"></a>gamma

您可以使用專案的 **gamma** 屬性屬性 `<image>` 來顯示具有不同 gamma 設定的圖片。

Gamma 屬性屬性的值可以是介於0和1之間的任何值。 依預設，此值設定為1。

例如，若要顯示三張具有不同 gamma 設定的圖片，您可以使用 `<image>` 元素並設定不同的 **gamma** 屬性屬性值，如下列 VML 標記法所示：

![image5 \-1.jpg (2714 個位元組) ](images/image5-1.jpg)![image5 \-2.jpg (2729 個位元組) ](images/image5-2.jpg)![image5 \-3.jpg (2726 個位元組) ](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858408) 。

 

 