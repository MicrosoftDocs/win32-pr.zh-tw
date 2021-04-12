---
description: 真實世界中的燈光包含一個非常高的動態範圍 (HDR) 的亮度值。
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: " (Direct3D 9) 的 HDR 照明"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187370"
---
# <a name="hdr-lighting-direct3d-9"></a> (Direct3D 9) 的 HDR 照明

真實世界中的燈光包含一個非常高的動態範圍 (HDR) 的亮度值。 真實世界有大約10個動態範圍 (DR) 的亮度值分散到亮度的範圍之間。 另一方面，電腦螢幕的顯示範圍 (或亮度值範圍) ：大約兩個動態範圍的順序。 產生 HDR 轉譯影像的挑戰，是要將真實世界的 HDR 值對應到電腦螢幕的有限範圍內。

色調對應是 DirectX 用來將 HDR 資訊對應到更有限範圍的技術。 套用至 CGI 轉譯的色調對應可大幅改善所呈現的光源詳細資料量，讓您可以在最深的區域中看到詳細資料，以及在外觀較亮的區域中提供對比。 產生的場景會呈現更多可見的光源詳細資料。

[HDRLighting 範例](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) 是示範 HDR 照明的 SDK 範例。

## <a name="tone-mapping"></a>語氣對應

色調對應通常會模擬監視的 DR 無法造成的光學現象。 這種情況的範例包括光暈或綻放 (，這些屬性大多是鏡頭) 的屬性，也就是在一般情況下，人類眼中發生的藍色變換，以及生物化學眼睛結果的其他採用原音。 如果顯示器的 DR 夠大，則不需要語氣對應，除了提供美術效果或某些相機鏡頭或收費裝置的屬性 (CCD) 。

色調對應會將場景中的亮度值範圍分割成一組區域。 每個區域都包含一個範圍的亮度值。

HDR 使用下列詞彙：

-   區域範圍的亮度值
-   場景的中間灰色-中間亮度區域
-   動態範圍-最高場景亮度至最低場景亮度的比率
-   場景光源的按鍵-主觀測量：這會因淺色而異至深色

若要從 RGB 值計算亮度，請使用：


```
L = 0.27R + 0.67G + 0.06B;
```



記錄平均的亮度是場景索引鍵的有用近似值。 一般方程式如下所示：

L<sub>w</sub> = exp \[ 1/N ( sum \[ Log ( delta + L<sub>w</sub> ( x，y ) ) \] ) \]

其中：

-   L<sub>w</sub> -記錄-平均亮度
-   N-影像中的圖元數目
-   delta-避免黑色圖元問題的小型因素
-   L<sub>w</sub> ( x，y ) -圖元 ( x，y ) 的世界空間亮度

若要將此對應至中間的值，以下是明亮比例調整運算子：

L ( x，y ) = a \* L<sub>w</sub> ( x，y ) /l<sub>w</sub>

其中：

-   L ( x，y ) 縮放亮度（圖元） ( x，y ) 
-   套用調整之後的影像索引鍵值

最後，以下是可壓縮高 luminances 的簡單音調對應運算子：

L<sub>d</sub> ( x、y ) = L ( x、y ) / ( 1 + L ( x、y ) ) 

其中：

-   L<sub>d</sub> ( x、y ) 壓縮和縮放亮度（圖元） ( x，y ) 
-   套用調整之後的影像索引鍵值

此運算子會將高 luminances 的級別調整為 1/L，並將低 luminances 比例調整為1。 如需詳細資訊，請參閱下列文章。

Reinhard、Erik、Mike Stark、Peter Shirley 和 James Ferwerda。 「[數位影像的攝影語氣複製品](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf)」。 關於圖形 (TOG) 、電腦圖形和互動式技術的29年會議記錄， (SIGGRAPH) ，267-276。 紐約，紐約州：按下，2002。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 



