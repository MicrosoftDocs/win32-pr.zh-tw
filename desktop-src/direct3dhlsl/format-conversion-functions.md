---
title: '格式轉換函數 (HLSL 參考) '
description: 此區段包含計算和圖元著色器中所使用的格式轉換函數。
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2842236bfd0a2875576af7235aefa5dce2db8bd6
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104990867"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="69f2f-103">格式轉換函數 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="69f2f-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="69f2f-104">此區段包含計算和圖元著色器中所使用的格式轉換函數。</span><span class="sxs-lookup"><span data-stu-id="69f2f-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="69f2f-105">轉換器函式</span><span class="sxs-lookup"><span data-stu-id="69f2f-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="69f2f-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="69f2f-106">Related topics</span></span>](#related-topics)

## <a name="converter-functions"></a><span data-ttu-id="69f2f-107">轉換器函式</span><span class="sxs-lookup"><span data-stu-id="69f2f-107">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="69f2f-108">DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-108">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-109">**\_ \_ \_ FLOAT4 的 D3DX R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-109">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="69f2f-110">**D3DX \_ FLOAT4 \_ 到 \_ R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-110">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="69f2f-111">DXGI \_ 格式 \_ R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="69f2f-111">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="69f2f-112">**D3DX \_ R10G10B10A2 \_ UINT \_ 至 \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="69f2f-112">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="69f2f-113">**D3DX \_ UINT4 \_ 到 \_ R10G10B10A2 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="69f2f-113">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="69f2f-114">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM：</span><span class="sxs-lookup"><span data-stu-id="69f2f-114">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="69f2f-115">**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-115">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="69f2f-116">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-116">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="69f2f-117">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="69f2f-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="69f2f-118">**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="69f2f-118">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="69f2f-119">**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="69f2f-119">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="69f2f-120">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="69f2f-120">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="69f2f-121">DXGI \_ 格式 \_ R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="69f2f-121">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="69f2f-122">**D3DX \_ R8G8B8A8 \_ UINT \_ 至 \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="69f2f-122">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="69f2f-123">**D3DX \_ UINT4 \_ 到 \_ R8G8B8A8 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="69f2f-123">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="69f2f-124">DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-124">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-125">**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-125">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="69f2f-126">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-126">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="69f2f-127">DXGI \_ 格式 \_ R8G8B8A8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="69f2f-127">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="69f2f-128">**D3DX \_ R8G8B8A8 \_ 聖 \_ 至 \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="69f2f-128">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="69f2f-129">**D3DX \_ INT4 \_ 至 \_ R8G8B8A8 \_ 聖**</span><span class="sxs-lookup"><span data-stu-id="69f2f-129">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="69f2f-130">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-130">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-131">**\_ \_ \_ FLOAT4 的 D3DX B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-131">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="69f2f-132">**D3DX \_ FLOAT4 \_ 到 \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-132">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="69f2f-133">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="69f2f-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="69f2f-134">**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="69f2f-134">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="69f2f-135">**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="69f2f-135">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="69f2f-136">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="69f2f-136">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="69f2f-137">DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-137">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-138">**\_ \_ \_ FLOAT3 的 D3DX B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-138">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="69f2f-139">**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-139">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="69f2f-140">DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="69f2f-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="69f2f-141">**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="69f2f-141">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="69f2f-142">**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="69f2f-142">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="69f2f-143">**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="69f2f-143">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="69f2f-144">DXGI \_ 格式 \_ R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="69f2f-144">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="69f2f-145">**D3DX \_ R16G16 \_ FLOAT \_ 至 \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="69f2f-145">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="69f2f-146">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ FLOAT**</span><span class="sxs-lookup"><span data-stu-id="69f2f-146">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="69f2f-147">DXGI \_ 格式 \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-147">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-148">**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-148">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="69f2f-149">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-149">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="69f2f-150">DXGI \_ 格式 \_ R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="69f2f-150">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="69f2f-151">**D3DX \_ R16G16 \_ UINT \_ 至 \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="69f2f-151">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="69f2f-152">**D3DX \_ UINT2 \_ 到 \_ R16G16 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="69f2f-152">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="69f2f-153">DXGI \_ 格式 \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="69f2f-153">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="69f2f-154">**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-154">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="69f2f-155">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="69f2f-155">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="69f2f-156">DXGI \_ 格式 \_ R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="69f2f-156">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="69f2f-157">**D3DX \_ R16G16 \_ 聖 \_ 至 \_ INT2**</span><span class="sxs-lookup"><span data-stu-id="69f2f-157">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="69f2f-158">**D3DX \_ INT2 \_ 至 \_ R16G16 \_ 聖**</span><span class="sxs-lookup"><span data-stu-id="69f2f-158">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="69f2f-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="69f2f-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f2f-160">內嵌格式轉換參考</span><span class="sxs-lookup"><span data-stu-id="69f2f-160">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="69f2f-161">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="69f2f-161">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 




