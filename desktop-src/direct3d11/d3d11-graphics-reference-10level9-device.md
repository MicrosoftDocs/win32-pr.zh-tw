---
title: 10Level9 ID3D11Device 方法
description: 本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 ID3D11Device 方法功能層級之間的差異。
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376197"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="84a01-103">10Level9 ID3D11Device 方法</span><span class="sxs-lookup"><span data-stu-id="84a01-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="84a01-104">本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 方法功能層級之間的差異。</span><span class="sxs-lookup"><span data-stu-id="84a01-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="84a01-105">ID3D11Device::CheckCounter</span><span class="sxs-lookup"><span data-stu-id="84a01-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="84a01-106">ID3D11Device::CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="84a01-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="84a01-107">ID3D11Device::CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="84a01-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="84a01-108">ID3D11Device::CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="84a01-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="84a01-109">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="84a01-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="84a01-110">ID3D11Device::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="84a01-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="84a01-111">ID3D11Device::CreateCounter</span><span class="sxs-lookup"><span data-stu-id="84a01-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="84a01-112">ID3D11Device::CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="84a01-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="84a01-113">ID3D11Device::CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="84a01-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="84a01-114">ID3D11Device::CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="84a01-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="84a01-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="84a01-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="84a01-116">ID3D11Device::CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="84a01-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="84a01-117">ID3D11Device::CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="84a01-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="84a01-118">ID3D11Device::CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="84a01-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="84a01-119">ID3D11Device::CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="84a01-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="84a01-120">ID3D11Device：： CreateQuery</span><span class="sxs-lookup"><span data-stu-id="84a01-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="84a01-121">ID3D11Device::CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="84a01-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="84a01-122">ID3D11Device::CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="84a01-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="84a01-123">ID3D11Device::CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="84a01-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="84a01-124">ID3D11Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="84a01-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="84a01-125">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="84a01-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="84a01-126">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="84a01-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="84a01-127">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="84a01-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="84a01-128">ID3D11Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="84a01-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="84a01-129">ID3D11Device::CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="84a01-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="84a01-130">ID3D11Device::OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="84a01-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="84a01-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="84a01-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="84a01-132">ID3D11Device::CheckCounter</span><span class="sxs-lookup"><span data-stu-id="84a01-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-133">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-133">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-134">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-136">選擇性地支援裝置相依的計數器。</span><span class="sxs-lookup"><span data-stu-id="84a01-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="84a01-137">使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device：： CheckCounterInfo</strong></a> 來判斷支援。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="84a01-140">ID3D11Device::CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="84a01-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-141">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-141">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-142">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-144">請參閱依 <a href="overviews-direct3d-11-devices-downlevel-intro.md">功能等級</a>的格式支援 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="84a01-147">ID3D11Device::CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="84a01-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-148">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-148">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-149">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-151">功能層級對 MSAA 支援沒有任何保證。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="84a01-154">ID3D11Device::CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="84a01-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="84a01-155">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-155">Feature Level</span></span>              | <span data-ttu-id="84a01-156">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a01-157">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="84a01-158">AlphaToCoverageEnable 必須是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="84a01-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="84a01-159">前四個 BlendEnables 必須有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84a01-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="84a01-160">\_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。</span><span class="sxs-lookup"><span data-stu-id="84a01-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="84a01-161">不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) </span><span class="sxs-lookup"><span data-stu-id="84a01-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="84a01-162">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="84a01-163">AlphaToCoverageEnable 必須是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="84a01-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="84a01-164">前四個 BlendEnables 必須有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84a01-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="84a01-165">前四個 RenderTargetWriteMasks 必須有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84a01-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="84a01-166">\_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。</span><span class="sxs-lookup"><span data-stu-id="84a01-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="84a01-167">不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) </span><span class="sxs-lookup"><span data-stu-id="84a01-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="84a01-168">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="84a01-169">AlphaToCoverageEnable 必須是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="84a01-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="84a01-170">前四個 BlendEnables 必須有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84a01-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="84a01-171">\_ \_ 不支援 D3D11 BLEND SRC \_ ALPHASAT。</span><span class="sxs-lookup"><span data-stu-id="84a01-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="84a01-172">不支援雙重來源色彩 blend (名稱中有 SRC1 的任何 SrcBlend 或 DestBlend) </span><span class="sxs-lookup"><span data-stu-id="84a01-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="84a01-173">D3D \_ 功能 \_ 等級 \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84a01-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="84a01-174">新增 Alpha 到涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="84a01-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="84a01-175">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="84a01-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="84a01-176">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-176">Feature Level</span></span>              | <span data-ttu-id="84a01-177">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a01-178">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="84a01-179">不支援</span><span class="sxs-lookup"><span data-stu-id="84a01-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="84a01-180">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="84a01-181">不支援</span><span class="sxs-lookup"><span data-stu-id="84a01-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="84a01-182">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="84a01-183">不支援</span><span class="sxs-lookup"><span data-stu-id="84a01-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="84a01-184">D3D \_ 功能 \_ 等級 \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84a01-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="84a01-185">*OutputMergerLogicOp* 成員已新增至 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)，以判斷 (圖元著色器輸出和轉譯目標內容之間的位邏輯運算支援邏輯作業，請參閱 [**D3D11 轉譯 \_ \_ 目標 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)) 。</span><span class="sxs-lookup"><span data-stu-id="84a01-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="84a01-186">ID3D11Device::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="84a01-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-187">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-187">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-188">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="84a01-190">緩衝區不能有呈現目標視圖。</span><span class="sxs-lookup"><span data-stu-id="84a01-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="84a01-191">緩衝區必須剛好有其中一個 D3D11_BIND_VERTEX_BUFFER、D3D11_BIND_INDEX_BUFFER 或 D3D11_BIND_CONSTANT_BUFFER。</span><span class="sxs-lookup"><span data-stu-id="84a01-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="84a01-192">只允許具有 DXGI_FORMAT_R16_UINT 格式的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a01-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="84a01-194">緩衝區不能有呈現目標視圖。</span><span class="sxs-lookup"><span data-stu-id="84a01-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="84a01-195">緩衝區必須剛好有其中一個 D3D11_BIND_VERTEX_BUFFER、D3D11_BIND_INDEX_BUFFER 或 D3D11_BIND_CONSTANT_BUFFER。</span><span class="sxs-lookup"><span data-stu-id="84a01-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="84a01-196">允許具有 DXGI_FORMAT_R16_UINT 的索引緩衝區，以及 D3D_FEATURE_LEVEL_10_0 和更高版本的 DXGI_FORMAT_R32_UINT 格式。</span><span class="sxs-lookup"><span data-stu-id="84a01-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="84a01-197">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="84a01-199">ID3D11Device::CreateCounter</span><span class="sxs-lookup"><span data-stu-id="84a01-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-200">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-200">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-201">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-203">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="84a01-206">ID3D11Device::CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="84a01-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-207">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-207">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-208">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-210">不支援雙面樣板。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="84a01-213">ID3D11Device::CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="84a01-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-214">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-214">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-215">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="84a01-217">不支援任何 9. \* 或 10. \* 功能等級。</span><span class="sxs-lookup"><span data-stu-id="84a01-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="84a01-218">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84a01-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="84a01-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="84a01-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="84a01-223">ID3D11Device::CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="84a01-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-224">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-224">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-225">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-227">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="84a01-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="84a01-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-231">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-231">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-232">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-234">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="84a01-237">ID3D11Device::CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="84a01-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-238">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-238">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-239">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="84a01-241">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84a01-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="84a01-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="84a01-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="84a01-246">ID3D11Device::CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="84a01-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="84a01-247">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-247">Feature Level</span></span>             | <span data-ttu-id="84a01-248">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a01-249">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-250">不支援 \_ \_ 每個 \_ 實例 \_ 資料的 D3D11 輸入</span><span class="sxs-lookup"><span data-stu-id="84a01-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="84a01-251">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-252">不支援 \_ \_ 每個 \_ 實例 \_ 資料的 D3D11 輸入</span><span class="sxs-lookup"><span data-stu-id="84a01-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="84a01-253">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-254">\_ \_ \_ \_ 如果任何資料流程的 \_ \_ 每個頂點 \_ \_ 資料都有 D3D11 輸入，則頂點資料流程零必須有 D3D11 輸入</span><span class="sxs-lookup"><span data-stu-id="84a01-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="84a01-255">如需可在每個功能層級上使用哪些格式的詳細資料，請參閱依 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 的格式支援圖表。</span><span class="sxs-lookup"><span data-stu-id="84a01-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="84a01-256">ID3D11Device::CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="84a01-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="84a01-257">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-257">Feature Level</span></span>             | <span data-ttu-id="84a01-258">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="84a01-259">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-260">必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="84a01-261">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-262">必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="84a01-263">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-264">必須使用 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3 或 ps \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="84a01-265">ID3D11Device::CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="84a01-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-266">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-266">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-267">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-269">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="84a01-272">ID3D11Device：： CreateQuery</span><span class="sxs-lookup"><span data-stu-id="84a01-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="84a01-273">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-273">Feature Level</span></span>             | <span data-ttu-id="84a01-274">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a01-275">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-276">支援事件查詢。</span><span class="sxs-lookup"><span data-stu-id="84a01-276">Event queries are supported.</span></span> <span data-ttu-id="84a01-277">時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。</span><span class="sxs-lookup"><span data-stu-id="84a01-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="84a01-278">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-279">支援事件和遮蔽查詢。</span><span class="sxs-lookup"><span data-stu-id="84a01-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="84a01-280">時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。</span><span class="sxs-lookup"><span data-stu-id="84a01-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="84a01-281">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-282">支援事件和遮蔽查詢。</span><span class="sxs-lookup"><span data-stu-id="84a01-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="84a01-283">時間戳記查詢是選擇性的：呼叫 [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) 以判斷支援。</span><span class="sxs-lookup"><span data-stu-id="84a01-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="84a01-284">ID3D11Device::CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="84a01-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-285">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-285">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-286">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-288">DepthClipEnable 必須是 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="84a01-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="84a01-289">DepthBiasClamp 必須設定為 0. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="84a01-292">ID3D11Device::CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="84a01-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-293">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-293">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-294">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-296">只能支援 Texture2D 物件的呈現目標視圖。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="84a01-299">ID3D11Device::CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="84a01-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-300">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-300">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-301">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="84a01-303">不支援比較篩選。</span><span class="sxs-lookup"><span data-stu-id="84a01-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="84a01-304">框線色彩必須在 [0，1] 內</span><span class="sxs-lookup"><span data-stu-id="84a01-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="84a01-305">最小」 LOD 不可為小數</span><span class="sxs-lookup"><span data-stu-id="84a01-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="84a01-306">」 LOD 上限必須是 FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="84a01-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="84a01-307">最大 anisotropy 為2。</span><span class="sxs-lookup"><span data-stu-id="84a01-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="84a01-308">不支援 D3D11_TEXTURE_ADDRESS_MIRRORONCE。</span><span class="sxs-lookup"><span data-stu-id="84a01-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="84a01-310">不支援比較篩選。</span><span class="sxs-lookup"><span data-stu-id="84a01-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="84a01-311">框線色彩必須在 [0，1] 內</span><span class="sxs-lookup"><span data-stu-id="84a01-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="84a01-312">最小」 LOD 不可為小數</span><span class="sxs-lookup"><span data-stu-id="84a01-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="84a01-313">」 LOD 上限必須是 FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="84a01-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="84a01-314">最大 anisotropy 為16。</span><span class="sxs-lookup"><span data-stu-id="84a01-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="84a01-315">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="84a01-317">ID3D11Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="84a01-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="84a01-318">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-318">Feature Level</span></span>             | <span data-ttu-id="84a01-319">MostDetailedMip plus MipLevels 必須包含最低的」 LOD (最小 subresource</span><span class="sxs-lookup"><span data-stu-id="84a01-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="84a01-320">View 必須包含所有資源陣列元素</span><span class="sxs-lookup"><span data-stu-id="84a01-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="84a01-321">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-322">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-322">Yes</span></span>                                                                          | <span data-ttu-id="84a01-323">是</span><span class="sxs-lookup"><span data-stu-id="84a01-323">yes</span></span>                                           |
| <span data-ttu-id="84a01-324">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-325">是</span><span class="sxs-lookup"><span data-stu-id="84a01-325">Yes</span></span>                                                                          | <span data-ttu-id="84a01-326">是</span><span class="sxs-lookup"><span data-stu-id="84a01-326">Yes</span></span>                                           |
| <span data-ttu-id="84a01-327">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-328">是</span><span class="sxs-lookup"><span data-stu-id="84a01-328">Yes</span></span>                                                                          | <span data-ttu-id="84a01-329">是</span><span class="sxs-lookup"><span data-stu-id="84a01-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="84a01-330">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="84a01-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-331">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-331">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-332">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-334">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="84a01-337">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="84a01-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="84a01-338">Texture2D 資源的寬度和高度會有不同于各 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)的限制。</span><span class="sxs-lookup"><span data-stu-id="84a01-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="84a01-339">在功能層級 9 \_ 3 中，以下是保證最小值的，而個別的執行可能會超出需求。</span><span class="sxs-lookup"><span data-stu-id="84a01-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="84a01-340">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-340">Feature Level</span></span>             | <span data-ttu-id="84a01-341">如果 MipCount > 1，維度必須是兩個的整數乘冪</span><span class="sxs-lookup"><span data-stu-id="84a01-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="84a01-342">支援的最小材質維度</span><span class="sxs-lookup"><span data-stu-id="84a01-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="84a01-343">Cube 紋理維度必須是2的乘冪</span><span class="sxs-lookup"><span data-stu-id="84a01-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="84a01-344">如果設定了其他 \_ TEXTURECUBE，則 ArraySize 為：</span><span class="sxs-lookup"><span data-stu-id="84a01-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="84a01-345">如果 \_ 未設定其他 TEXTURECUBE，則 ArraySize 為。</span><span class="sxs-lookup"><span data-stu-id="84a01-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="84a01-346">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-347">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-347">Yes</span></span>                                                          | <span data-ttu-id="84a01-348">2048</span><span class="sxs-lookup"><span data-stu-id="84a01-348">2048</span></span>                                | <span data-ttu-id="84a01-349">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-349">Yes</span></span>                                           | <span data-ttu-id="84a01-350">6</span><span class="sxs-lookup"><span data-stu-id="84a01-350">6</span></span>                                              | <span data-ttu-id="84a01-351">1</span><span class="sxs-lookup"><span data-stu-id="84a01-351">1</span></span>                                                  |
| <span data-ttu-id="84a01-352">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-353">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-353">Yes</span></span>                                                          | <span data-ttu-id="84a01-354">2048</span><span class="sxs-lookup"><span data-stu-id="84a01-354">2048</span></span>                                | <span data-ttu-id="84a01-355">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-355">Yes</span></span>                                           | <span data-ttu-id="84a01-356">6</span><span class="sxs-lookup"><span data-stu-id="84a01-356">6</span></span>                                              | <span data-ttu-id="84a01-357">1</span><span class="sxs-lookup"><span data-stu-id="84a01-357">1</span></span>                                                  |
| <span data-ttu-id="84a01-358">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-359">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-359">Yes</span></span>                                                          | <span data-ttu-id="84a01-360">4096</span><span class="sxs-lookup"><span data-stu-id="84a01-360">4096</span></span>                                | <span data-ttu-id="84a01-361">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-361">Yes</span></span>                                           | <span data-ttu-id="84a01-362">6</span><span class="sxs-lookup"><span data-stu-id="84a01-362">6</span></span>                                              | <span data-ttu-id="84a01-363">1</span><span class="sxs-lookup"><span data-stu-id="84a01-363">1</span></span>                                                  |



 

