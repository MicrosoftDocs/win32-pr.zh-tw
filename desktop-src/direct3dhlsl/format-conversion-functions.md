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
ms.openlocfilehash: 355fb59aa6a94e144daf05942b40d3f685daff51
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222876"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="9ae6e-103">格式轉換函數 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="9ae6e-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="9ae6e-104">此區段包含計算和圖元著色器中所使用的格式轉換函數。</span><span class="sxs-lookup"><span data-stu-id="9ae6e-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="9ae6e-105">轉換器函式</span><span class="sxs-lookup"><span data-stu-id="9ae6e-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="9ae6e-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ae6e-106">Related topics</span></span>](#related-topics)

> <span data-ttu-id="9ae6e-107">.Inl 標頭隨附于舊版 DirectX SDK，並依賴 XNAMath 來支援 c + + 支援。 D3DX_DXGIFormatConvert</span><span class="sxs-lookup"><span data-stu-id="9ae6e-107">The D3DX_DXGIFormatConvert.inl header ships in the legacy DirectX SDK and relied on XNAMath for C++ support.</span></span> <span data-ttu-id="9ae6e-108">它也包含在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中。</span><span class="sxs-lookup"><span data-stu-id="9ae6e-108">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span> <span data-ttu-id="9ae6e-109">最新版本使用 DirectXMath 進行 c + + 支援，而所有函式都定義于 **DirectX** c + + 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="9ae6e-109">The latest version uses DirectXMath for C++ support, and all functions are defined in the **DirectX** C++ namespace.</span></span>

## <a name="converter-functions"></a><span data-ttu-id="9ae6e-110">轉換器函式</span><span class="sxs-lookup"><span data-stu-id="9ae6e-110">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="9ae6e-111">DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-111">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-112">**\_ \_ \_ FLOAT4 的 D3DX R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-112">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="9ae6e-113">**D3DX \_ FLOAT4 \_ 到 \_ R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-113">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="9ae6e-114">DXGI \_ 格式 \_ R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="9ae6e-114">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="9ae6e-115">**D3DX \_ R10G10B10A2 \_ UINT \_ 至 \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-115">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="9ae6e-116">**D3DX \_ UINT4 \_ 到 \_ R10G10B10A2 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-116">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="9ae6e-117">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM：</span><span class="sxs-lookup"><span data-stu-id="9ae6e-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="9ae6e-118">**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-118">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="9ae6e-119">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-119">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="9ae6e-120">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="9ae6e-120">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="9ae6e-121">**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-121">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="9ae6e-122">**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-122">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="9ae6e-123">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-123">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="9ae6e-124">DXGI \_ 格式 \_ R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="9ae6e-124">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="9ae6e-125">**D3DX \_ R8G8B8A8 \_ UINT \_ 至 \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-125">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="9ae6e-126">**D3DX \_ UINT4 \_ 到 \_ R8G8B8A8 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-126">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="9ae6e-127">DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-127">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-128">**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-128">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="9ae6e-129">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-129">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="9ae6e-130">DXGI \_ 格式 \_ R8G8B8A8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="9ae6e-130">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="9ae6e-131">**D3DX \_ R8G8B8A8 \_ 聖 \_ 至 \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-131">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="9ae6e-132">**D3DX \_ INT4 \_ 至 \_ R8G8B8A8 \_ 聖**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-132">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="9ae6e-133">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-134">**\_ \_ \_ FLOAT4 的 D3DX B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-134">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="9ae6e-135">**D3DX \_ FLOAT4 \_ 到 \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-135">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="9ae6e-136">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="9ae6e-136">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="9ae6e-137">**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-137">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="9ae6e-138">**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-138">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="9ae6e-139">**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-139">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="9ae6e-140">DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-141">**\_ \_ \_ FLOAT3 的 D3DX B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-141">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="9ae6e-142">**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-142">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="9ae6e-143">DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="9ae6e-143">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="9ae6e-144">**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3 不 \_ 精確**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-144">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="9ae6e-145">**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-145">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="9ae6e-146">**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-146">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="9ae6e-147">DXGI \_ 格式 \_ R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="9ae6e-147">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="9ae6e-148">**D3DX \_ R16G16 \_ FLOAT \_ 至 \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-148">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="9ae6e-149">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ FLOAT**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-149">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="9ae6e-150">DXGI \_ 格式 \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-150">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-151">**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-151">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="9ae6e-152">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-152">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="9ae6e-153">DXGI \_ 格式 \_ R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="9ae6e-153">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="9ae6e-154">**D3DX \_ R16G16 \_ UINT \_ 至 \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-154">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="9ae6e-155">**D3DX \_ UINT2 \_ 到 \_ R16G16 \_ UINT**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-155">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="9ae6e-156">DXGI \_ 格式 \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="9ae6e-156">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="9ae6e-157">**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-157">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="9ae6e-158">**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-158">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="9ae6e-159">DXGI \_ 格式 \_ R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="9ae6e-159">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="9ae6e-160">**D3DX \_ R16G16 \_ 聖 \_ 至 \_ INT2**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-160">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="9ae6e-161">**D3DX \_ INT2 \_ 至 \_ R16G16 \_ 聖**</span><span class="sxs-lookup"><span data-stu-id="9ae6e-161">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="9ae6e-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ae6e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae6e-163">內嵌格式轉換參考</span><span class="sxs-lookup"><span data-stu-id="9ae6e-163">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="9ae6e-164">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="9ae6e-164">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
