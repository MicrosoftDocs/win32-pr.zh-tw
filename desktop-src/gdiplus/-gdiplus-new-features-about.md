---
description: 下列各節說明 Windows GDI + 中的數個新功能。
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: 新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690347"
---
# <a name="new-features"></a>新功能

下列各節說明 Windows GDI + 中的數個新功能。

-   [漸層筆刷](#gradient-brushes)
-   [基本曲線](#cardinal-splines)
-   [獨立路徑物件](#independent-path-objects)
-   [轉換和矩陣物件](#transformations-and-the-matrix-object)
-   [可擴充的區域](#scalable-regions)
-   [Alpha 混色](#alpha-blending)
-   [支援多種影像格式](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>漸層筆刷

GDI + 藉由提供線性漸層和軌跡漸層筆刷來填滿形狀、路徑和區域，來展開 Windows 圖形裝置介面 (GDI) 。 漸層筆刷也可以用來繪製線條、曲線和路徑。 當您以線性漸層筆刷填滿圖形時，色彩會在您移動整個圖形時逐漸變更。 例如，假設您在圖形的左邊緣指定藍色，在右邊緣指定綠色來建立水準漸層筆刷。 當您使用水準漸層筆刷來填滿該圖形時，當您從左邊緣移至其右邊緣時，它會逐漸從藍色變更為綠色。 同樣地，以垂直漸層筆刷填滿的形狀，會隨著您從上往下移動而改變色彩。 下圖顯示填滿水準漸層筆刷的橢圓形，以及以對角漸層筆刷填滿的區域。

![以水準漸層填滿，且由對角線漸層所組成的圖形圖例](images/aboutgdip01-art01.png)

當您使用路徑漸層筆刷填滿圖形時，您可以使用各種選項來指定當您從圖形的某個部分移至另一個部分時，色彩如何變更。 其中一個選項是使用中間色彩和界限色彩，讓圖元從形狀的中間移到外部邊緣時，從某種色彩逐漸變更為另一種色彩。 下圖顯示 (從一對貝茲曲線建立的路徑，) 填滿路徑漸層筆刷。

![類似無限大符號的圖形圖例，填滿藍色，其中一半符合邊緣的綠色](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>基本曲線

GDI + 支援在 GDI 中不支援的基線曲線。 基本曲線是一條聯結的個別曲線，形成較大的曲線。 曲線是由點陣列所指定，並傳遞該陣列中的每個點。 基線曲線會順暢地通過 (沒有任何尖角) 整個陣列中的每個點，因此比連接直線所建立的路徑更精簡。 下圖顯示兩個路徑，其中一個是連接直線，另一個建立為基線曲線。

![圖例顯示相同的五個點兩次：透過基線曲線連接後，另一個則是依線段](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>獨立路徑物件

在 GDI 中，路徑屬於裝置內容，而且路徑會在繪製時損毀。 使用 GDI + 時，繪圖是由 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件執行，而且您可以建立和維護數個與 **圖形** 物件不同的 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件。 繪圖動作不會終結 **GraphicsPath** 物件，因此您可以使用相同的 **GraphicsPath** 物件來繪製路徑數次。

## <a name="transformations-and-the-matrix-object"></a>轉換和矩陣物件

GDI + 提供 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件，這是一種功能強大的工具，可讓轉換 (旋轉、轉譯等) 輕鬆且彈性。 矩陣物件與轉換的物件搭配運作。 例如， [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件有一個 [**GraphicsPath：： Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) 方法，它會以引數的形式接收 **矩陣** 物件的位址。 單一的3×3矩陣可以儲存一個轉換或一連串的轉換。 下圖顯示兩個轉換順序之前和之後的路徑 (首次調整，然後旋轉) 。

![圖例顯示圖案的外框，然後是相同的外框，但較窄和旋轉](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>可擴充的區域

GDI + 會大幅擴充 GDI 的支援區域。 在 GDI 中，區域會儲存在裝置座標中，而唯一可套用至區域的轉換是轉譯。 GDI + 會以全局座標儲存區域，並允許區域進行任何轉換 (調整，例如可儲存在轉換矩陣中的) 。 下圖顯示三個轉換順序之前和之後的區域：調整、旋轉和轉譯。

![圖例顯示以座標軸為中心的形狀，然後是相同的形狀，但較大、旋轉和轉譯為右邊](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Alpha 混色

請注意，在上圖中，您可以看到未轉換區域 (透過已轉換的區域填滿紅色)  (填滿了影線筆刷) 。 這是由 GDI + 支援的 Alpha 混色所達成。 使用 Alpha 混色時，您可以指定填滿色彩的透明度。 透明色彩會與背景色彩混合使用，您可以使用填滿色彩的透明色彩，讓背景顯示的越多。 下圖顯示四個在不同透明度層級 (紅色) 填滿色彩的省略號。

![顯示與半透明矩形重迭的四個不同透明度橢圓形的圖例](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>支援多種影像格式

GDI + 提供 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)、 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別，可讓您以各種不同的格式載入、儲存和操作影像。 下列為支援的格式：

-   BMP
-   圖形交換格式 (GIF)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   圖示
-   WMF
-   EMF

 

 