<span data-ttu-id="84a01-364">在上表中， **其他 \_ TEXTURECUBE** 的完整名稱是 [**D3D11 \_ 資源 \_ 其他 \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)。</span><span class="sxs-lookup"><span data-stu-id="84a01-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="84a01-365">以下是所有9個 \_ \* [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)的條件：</span><span class="sxs-lookup"><span data-stu-id="84a01-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="84a01-366">使用 D3D11 \_ usage \_ DEFAULT 或 D3D11 \_ usage \_ 不可變時，BindFlags 不可以是零。</span><span class="sxs-lookup"><span data-stu-id="84a01-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="84a01-367">使用 D3D11 系結深度樣板時 \_ \_ \_ ，MipLevels 必須是1。</span><span class="sxs-lookup"><span data-stu-id="84a01-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="84a01-368">使用 D3D11 \_ BIND \_ 著色器 \_ 資源時，SampleDesc 必須是1。</span><span class="sxs-lookup"><span data-stu-id="84a01-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="84a01-369">當目前使用 D3D11 系結時 \_ \_ ，資源無法具有 D3D11 系結 \_ \_ 著色器 \_ 資源。</span><span class="sxs-lookup"><span data-stu-id="84a01-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="84a01-370">使用 D3D10 \_ DDI \_ 資源 \_ 的其他 \_ 共用時，格式不能是 DXGI 格式 \_ \_ R8G8B8A8 \_ UNORM 或 dxgi \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。</span><span class="sxs-lookup"><span data-stu-id="84a01-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="84a01-371">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="84a01-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="84a01-372">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-372">Feature Level</span></span>             | <span data-ttu-id="84a01-373">任何軸) 的最大維度 (</span><span class="sxs-lookup"><span data-stu-id="84a01-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="84a01-374">維度必須是2的乘冪</span><span class="sxs-lookup"><span data-stu-id="84a01-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="84a01-375">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-376">256</span><span class="sxs-lookup"><span data-stu-id="84a01-376">256</span></span>                          | <span data-ttu-id="84a01-377">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-377">Yes</span></span>                             |
| <span data-ttu-id="84a01-378">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-379">512</span><span class="sxs-lookup"><span data-stu-id="84a01-379">512</span></span>                          | <span data-ttu-id="84a01-380">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-380">Yes</span></span>                             |
| <span data-ttu-id="84a01-381">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-382">512</span><span class="sxs-lookup"><span data-stu-id="84a01-382">512</span></span>                          | <span data-ttu-id="84a01-383">Yes</span><span class="sxs-lookup"><span data-stu-id="84a01-383">Yes</span></span>                             |



 

