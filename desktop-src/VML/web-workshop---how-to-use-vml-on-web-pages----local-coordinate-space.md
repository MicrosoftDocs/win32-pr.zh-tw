---
title: 使用本機座標空間
description: 使用本機座標空間
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- 網路研討會，區域座標空間
- 設計網頁，區域座標空間
- Vector Markup Language (VML) 、本機座標空間
- VML (Vector Markup Language) ，區域座標空間
- 向量圖形，區域座標空間
- 本機座標空間
- VML 圖形，區域座標空間
- Vector Markup Language (VML) 、群組圖形
- VML (Vector Markup Language) 、群組圖案
- 向量圖形，群組圖形
- VML 圖形，群組
- 將圖形分組
- Vector Markup Language (VML) 、縮放圖形
- VML (Vector Markup Language) 、縮放形狀
- 向量圖形，縮放形狀
- VML 圖形，縮放比例
- 調整形狀
- Vector Markup Language (VML) ，調整大小圖形
- VML (Vector Markup Language) ，調整大小圖形
- 向量圖形，調整大小圖形
- VML 圖形，調整大小
- 調整大小圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682966"
---
# <a name="using-local-coordinate-space"></a>使用本機座標空間

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

如您所學到的，您可以指定 **寬度** 和 **高度** 樣式屬性，來定義要在其中呈現圖形或群組內容之包含方塊的大小。 在本主題中，我們將說明什麼是本機座標空間，以及如何在 VML 中使用它來調整圖形。

如果系統要求您在一段方格紙上繪製一部以二英寸為二的矩形，您要找的第一件事就是開始 (起始點) 的位置。 然後，您會找出如何將一英寸對應至方格紙的儲存格， (座標) 。

同樣地，當圖形或群組的內容呈現在網頁的包含方塊內部時，必須定義起始點和座標。 VML 提供本機座標空間，以允許每個圖形或群組定義自己的起點和座標。 如果您未指定座標空間，將會使用預設值。 根據預設，來源會從內含方塊的左上角開始。

例如，如下所示紅色橢圓形的 VML 標記法不會指定 **coordsize** 和 **coordorigin** 屬性屬性。 因此，會使用預設的本機座標空間。 Oval 的大小為100點 (寬度) 75 點 (高度) 。 您可以指定不同的寬度或高度來調整橢圓大小，如您在 [尺規圖形](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) 主題中所學到的一樣。

![oval1.gif (627 個位元組) ](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





當圖形變得更複雜時，或當您想要將數個圖案組合在一起時，您應該使用 VML 中提供的本機座標空間功能。

針對每個圖形或群組，您可以使用 **coordsize** 和 **coordorigin** 屬性屬性來定義圖形或群組的本機座標空間。 **Coordsize** 屬性會指定寬度的單位數目，以及包含方塊的高度。 **Coordorigin** 屬性會定義包含方塊左上角的座標。 所有位置相關資訊 (例如寬度、高度、左方、頂端、路徑等 ) 都會以本機座標空間中的單位表示。

例如，如下列 VML 標記法所示， `width: 100pt; height: 100pt;` 會將圖形的包含方塊大小定義為100點乘以100點。

![cord1.gif (836 個位元組) ](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` 將圖形的本機座標空間大小定義為21600單位（依21600單位）。 因此，本機座標空間中的一個單位相當於1/216 點。
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` 將圖形的外框定義為菱形形狀。 如我們所學到的，所有位置相關資訊 (例如寬度、高度、左方、頂端、路徑等 ) 都會以本機座標空間中的單位表示。 因此，中的 10800 `<path>` 表示10800單位，這相當於50點。

當您想要調整此鑽石形狀的大小時，只要指定不同的寬度或高度即可，您不需要變更中的任何值 `<path>` 。 針對這個複雜的圖形，如果您未使用本機座標空間功能，則 `<path>` 每當您想要調整其大小時，都必須變更中的每個值。

例如，您可以只指定不同的寬度或高度來調整鑽石圖形，如下列 VML 標記法所示：

![cord2.gif (1692 個位元組) ](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





您也可以在專案中使用區域座標空間， `<group>` 讓群組中的所有圖形內容都能根據相同的座標進行調整。 然後，每當您想要調整或移動一組圖形時，只要變更群組的寬度和高度，或 **coordsize** 和 **coordorigin** 設定。

例如，在下列 VML 表示中， `<v:group style='... width:200pt;height:200pt;'>` 會將群組的大小定義為200點乘以200點。

![cord3.gif (645 個位元組) ](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` 定義群組的本機座標空間大小，以1000單位乘以1000單位。 因此，本機座標空間中的1個單位相當於1/5 點。
-   `coordorigin="-500,-500"` 將內含方塊的左上角定義為 "-500，-500"。 因此，在包含方塊內的座標系統範圍是從-500 到500，沿著 X 軸，以及-500 到 y 軸的500。 換句話說，內含方塊的中心是「0，0」。
-   `<v:oval style='... width:400;height:300;'>` 將紅色橢圓的包含方塊大小定義為400單位 (寬度) 300 單位 (高度) 。 因為區域座標空間中的一個單位相當於1/5 點，所以紅色橢圓形的包含方塊大小是80點 (寬度) 由60點 (高度) 。

同樣地，綠色 roundrect 的內含方塊大小為50點 (寬度) 40 點 (高度) 。

當您想要調整紅色橢圓和綠色 roundrect 的大小時，只要變更 `<v:group style='... width:200pt;height:200pt;'>` 。 這就是-您不需要個別變更兩個圖形的大小。

例如，如果您變更 `<v:group style='... width:200pt;height:200pt;'>` 為 `<v:group style='... width:300pt;height:300pt;'>` ，圖形會變得更大，如下圖所示：

![cord4.gif (943 個位元組) ](images/cord4.gif)



您也會注意到圖形的位置不同。 這是因為圖形是從位於內含方塊中央的 "0，0" 繪製。 因為您將 [包含] 方塊放大，所以包含的方塊中央也會移動。

如果您變更 `coordorigin="-500,-500"` 為 `coordorigin="0,0"` （如下圖所示），您會注意到紅色橢圓和綠色 roundrect 都會向上移至新的位置。 這是因為 "0，0" 現在會在內含方塊的左上角找到。

![cord5.gif (648 個位元組) ](images/cord5.gif)



也請務必注意，[包含] 方塊不會建立裁剪區域。 圖形可能會在內含方塊的界限之外繪製。 [包含] 方塊只是用來將本機座標空間對應到頁面空間。

如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858382) 。

 

 