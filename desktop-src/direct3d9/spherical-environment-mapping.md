---
description: 球形環境地圖（或球體圖）是特殊紋理，其中包含圍繞物件的場景影像，或物件周圍的光源效果。
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: " (Direct3D 9) 的球面環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be4347b71a041aaa8d7057ac2bb7523bfa235fe59f84fe1ba54c54283cd2159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746382"
---
# <a name="spherical-environment-mapping-direct3d-9"></a> (Direct3D 9) 的球面環境對應

球形環境地圖（或球體圖）是特殊紋理，其中包含圍繞物件的場景影像，或物件周圍的光源效果。 不同于三次的環境對應，球體地圖不會直接代表物件的周圍。 [環境對應 (Direct3D 9) ](environment-mapping.md)主題中的茶壺映射會顯示您可以使用球體對應達成的反映效果。 球體圖是一種2D 標記法，代表物件周圍場景的完整360度觀點，如同透過魚眼的鏡頭拍攝，如下圖所示。

![建築物內部之球體圖的圖例](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>球面環境地圖的材質座標

您為每個接收環境對應的頂點所指定的材質座標，應該將材質定址為表面曲率所建立之反射失真的函式。 應用程式必須針對每個頂點計算這些材質座標，以達成所要的效果。 產生材質座標的一個簡單且有效的方式，就是使用頂點 normal 做為輸入。 雖然有數種方法存在，但在使用球體對應執行環境對應的應用程式中，會共通下列方程式。

![球體圖的計算紋理座標方程式](images/spheremap-formula.png)

在這些公式中，您和 v 是要計算的材質座標，而 N<sub>X</sub> 和 n<sub>Y</sub> 是相機空間頂點標準的 X 和 Y 元件。 公式很簡單但有效。 如果正常的 x 元件是正數，則會將法線指向右邊，並調整 u 座標以適當地定址紋理。 同樣地，v 座標：正面 y 表示正常的點。 對每個元件中的負數值而言，相反的情況。

如果直接在相機上的點，則產生的座標應該不會失真。 這兩個座標的 + 0.5 偏差會在球體圖的中央放置零扭曲點，而 (0、0、z) 的頂點法線則會解決此點。 此公式不會考慮一般的 z 元件，但使用公式的應用程式可以略過具有正 z 元素的垂直頂點，以優化計算。 這適用于平面陰影物件，因為在相機空間中，如果正常點離相機 (正 z) ，則在呈現物件時，會挑選頂點。 針對 Gouraud 陰影的物件，一般可以從相機指向相機 (正 x) ，而包含頂點的三角形仍然可以顯示。 如果您沒有為此頂點計算您和 v，可能仍會使用臉部，導致非預期的行為。

## <a name="applying-spherical-environment-maps"></a>套用球形環境地圖

您可以使用 [**IDirect3DDevice9：： SetTexture**](/windows/desktop/api) 方法將材質設定為適當的材質階段，將環境對應套用至任何其他材質的相同方式。 將第一個參數設定為所需紋理階段的索引，並將第二個參數設定為您為環境對應建立紋理時所傳回之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的位址。 您可以視需要設定色彩和 Alpha 混合作業和引數，以達成所需的材質混合效果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[環境對應](environment-mapping.md)
</dt> </dl>

 

 