<span data-ttu-id="84a01-384">如果資源是 D3D11 \_ 使用 \_ 預設值，或 D3D11 \_ 使用方式 \_ 不變，則 BindFlags 不可以是零。</span><span class="sxs-lookup"><span data-stu-id="84a01-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="84a01-385">ID3D11Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="84a01-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-386">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-386">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-387">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="84a01-389">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="84a01-392">ID3D11Device::CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="84a01-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="84a01-393">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-393">Feature Level</span></span>             | <span data-ttu-id="84a01-394">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="84a01-395">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="84a01-396">必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="84a01-397">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="84a01-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="84a01-398">必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="84a01-399">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84a01-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="84a01-400">必須使用 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3 或 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84a01-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="84a01-401">ID3D11Device::OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="84a01-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84a01-402">功能層級</span><span class="sxs-lookup"><span data-stu-id="84a01-402">Feature Level</span></span></th>
<th><span data-ttu-id="84a01-403">行為差異</span><span class="sxs-lookup"><span data-stu-id="84a01-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84a01-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="84a01-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="84a01-405">使用 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device：： CheckFeatureSupport</strong></a> 搭配 <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> 值和 <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> 結構，以判斷是否可以共用格式。</span><span class="sxs-lookup"><span data-stu-id="84a01-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="84a01-406">如果可以共用格式， <strong>CheckFeatureSupport</strong> 會傳回 <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> 旗標。</span><span class="sxs-lookup"><span data-stu-id="84a01-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="84a01-407">使用功能層級9時，[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 和 <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> 不可共用，即使裝置指出適用于 <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>的選擇性功能支援。</span><span class="sxs-lookup"><span data-stu-id="84a01-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="84a01-408">除非10_0 或更高的功能等級，否則嘗試以 DXGI 格式建立共用資源 <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> 和 <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> 一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="84a01-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="84a01-409">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84a01-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="84a01-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="84a01-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84a01-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="84a01-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="84a01-412">相關主題</span><span class="sxs-lookup"><span data-stu-id="84a01-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84a01-413">10Level9 參考</span><span class="sxs-lookup"><span data-stu-id="84a01-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

