---
description: 深入瞭解 Alpha 混色。 Alpha 混色用來顯示具有透明或半透明圖元的影像。
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: " (Direct3D 9) 的 Alpha 混色"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081c194b9eae85dca5599f2bf9f779d1cd896c8a37641df5105bb049b4a5bc22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751578"
---
# <a name="alpha-blending-direct3d-9"></a> (Direct3D 9) 的 Alpha 混色

Alpha 混色用來顯示具有透明或半透明圖元的影像。 除了紅色、綠色和藍色色頻外，Alpha 點陣圖中的每個圖元都有一個透明元件，稱為 Alpha 色板。 Alpha 色板通常會包含與色頻一樣多的位數。 例如，8位 Alpha 色板可以代表256的透明度層級，從 0 (整個圖元都是透明) 至 255 (整個圖元都不是不透明的) 。 下列清單顯示您可以使用 Alpha 混合建立的一些特殊效果。

您可以使用或不使用 Alpha 值來定義色彩。 沒有 Alpha 的色彩是 RGB 色彩，Alpha 會儲存為 ARGB。 頂點資料、材質資料和材質資料可以用來提供物件的透明度。 框架緩衝區也可以用來產生透明度效果。

-   [ (Direct3D 9) 的頂點 Alpha ](vertex-alpha.md)
-   [ (Direct3D 9 的材質 Alpha) ](material-alpha.md)
-   [ (Direct3D 9) 的材質 Alpha ](texture-alpha.md)
-   [ (Direct3D 9) 的框架緩衝區 Alpha ](frame-buffer-alpha.md)
-   [轉譯目標 Alpha (Direct3D 9) ](render-target-alpha.md)

示範 Alpha 的範例包括：

-   [Billboarding (Direct3D 9) ](billboarding.md)
-   [ (Direct3D 9) 的雲端、冒煙和蒸氣軌跡 ](clouds--smoke--and-vapor-trails.md)
-   [)  (Direct3D 9 的火災、光暈和爆炸 ](fire--flares--and-explosions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 轉譯](direct3d-rendering.md)
</dt> </dl>

 

 



