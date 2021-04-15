---
description: 以光源來發亮時，遮罩表面會顯示擴散光源反射。
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: " (Direct3D 9) 的擴散燈光地圖"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467647"
---
# <a name="diffuse-light-maps-direct3d-9"></a> (Direct3D 9) 的擴散燈光地圖

以光源來發亮時，遮罩表面會顯示擴散光源反射。 擴散光線的亮度，取決於與光源的距離，以及表面法向和光源方向向量之間的角度。 光源計算模擬的擴散光源效果只會產生一般效果。

您的應用程式可透過紋理光線對應模擬更複雜的擴散光源。 若要這麼做，請將漫射光源對應新增至基網底理，如下列 c + + 程式碼範例所示。


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用紋理的燈光對應](light-mapping-with-textures.md)
</dt> </dl>

 

 



