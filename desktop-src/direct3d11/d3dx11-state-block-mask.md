---
title: 'D3DX11_STATE_BLOCK_MASK 結構 (D3dx11effect .h) '
description: 指出裝置狀態。
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323120"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="a8b5b-104">D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩結構</span><span class="sxs-lookup"><span data-stu-id="a8b5b-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="a8b5b-105">指出裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b5b-106">語法</span><span class="sxs-lookup"><span data-stu-id="a8b5b-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="a8b5b-107">成員</span><span class="sxs-lookup"><span data-stu-id="a8b5b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8b5b-108">**與**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-109">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-110">指出是否要儲存頂點著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-111">**VSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-112">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-113">頂點著色器取樣器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="a8b5b-114">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-115">**VSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-116">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-117">頂點著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="a8b5b-118">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-119">**VSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-120">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-121">頂點著色器常數緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-122">陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-123">**VSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-124">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-125">頂點著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="a8b5b-126">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-127">**房 協**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-128">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-129">指出是否要儲存輪廓著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-130">**HSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-131">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-132">輪廓著色器取樣器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="a8b5b-133">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-134">**HSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-135">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-136">輪廓著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-136">Array of hull-shader resources.</span></span> <span data-ttu-id="a8b5b-137">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-138">**HSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-139">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-140">輪廓的陣列-著色器常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-141">陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-142">**HSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-143">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-144">輪廓著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="a8b5b-145">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-146">**Ds**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-147">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-148">指出是否要儲存網域著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-149">**DSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-150">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-151">網域著色器取樣器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="a8b5b-152">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-153">**DSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-154">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-155">網域著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-155">Array of domain-shader resources.</span></span> <span data-ttu-id="a8b5b-156">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-157">**DSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-158">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-159">網域著色器常數緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-160">陣列是多位元組的位元遮罩，其中每個位都代表一個緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-161">**DSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-162">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-163">網域著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="a8b5b-164">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-166">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-167">指出是否要儲存幾何著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-168">**GSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-169">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-170">幾何的陣列-著色器取樣器。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="a8b5b-171">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-172">**GSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-173">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-174">Geometry 的陣列-著色器資源。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="a8b5b-175">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-176">**GSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-177">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-178">Geometry 的陣列-著色器常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-179">陣列是多位元組的位元遮罩，其中每個位都代表一個緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-180">**GSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-181">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-182">Geometry-著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="a8b5b-183">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-184">**Ps**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-185">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-186">指出是否要儲存圖元著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-187">**PSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-188">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-189">圖元著色器取樣器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="a8b5b-190">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-191">**PSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-192">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-193">圖元著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="a8b5b-194">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-195">**PSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-196">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-197">圖元著色器常數緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-198">陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-199">**PSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-200">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-201">圖元著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="a8b5b-202">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-203">**PSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-204">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-205">布林值，指出是否要儲存圖元著色器的未排序存取視圖。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-207">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-208">指出是否要儲存計算著色器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-209">**CSSamplers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-210">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-211">計算著色器取樣器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="a8b5b-212">陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-213">**CSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-214">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-215">計算著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-215">Array of compute-shader resources.</span></span> <span data-ttu-id="a8b5b-216">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-217">**CSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-218">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-219">計算著色器常數緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="a8b5b-220">陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-221">**CSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-222">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-223">計算著色器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="a8b5b-224">陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-225">**CSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-226">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-227">布林值，指出是否要儲存計算著色器的未排序存取視圖。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-228">**IAVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-229">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-230">頂點緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-230">Array of vertex buffers.</span></span> <span data-ttu-id="a8b5b-231">陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-232">**IAIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-233">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-234">指出是否要儲存索引緩衝區狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-235">**IAInputLayout**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-236">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-237">指出是否要儲存輸入配置狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-238">**IAPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-239">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-240">指出是否要儲存基本拓撲狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-241">**OMRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-242">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-243">指出是否要儲存轉譯目標狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-244">**OMDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-245">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-246">指出是否要儲存深度樣板狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-247">**OMBlendState**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-248">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-249">指出是否要儲存 blend 狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-250">**RSViewports**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-251">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-252">布林值，指出是否要儲存區的狀態。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-253">**RSScissorRects**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-254">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-255">指出是否要儲存剪式矩形狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-256">**RSRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-257">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-258">指出是否要儲存轉譯器狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-259">**SOBuffers**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-260">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-261">指出是否要儲存資料流程輸出緩衝區狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5b-262">**預測**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="a8b5b-263">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8b5b-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8b5b-264">指出是否要儲存 predication 狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8b5b-265">備註</span><span class="sxs-lookup"><span data-stu-id="a8b5b-265">Remarks</span></span>

<span data-ttu-id="a8b5b-266">狀態欄塊遮罩表示裝置會指出通過或技術有所變更。</span><span class="sxs-lookup"><span data-stu-id="a8b5b-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b5b-267">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8b5b-267">Requirements</span></span>



| <span data-ttu-id="a8b5b-268">需求</span><span class="sxs-lookup"><span data-stu-id="a8b5b-268">Requirement</span></span> | <span data-ttu-id="a8b5b-269">值</span><span class="sxs-lookup"><span data-stu-id="a8b5b-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b5b-270">標頭</span><span class="sxs-lookup"><span data-stu-id="a8b5b-270">Header</span></span><br/> | <dl> <span data-ttu-id="a8b5b-271"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b5b-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b5b-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8b5b-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b5b-273">效果11結構</span><span class="sxs-lookup"><span data-stu-id="a8b5b-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

