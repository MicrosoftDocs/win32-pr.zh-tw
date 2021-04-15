---
description: 使用 (Direct3D 9) 的凹凸對應
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: 使用 (Direct3D 9) 的凹凸對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467930"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="ee5bb-103">使用 (Direct3D 9) 的凹凸對應</span><span class="sxs-lookup"><span data-stu-id="ee5bb-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="ee5bb-104">偵測對凹凸對應的支援</span><span class="sxs-lookup"><span data-stu-id="ee5bb-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="ee5bb-105">如果裝置支援 D3DTOP \_ BUMPENVMAP 或 D3DTOP BUMPENVMAPLUMINANCE 材質混合作業，則該裝置可以執行「執行」對應 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="ee5bb-106">使用 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 搭配 D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP，以查看是否支援凹凸對應的格式。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="ee5bb-107">此外，應用程式也應該檢查裝置功能，以確定裝置支援適當數量的混合階段（通常至少為三個），並公開至少一個凹凸對應像素格式。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="ee5bb-108">下列程式碼範例會使用指定的準則來檢查裝置功能，以偵測目前裝置中的凹凸對應支援。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="ee5bb-109">建立凹凸地圖材質</span><span class="sxs-lookup"><span data-stu-id="ee5bb-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="ee5bb-110">您可以建立像任何其他材質一樣的凹凸地圖紋理。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="ee5bb-111">您的應用程式會驗證支援凹凸對應，並取得有效的像素格式，如偵測對凹凸對應的支援所述。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="ee5bb-112">建立介面之後，如果表面格式包含亮度，您就可以載入具有適當 delta 值和亮度的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="ee5bb-113">每個圖元元件的值會以 [ (Direct3D 9) 的放大地圖像素格式 ](bump-map-pixel-formats.md)說明。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="ee5bb-114">設定凹凸對應參數</span><span class="sxs-lookup"><span data-stu-id="ee5bb-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="ee5bb-115">當您的應用程式已建立一個 [凹凸對應] 並設定每個圖元的內容時，您可以藉由設定 [凹凸對應] 參數來準備轉譯。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="ee5bb-116">凹凸對應參數包括設定所需的材質和其混合作業，以及凹凸地圖本身的轉換和亮度控制項。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="ee5bb-117">將基底材質圖、將地圖和環境地圖材質設定為材質混合階段。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="ee5bb-118">設定每個材質階段的色彩和 Alpha 混合作業。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="ee5bb-119">設定 [凹凸地圖] 轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="ee5bb-120">視需要設定亮度比例和位移值。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="ee5bb-121">下列程式碼範例會設定三個材質 (基底材質圖、凹凸地圖和反射環境對應) 至適當的材質混合階段。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="ee5bb-122">將材質設定為其混合階段之後，下列程式碼範例會針對每個階段準備混合作業和引數。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="ee5bb-123">當設定混合作業和引數時，下列程式碼範例會藉由將 D3DTEXTURESTAGESTATETYPE 的 D3DTSS \_ BUMPENVMAPMAT00 和 D3DTSS \_ BUMPENVMAPMAT11 成員設定為 1.0 [](./d3dtexturestagestatetype.md) ，將2x2 凹凸對應矩陣設定為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="ee5bb-124">將矩陣設定為身分識別會導致系統在未修改的情況下使用增量對應中的差異值，但這不是必要條件。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="ee5bb-125">如果您將 [凹凸對應] 作業設定為包含亮度 (D3DTOP \_ BUMPENVMAPLUMINANCE) ，您必須設定亮度控制項。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="ee5bb-126">亮度控制項會設定系統在下一個階段調整材質色彩之前，如何計算亮度。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="ee5bb-127">如需詳細資訊，請參閱將 [對應公式 (Direct3D 9) ](bump-mapping-formulas.md)。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="ee5bb-128">當您的應用程式設定了凹凸對應參數之後，就可以正常轉譯，而轉譯的多邊形會收到平滑對應效果。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="ee5bb-129">請注意，上述範例會顯示為反射環境對應設定的參數。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="ee5bb-130">執行擴散燈光對應時，應用程式會將最後一個階段的材質混色作業設定為 D3DTOP \_ lambert。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="ee5bb-131">如需詳細資訊，請參閱 [ (Direct3D 9 的擴散燈光圖) ](diffuse-light-maps.md)。</span><span class="sxs-lookup"><span data-stu-id="ee5bb-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee5bb-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee5bb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee5bb-133">凹凸對應</span><span class="sxs-lookup"><span data-stu-id="ee5bb-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
