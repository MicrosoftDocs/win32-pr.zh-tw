---
description: 傳統紋理會視為單一元素紋理。
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: " (Direct3D 9) 的多元素紋理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a434d1e6c6a892c794551aa0caf34890f3def9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970676"
---
# <a name="multiple-element-textures-direct3d-9"></a><span data-ttu-id="8e36d-103"> (Direct3D 9) 的多元素紋理</span><span class="sxs-lookup"><span data-stu-id="8e36d-103">Multiple-element Textures (Direct3D 9)</span></span>

<span data-ttu-id="8e36d-104">傳統紋理會視為單一元素紋理。</span><span class="sxs-lookup"><span data-stu-id="8e36d-104">Traditional textures are considered to be single-element textures.</span></span> <span data-ttu-id="8e36d-105">多元素紋理可讓應用程式從圖元著色器同時寫入材質的多個元素。</span><span class="sxs-lookup"><span data-stu-id="8e36d-105">Multiple-element textures enable applications to write simultaneously to multiple elements of a texture from the pixel shader.</span></span> <span data-ttu-id="8e36d-106">下一次轉譯階段的結果是，應用程式可以使用一或多個元素做為單一元素材質，也就是圖元著色器的輸入。</span><span class="sxs-lookup"><span data-stu-id="8e36d-106">The result in the next rendering pass is that an application can use one or more of the elements as a single-element texture - that is, as inputs to the pixel shader.</span></span> <span data-ttu-id="8e36d-107">您可以將這些額外的元素視為中繼結果的暫存存放區，以供應用程式稍後傳遞。</span><span class="sxs-lookup"><span data-stu-id="8e36d-107">These additional elements can be thought of as a temporary store for intermediate results that will be used in a later pass by the application.</span></span>

<span data-ttu-id="8e36d-108">第一代公開這項功能的硬體具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="8e36d-108">The first generation of hardware that exposes this feature has the following restrictions:</span></span>

