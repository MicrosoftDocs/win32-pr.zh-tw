---
description: Direct3D 10 的座標系統是針對圖元和材質所定義。
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: " (Direct3D 10) 協調系統"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689163"
---
# <a name="coordinate-systems-direct3d-10"></a> (Direct3D 10) 協調系統

Direct3D 10 的座標系統是針對圖元和材質所定義。



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 之間的差異：<br/> Direct3D 10 會將左上角的左上角定義為呈現目標的原點。<br/> Direct3D 9 會將左上圖元的中央定義為呈現目標的原點。<br/> |



 

-   [圖元座標系統](#pixel-coordinate-system)
    -   [Direct3D 9 的圖元座標系統](#pixel-coordinate-system-for-direct3d-9)
-   [材質座標系統](#texel-coordinate-system)
    -   [材質座標系統](#texel-coordinate-system)
-   [相關主題](#related-topics)

## <a name="pixel-coordinate-system"></a>像素座標系統

Direct3D 10 中的圖元座標系統會定義位於左上角之呈現目標的原點。 如下圖所示。 像素中心離整數位置偏移 (0.5f, 0.5f)。

![direct3d 10 中的像素座標系統圖表](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Direct3D 9 的圖元座標系統

以下是 Direct3D 9 的圖元座標系統，其定義原點或轉譯目標作為左上角圖元的中心， (0.5，0.5) 遠離左上角，如下列圖表所示。 在 Direct3D 9 中，圖元中心位於整數位置。

![direct3d 9 中圖元座標系統的圖表](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>紋素座標系統

紋素座標系統在紋理左上角的原點，如下圖所示。 這使得在 Direct3D 10) 中呈現螢幕對齊的材質很簡單 (，因為圖元座標系統與材質座標系統對齊。

![紋理座標系統的圖表](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>紋素座標系統

紋理座標以標準化或按比例調整之數字表示。每個紋理座標對應特定紋素，如下所示︰

對於標準座標︰

-   點取樣：材質 \# = floor (U \* 寬度) 
-   線性取樣：左方材質 \# = floor (U \* 寬度) ，Right 材質 \# = 左方材質 \# + 1

對於按比例調整座標︰

-   點取樣：材質 \# = floor (U) 
-   線性取樣：左方材質 \# = floor (U-0.5) ，Right 材質 \# = Left 材質 \# + 1

寬度是紋理的寬度 (以紋素為單位)。

計算紋素位置之後，就會紋理尋址環繞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




