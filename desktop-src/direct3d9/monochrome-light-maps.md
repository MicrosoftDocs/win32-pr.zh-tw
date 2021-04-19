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
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="c490f-103"> (Direct3D 9) 的單色燈光地圖</span><span class="sxs-lookup"><span data-stu-id="c490f-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="c490f-104">某些舊版 3D 加速板不支援使用 alpha 目的地像素值的紋理混合。</span><span class="sxs-lookup"><span data-stu-id="c490f-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="c490f-105">如需詳細資訊，請參閱 [ (Direct3D 9 的 Alpha 材質混合) ](alpha-texture-blending.md) 。</span><span class="sxs-lookup"><span data-stu-id="c490f-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="c490f-106">通常這些介面卡也不支援多紋理混合。</span><span class="sxs-lookup"><span data-stu-id="c490f-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="c490f-107">如果您的應用程式正在這類的介面卡上執行，就可以使用多重紋理混合來執行單色光線對應。</span><span class="sxs-lookup"><span data-stu-id="c490f-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="c490f-108">若要執行單色光線對應，應用程式會將光源資訊儲存在光線對應紋理的 alpha 資料中。</span><span class="sxs-lookup"><span data-stu-id="c490f-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="c490f-109">此應用程式使用 Direct3D 的紋理篩選功能，從基本影像中的每個像素對應到光線圖中的對應紋素中。</span><span class="sxs-lookup"><span data-stu-id="c490f-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="c490f-110">它將來源混合因素設定為對應紋素的 alpha 值。</span><span class="sxs-lookup"><span data-stu-id="c490f-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="c490f-111">下列範例說明應用程式如何使用材質作為單色燈光圖：</span><span class="sxs-lookup"><span data-stu-id="c490f-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


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



<span data-ttu-id="c490f-112">因為顯示不支援目的地 Alpha 混合的介面卡通常不支援多重紋理混合，所以此範例會將燈光地圖設定為第一個材質（可在所有3D 加速器卡片上使用）。</span><span class="sxs-lookup"><span data-stu-id="c490f-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="c490f-113">範例程式碼會設定材質混合階段的色彩運算，以將材質資料與基本的現有色彩混合。</span><span class="sxs-lookup"><span data-stu-id="c490f-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="c490f-114">然後，它會選取第一個材質和基本的現有色彩做為輸入資料。</span><span class="sxs-lookup"><span data-stu-id="c490f-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c490f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c490f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c490f-116">使用紋理的燈光對應</span><span class="sxs-lookup"><span data-stu-id="c490f-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