-   <span data-ttu-id="8e36d-109">所有多元素紋理介面都會自動設定。</span><span class="sxs-lookup"><span data-stu-id="8e36d-109">All multiple-element texture surfaces will be allocated automatically.</span></span> <span data-ttu-id="8e36d-110">這項限制的解決方式是將它視為新的介面格式類型，並交錯多個 RGBA 通道。</span><span class="sxs-lookup"><span data-stu-id="8e36d-110">This limitation is addressed by treating this as a new type of surface format with multiple RGBA channels interleaved.</span></span>
-   <span data-ttu-id="8e36d-111">多元素材質的所有元素都可以有相同的位深度。</span><span class="sxs-lookup"><span data-stu-id="8e36d-111">All elements of the multiple element texture can have the same bit depth.</span></span> <span data-ttu-id="8e36d-112">這項限制會以新表面格式的名稱表示。</span><span class="sxs-lookup"><span data-stu-id="8e36d-112">This limitation is expressed by the name of the new surface formats.</span></span>
-   <span data-ttu-id="8e36d-113">多元素材質不可為主要/可顯示的材質。</span><span class="sxs-lookup"><span data-stu-id="8e36d-113">A multiple-element texture cannot be the primary/displayable.</span></span> <span data-ttu-id="8e36d-114">換句話說，它必須是僅限畫面。</span><span class="sxs-lookup"><span data-stu-id="8e36d-114">In other words, it must be off-screen only.</span></span> <span data-ttu-id="8e36d-115">這項限制是由表面格式列舉來表示。</span><span class="sxs-lookup"><span data-stu-id="8e36d-115">This limitation is expressed by the surface-format enumeration.</span></span>
-   <span data-ttu-id="8e36d-116">不允許使用遞色、Alpha 測試、fogging、混色、點陣 op 或遮罩。</span><span class="sxs-lookup"><span data-stu-id="8e36d-116">No dithering, alpha test, fogging, blending, raster-op, or masking is allowed.</span></span> <span data-ttu-id="8e36d-117">除了 z 測試和樣板測試以外，不會完成任何的後置圖元著色器處理。</span><span class="sxs-lookup"><span data-stu-id="8e36d-117">No post-pixel shader processing is done, except the z-test and stencil test.</span></span>
-   <span data-ttu-id="8e36d-118">紋理不能是 mipmap。</span><span class="sxs-lookup"><span data-stu-id="8e36d-118">The texture cannot be a mipmap.</span></span> <span data-ttu-id="8e36d-119">建立 mip 鏈將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8e36d-119">Creation of the mip chain will fail.</span></span>
-   <span data-ttu-id="8e36d-120">相同的專案無法同時設定為轉譯目標的材質。</span><span class="sxs-lookup"><span data-stu-id="8e36d-120">The same element cannot be set as a texture at the same time it is a render target.</span></span> <span data-ttu-id="8e36d-121">不過，相同多元素紋理介面的不同元素可以同時是材質和轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="8e36d-121">However, different elements of the same multiple-element texture surface can simultaneously be textures and render targets.</span></span>
-   <span data-ttu-id="8e36d-122">不支援消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="8e36d-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="8e36d-123">無法篩選多個元素的材質介面（作為材質使用時）。</span><span class="sxs-lookup"><span data-stu-id="8e36d-123">Multiple-element texture surfaces, when used as a texture, cannot be filtered.</span></span> <span data-ttu-id="8e36d-124">這項限制可使用 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8e36d-124">This limitation can be verified using [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>
-   <span data-ttu-id="8e36d-125">無法鎖定多元素紋理表面。</span><span class="sxs-lookup"><span data-stu-id="8e36d-125">Multiple-element texture surfaces cannot be locked.</span></span>
-   <span data-ttu-id="8e36d-126">您可以將每個階段指派給不同的階段，以同時使用一個以上的多重元素紋理介面，就像一般材質一樣。</span><span class="sxs-lookup"><span data-stu-id="8e36d-126">More than one multiple-element texture surface can be used simultaneously by assigning each to various stages, just as with normal textures.</span></span>
-   <span data-ttu-id="8e36d-127">多元素紋理介面支援從2.2 到1.0 的轉換轉換，就像使用其他材質格式一樣。</span><span class="sxs-lookup"><span data-stu-id="8e36d-127">Multiple-element texture surfaces support conversion of gamma from 2.2 to 1.0 conversion on a read operation, just as with other texture formats.</span></span>
-   <span data-ttu-id="8e36d-128">部分的執行不會將輸出寫入遮罩套用 (D3DRS \_ COLORWRITEENABLE) 。</span><span class="sxs-lookup"><span data-stu-id="8e36d-128">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="8e36d-129">可以有獨立色彩寫入遮罩的人員。</span><span class="sxs-lookup"><span data-stu-id="8e36d-129">Those that can have independent color write masks.</span></span> <span data-ttu-id="8e36d-130">這是使用新的功能位來表示。</span><span class="sxs-lookup"><span data-stu-id="8e36d-130">This is expressed using a new capability bit.</span></span> <span data-ttu-id="8e36d-131">可用的獨立色彩寫入遮罩數目會等於裝置所能使用的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="8e36d-131">The number of independent color write masks available will be equal to the maximum number of elements of which the device is capable.</span></span>
-   <span data-ttu-id="8e36d-132">[**清除**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) [清除已設定為轉譯目標的多重元素材質的所有元素]。</span><span class="sxs-lookup"><span data-stu-id="8e36d-132">[**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) clears all elements of the multiple-element texture which is set as the render target.</span></span>

<span data-ttu-id="8e36d-133">使用多元素紋理時，會遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8e36d-133">The usage of multiple-element textures follows these steps:</span></span>

1.  <span data-ttu-id="8e36d-134">應用程式會藉由檢查多元素材質格式的可用性，來探索這項功能的支援。</span><span class="sxs-lookup"><span data-stu-id="8e36d-134">Applications discover support for this feature by checking for the availability of multiple-element texture formats.</span></span>
2.  <span data-ttu-id="8e36d-135">應用程式會藉由呼叫 [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)來建立這些表面。</span><span class="sxs-lookup"><span data-stu-id="8e36d-135">The application creates these surfaces by calling [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).</span></span>
3.  <span data-ttu-id="8e36d-136">應用程式會使用 [**SetRenderTarget**](/windows/desktop/api) 呼叫將介面設定為呈現目標。</span><span class="sxs-lookup"><span data-stu-id="8e36d-136">The application sets the surface as a render target using the [**SetRenderTarget**](/windows/desktop/api) call.</span></span> <span data-ttu-id="8e36d-137">圖元著色器使用 [mov-ps](../direct3dhlsl/mov---ps.md) 指令提供輸出給表面。</span><span class="sxs-lookup"><span data-stu-id="8e36d-137">The pixel shader provides output to the surfaces using the [mov - ps](../direct3dhlsl/mov---ps.md) instruction.</span></span>
4.  <span data-ttu-id="8e36d-138">呼叫 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) ，以將多元素紋理介面設定至特定階段。</span><span class="sxs-lookup"><span data-stu-id="8e36d-138">[**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) is called to set a multiple-element texture surface to a particular stage.</span></span> <span data-ttu-id="8e36d-139">如同其他材質一樣，相同的表面也可同時設定為多個階段。</span><span class="sxs-lookup"><span data-stu-id="8e36d-139">As with other textures, the same surface is allowed to be set to multiple stages at once.</span></span>
5.  <span data-ttu-id="8e36d-140">呼叫 [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)時，會將 D3DSAMP \_ ELEMENTINDEX 設定為多元素紋理中取樣器範例的適當元素編號。</span><span class="sxs-lookup"><span data-stu-id="8e36d-140">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) is called to set D3DSAMP\_ELEMENTINDEX to the appropriate element number in the multiple-element texture from which the sampler samples.</span></span> <span data-ttu-id="8e36d-141">此狀態的預設值為0，表示非多重元素紋理將可運作。</span><span class="sxs-lookup"><span data-stu-id="8e36d-141">Default value for this state is 0, which means non-multiple-element textures will work.</span></span> <span data-ttu-id="8e36d-142">將此狀態設定為不適當的數位會導致未定義的行為-如果多重元素材質只有兩個元素寬，但是會要求取樣器從第四個元素取樣，例如。</span><span class="sxs-lookup"><span data-stu-id="8e36d-142">Setting this state to an inappropriate number results in an undefined behavior - if the multiple-element texture is only two elements wide but the sampler is asked to sample from the fourth element, for example.</span></span>

