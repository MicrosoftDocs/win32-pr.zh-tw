---
description: 某些舊版 3D 加速板不支援使用 alpha 目的地像素值的紋理混合。
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: " (Direct3D 9) 的單色燈光地圖"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971096"
---
# <a name="monochrome-light-maps-direct3d-9"></a> (Direct3D 9) 的單色燈光地圖

某些舊版 3D 加速板不支援使用 alpha 目的地像素值的紋理混合。 如需詳細資訊，請參閱 [ (Direct3D 9 的 Alpha 材質混合) ](alpha-texture-blending.md) 。 通常這些介面卡也不支援多紋理混合。 如果您的應用程式正在這類的介面卡上執行，就可以使用多重紋理混合來執行單色光線對應。

若要執行單色光線對應，應用程式會將光源資訊儲存在光線對應紋理的 alpha 資料中。 此應用程式使用 Direct3D 的紋理篩選功能，從基本影像中的每個像素對應到光線圖中的對應紋素中。 它將來源混合因素設定為對應紋素的 alpha 值。

下列範例說明應用程式如何使用材質作為單色燈光圖：


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



因為顯示不支援目的地 Alpha 混合的介面卡通常不支援多重紋理混合，所以此範例會將燈光地圖設定為第一個材質（可在所有3D 加速器卡片上使用）。 範例程式碼會設定材質混合階段的色彩運算，以將材質資料與基本的現有色彩混合。 然後，它會選取第一個材質和基本的現有色彩做為輸入資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用紋理的燈光對應](light-mapping-with-textures.md)
</dt> </dl>

 

 



