---
description: 如果您的應用程式使用彩色的淺色地圖，通常會更實際地轉譯3D 場景。 彩色光線對應使用光線對應中的 RGB 資料，作為光線資訊。
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: " (Direct3D 9) 的色彩淺色地圖"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468173"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="71992-104"> (Direct3D 9) 的色彩淺色地圖</span><span class="sxs-lookup"><span data-stu-id="71992-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="71992-105">如果您的應用程式使用彩色的淺色地圖，通常會更實際地轉譯3D 場景。</span><span class="sxs-lookup"><span data-stu-id="71992-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="71992-106">彩色光線對應使用光線對應中的 RGB 資料，作為光線資訊。</span><span class="sxs-lookup"><span data-stu-id="71992-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="71992-107">下列 c + + 程式碼範例示範使用 RGB 色彩資料的燈光對應。</span><span class="sxs-lookup"><span data-stu-id="71992-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="71992-108">此範例會將燈光圖設定為第一個材質。</span><span class="sxs-lookup"><span data-stu-id="71992-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="71992-109">接著，它會設定第一個混合階段的狀態，以 lambert 傳入的材質資料。</span><span class="sxs-lookup"><span data-stu-id="71992-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="71992-110">它會使用第一個材質和基本的目前色彩作為 lambert 作業的引數。</span><span class="sxs-lookup"><span data-stu-id="71992-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71992-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="71992-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71992-112">使用紋理的燈光對應</span><span class="sxs-lookup"><span data-stu-id="71992-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



