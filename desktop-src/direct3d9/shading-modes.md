---
description: 用來呈現多邊形的陰影模式對其外觀有深遠的影響。 陰影模式會決定多邊形臉部上任何點的色彩和光源濃度。 Direct3D 支援兩種網底模式。
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: " (Direct3D 9) 的陰影模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553173"
---
# <a name="shading-modes-direct3d-9"></a> (Direct3D 9) 的陰影模式

用來呈現多邊形的陰影模式對其外觀有深遠的影響。 陰影模式會決定多邊形臉部上任何點的色彩和光源濃度。 Direct3D 支援兩種網底模式。

-   [平面網底](#flat-shading)
-   [Gouraud 網底](#gouraud-shading)

## <a name="flat-shading"></a>平面網底

在平面陰影模式中，Direct3D 轉譯管線會使用多邊形材質的色彩，將多邊形材質的色彩轉譯成整個多邊形的色彩。 以平面陰影轉譯的3D 物件如果不是共面，則會在多邊形之間呈現明顯的邊緣。

下圖顯示以平面陰影呈現的茶壺。 每個多邊形的外框都清楚可見。 平面陰影是最快速的陰影形式。

![使用平面陰影的茶壺圖例](images/flattea.png)

## <a name="gouraud-shading"></a>Gouraud 網底

當 Direct3D 使用 Gouraud 陰影轉譯多邊形時，會使用頂點 normal 和光源參數來計算每個頂點的色彩。 然後，它會將色彩插到多邊形的臉部上，並以線性方式進行插補。 例如，如果頂點1的紅色元件是0.8，而頂點2的紅色元件是0.4，則使用 Gouraud 網底模式和 RGB 色彩模型，Direct3D 照明模組會將紅色的0.6 元件指派給這些頂點之間線條中間點的圖元。

下圖將示範 Gouraud 陰影。 這個茶壺是由許多平面的三角形多邊形所組成。 不過，Gouraud 陰影會讓物件的表面顯示為曲線且平滑。

![使用 gouraud 網底的茶壺圖例](images/gourtea.png)

Gouraud 陰影也可以用來顯示具有尖邊緣的物件。

如需詳細資訊，請參閱 [ (Direct3D 9) 的臉部和頂點一般向量 ](face-and-vertex-normal-vectors.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[陰影](shading.md)
</dt> </dl>

 

 



