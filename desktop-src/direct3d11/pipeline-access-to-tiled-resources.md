---
title: 磚資源的管線存取
description: 磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e4656247a1ad59d053ea9871314f9370ff00930cf24a452e363775101f58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375818"
---
# <a name="pipeline-access-to-tiled-resources"></a>磚資源的管線存取

磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。 如需支援的系結清單，請參閱 [建立資源的參數](tiled-resource-creation-parameters.md)。 複製 \* 作業也適用于並排顯示的資源。

如果有一個或多個檢視中的多個磚座標繫結相同的記憶體位置、從不同路徑讀取和寫入方式到相同記憶體，會發生不確定和非重複順序的記憶體存取。

如果從著色器的記憶體存取使用量後所有磚對應到獨特的磚，所有實作到以非磚方式具有相同的記憶體內容的表面的行為是相同的。

本節提供有關管線存取並排資源的詳細資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                              | 描述                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [非對應磚的 SRV 行為](srv-behavior-with-non-mapped-tiles.md)<br/>                            | 著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。 <br/>                                          |
| [非對應磚的 UAV 行為](uav-behavior-with-non-mapped-tiles.md)<br/>                            | 未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。 <br/>                                                            |
| [非對應磚的轉譯器行為](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | 本節說明非對應磚的轉譯器行為。<br/>                                                                                              |
| [重複對應的磚存取限制](tile-access-limitations-with-duplicate-mappings-.md)<br/> | 本節說明重複對應的磚存取限制。<br/>                                                                                        |
| [磚資源紋理取樣功能](tiled-resources-texture-sampling-features.md)<br/>              | 本節說明並排顯示的資源紋理取樣功能。<br/>                                                                                              |
| [HLSL 磚的資源曝光](hlsl-tiled-resources-exposure.md)<br/>                                      | 需要新的 Microsoft 高階著色器語言 (HLSL) 語法，以支援 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)中的磚資源。 <br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源](tiled-resources.md)
</dt> </dl>

 

