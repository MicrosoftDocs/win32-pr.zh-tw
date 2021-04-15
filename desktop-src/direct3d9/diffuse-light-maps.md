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
# <a name="diffuse-light-maps-direct3d-9"></a><span data-ttu-id="bb909-103"> (Direct3D 9) 的擴散燈光地圖</span><span class="sxs-lookup"><span data-stu-id="bb909-103">Diffuse Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="bb909-104">以光源來發亮時，遮罩表面會顯示擴散光源反射。</span><span class="sxs-lookup"><span data-stu-id="bb909-104">When illuminated by a light source, matte surfaces display diffuse light reflection.</span></span> <span data-ttu-id="bb909-105">擴散光線的亮度，取決於與光源的距離，以及表面法向和光源方向向量之間的角度。</span><span class="sxs-lookup"><span data-stu-id="bb909-105">The brightness of diffuse light depends on the distance from the light source and the angle between the surface normal and the light source direction vector.</span></span> <span data-ttu-id="bb909-106">光源計算模擬的擴散光源效果只會產生一般效果。</span><span class="sxs-lookup"><span data-stu-id="bb909-106">The diffuse lighting effects simulated by lighting calculations produce only general effects.</span></span>

<span data-ttu-id="bb909-107">您的應用程式可透過紋理光線對應模擬更複雜的擴散光源。</span><span class="sxs-lookup"><span data-stu-id="bb909-107">Your application can simulate more complex diffuse lighting with texture light maps.</span></span> <span data-ttu-id="bb909-108">若要這麼做，請將漫射光源對應新增至基網底理，如下列 c + + 程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="bb909-108">Do this by adding the diffuse light map to the base texture, as shown in the following C++ code example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bb909-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb909-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb909-110">使用紋理的燈光對應</span><span class="sxs-lookup"><span data-stu-id="bb909-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