## <a name="api-support"></a><span data-ttu-id="8e36d-143">API 支援</span><span class="sxs-lookup"><span data-stu-id="8e36d-143">API Support</span></span>

<span data-ttu-id="8e36d-144">以下是支援多元素紋理的 API 元素摘要：</span><span class="sxs-lookup"><span data-stu-id="8e36d-144">The following is a summary of the API elements that support multiple-element textures:</span></span>

-   <span data-ttu-id="8e36d-145">[D3DFMT \_ MULTI2 \_ ARGB8](d3dformat.md)表面格式表示格式的交錯性質。</span><span class="sxs-lookup"><span data-stu-id="8e36d-145">The [D3DFMT\_MULTI2\_ARGB8](d3dformat.md) surface format expresses the interleaved nature of the format.</span></span>
-   <span data-ttu-id="8e36d-146">D3DSAMP \_ ELEMENTINDEX 取樣器狀態會指出要使用的元素索引。</span><span class="sxs-lookup"><span data-stu-id="8e36d-146">The D3DSAMP\_ELEMENTINDEX sampler state indicates which element index to use.</span></span>
-   <span data-ttu-id="8e36d-147">下列轉譯狀態支援多元素紋理：</span><span class="sxs-lookup"><span data-stu-id="8e36d-147">The following render states support multiple-element textures:</span></span>

    -   <span data-ttu-id="8e36d-148">D3DRS \_ COLORWRITEENABLE1</span><span class="sxs-lookup"><span data-stu-id="8e36d-148">D3DRS\_COLORWRITEENABLE1</span></span>
    -   <span data-ttu-id="8e36d-149">D3DRS \_ COLORWRITEENABLE2</span><span class="sxs-lookup"><span data-stu-id="8e36d-149">D3DRS\_COLORWRITEENABLE2</span></span>
    -   <span data-ttu-id="8e36d-150">D3DRS \_ COLORWRITEENABLE3</span><span class="sxs-lookup"><span data-stu-id="8e36d-150">D3DRS\_COLORWRITEENABLE3</span></span>

    <span data-ttu-id="8e36d-151">D3DRS \_ COLORWRITEENABLE 適用于呈現目標 (或元素) 零。</span><span class="sxs-lookup"><span data-stu-id="8e36d-151">D3DRS\_COLORWRITEENABLE applies to render target (or element) zero.</span></span>

-   <span data-ttu-id="8e36d-152">[D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md)旗標表示裝置支援多個元素紋理或多個呈現目標的獨立寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="8e36d-152">The [D3DPMISCCAPS\_INDEPENDENTWRITEMASKS](d3dpmisccaps.md) flag indicates that the device supports independent write masks for multiple element textures or multiple render targets.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e36d-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e36d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e36d-154">圖元管線</span><span class="sxs-lookup"><span data-stu-id="8e36d-154">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
