---
description: 通常，為頂點指定的點不完全符合螢幕上的像素。 當發生此狀況，Direct3D 會套用點陣化規則來判斷哪些像素適用於指定三角形。
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: " (Direct3D 9) 的點陣化規則"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195654"
---
# <a name="rasterization-rules-direct3d-9"></a> (Direct3D 9) 的點陣化規則

通常，為頂點指定的點不完全符合螢幕上的像素。 當發生此狀況，Direct3D 會套用點陣化規則來判斷哪些像素適用於指定三角形。

-   [三角形的點陣化規則](#triangle-rasterization-rules)
-   [點與行規則](#point-and-line-rules)
-   [點 Sprite 規則](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>三角形點陣化規則

Direct3D 針對填充幾何使用左上角填充慣例。 這是針對 GDI 和 OpenGL 矩形中使用的相同慣例。 在 Direct3D 中，像素的中心是決定點。 如果中心在三角形內部，像素是三角形的一部分。 像素中心位於整數座標。

這個 Direct3D 使用的三角形點陣化規則描述，不一定適用於所有可用的硬體。 您的測試可能會發現這些規則實作的次要變化。

下圖顯示左上角位於 (0, 0) ，右下角位於 (5, 5) 的矩形。 如您所預期，這個矩形填滿 25 個像素。 矩形的寬度定義為右減左。 高度被定義為上減下。

![編號正方形分為六個數據列和資料行的圖例](images/pixmap.png)

在左上填充慣例，*上* 是指水平跨距的垂直位置，*左* 是指跨距內像素的水平位置。 邊不可為頂邊，除是是水平方向。 一般而言，大部分三角形只有左右邊。 下圖顯示頂邊和右邊。

![包含兩個三角形的編號正方形圖例](images/triedge.png)

左上角填充慣例判斷當三角形通過像素的中心時 Direct3D 會採取的動作。 下圖顯示兩個三角形，一個在 (0, 0)、(5, 0) 和 (5, 5)，另一個在 (0, 5)、(0, 0) 和 (5, 5)。 在本案例中第一個三角形取得 15 像素 (顯示黑色)，第二個僅取得 10 像素 (顯示灰色)，因為的共用邊是第一個三角形的左邊。

![顯示兩個三角形的編號方塊圖例](images/twotris.png)

如果您定義在 (0.5, 0.5) 左上角的矩形，而其右下角在 (2.5, 4.5)，此矩形中心點則在 (1.5, 2.5)。 當 Direct3D 點陣化將這個矩形切成方格時，每個像素中心均明確地位於四個三角形的每個三角形內，不需要左上角填充慣例。 下圖顯示此項。 矩形中的像素依據 Direct3D 包含像素的三角形中標示。

![顯示編號的方形，其中包含的矩形會分成四個三角形。](images/noambig.png)

如果您移動前述圖中的矩形，其左上角便會在 (1.0, 1.0)，其右下角在 (3.0, 5.0)，而其中心點在 (2.0, 3.0)，Direct3D 會套用左上角填充慣例。 此矩形中的大多數像素跨兩個或更多三角形間的邊界，如下圖所示。

![編號方塊的圖例，其中包含分成四個三角形的矩形](images/fillrule.png)

針對這兩個矩形，同一個像素會受到影響，如下圖所示。

![由前面兩個編號方塊影響的圖元圖例](images/samepix.png)

## <a name="point-and-line-rules"></a>點和行規則

點的呈現與點精靈相同，兩者均呈現為對齊螢幕的四邊形，因此遵守和多邊形著色演算相同的規則。

非平滑化行轉譯規則確實和是[GDI 行](../gdi/lines.md)一樣。

如需反鋸齒線轉譯的詳細資訊，請參閱 [**ID3DXLine**](id3dxline.md)。

## <a name="point-sprite-rules"></a>點精靈規則

點精靈和修補程式的基本類型，就好像基本類型第一次鑲嵌至三角形，而結果三角形點陣被點陣化。 如需詳細資訊，請參閱 [點 sprite (Direct3D 9) ](point-sprites.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[座標系統和幾何](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
