---
title: 'ld_uav_typed (sm5-asm) '
description: 從具類型的未排序存取視圖中隨機存取專案的讀取 (UAV) 。
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313682"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="1a665-103">ld \_ uav \_ 類型 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="1a665-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="1a665-104">從具類型的未排序存取視圖中隨機存取專案的讀取 (UAV) 。</span><span class="sxs-lookup"><span data-stu-id="1a665-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="1a665-105">ld \_ uav 具 \_ 類型的 dst0 \[ . mask \] 、srcAddress \[ . swizzle \] 、srcUAV \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1a665-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="1a665-106">項目</span><span class="sxs-lookup"><span data-stu-id="1a665-106">Item</span></span>                                                                                                           | <span data-ttu-id="1a665-107">描述</span><span class="sxs-lookup"><span data-stu-id="1a665-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1a665-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="1a665-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="1a665-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="1a665-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1a665-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="1a665-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="1a665-111">\[中的 \] 指定要讀取的位址。</span><span class="sxs-lookup"><span data-stu-id="1a665-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="1a665-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span><span class="sxs-lookup"><span data-stu-id="1a665-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="1a665-113">\[\]來源中的讀取來源。</span><span class="sxs-lookup"><span data-stu-id="1a665-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1a665-114">備註</span><span class="sxs-lookup"><span data-stu-id="1a665-114">Remarks</span></span>

<span data-ttu-id="1a665-115">此指令會從 *srcAddress* 中不帶正負號的整數位址，執行 *srcUAV* 讀取的4元件元素，並根據格式轉換為每個元件的32位，然後寫入著色器中的 *dst0* 。</span><span class="sxs-lookup"><span data-stu-id="1a665-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="1a665-116">*srcUAV* 是 UAV (u \#) 宣告為具類型。</span><span class="sxs-lookup"><span data-stu-id="1a665-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="1a665-117">不過，系結資源的類型必須是 R32 \_ UINT/聖/FLOAT。</span><span class="sxs-lookup"><span data-stu-id="1a665-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="1a665-118">從位址取得的32位不帶正負號整陣列件的數目，取決於在 *srcUAV* 中宣告之資源的維度。</span><span class="sxs-lookup"><span data-stu-id="1a665-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="1a665-119">定址與 [ld](ld--sm4---asm-.md) 指令相同。</span><span class="sxs-lookup"><span data-stu-id="1a665-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="1a665-120">超出範圍定址與 **ld** 指令相同。</span><span class="sxs-lookup"><span data-stu-id="1a665-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="1a665-121">此指令的行為與 **ld** 指令相同（如果呼叫的是 **ld dst0 \[ \] ，srcAddress \[ . swizzle \] ，srcUAV \[ . swizzle \]** ）。</span><span class="sxs-lookup"><span data-stu-id="1a665-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="1a665-122">它無效且未定義，無法在未宣告為具類型的 UAV 上使用這個指令。</span><span class="sxs-lookup"><span data-stu-id="1a665-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="1a665-123">在結構化或無別 UAV 上執行這項操作，是不正確。</span><span class="sxs-lookup"><span data-stu-id="1a665-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="1a665-124">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1a665-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1a665-125">頂點</span><span class="sxs-lookup"><span data-stu-id="1a665-125">Vertex</span></span> | <span data-ttu-id="1a665-126">船體</span><span class="sxs-lookup"><span data-stu-id="1a665-126">Hull</span></span> | <span data-ttu-id="1a665-127">網域</span><span class="sxs-lookup"><span data-stu-id="1a665-127">Domain</span></span> | <span data-ttu-id="1a665-128">幾何</span><span class="sxs-lookup"><span data-stu-id="1a665-128">Geometry</span></span> | <span data-ttu-id="1a665-129">像素</span><span class="sxs-lookup"><span data-stu-id="1a665-129">Pixel</span></span> | <span data-ttu-id="1a665-130">計算</span><span class="sxs-lookup"><span data-stu-id="1a665-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1a665-131">X</span><span class="sxs-lookup"><span data-stu-id="1a665-131">X</span></span>     | <span data-ttu-id="1a665-132">X</span><span class="sxs-lookup"><span data-stu-id="1a665-132">X</span></span>       |



 

<span data-ttu-id="1a665-133">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="1a665-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="1a665-134">頂點</span><span class="sxs-lookup"><span data-stu-id="1a665-134">Vertex</span></span> | <span data-ttu-id="1a665-135">船體</span><span class="sxs-lookup"><span data-stu-id="1a665-135">Hull</span></span> | <span data-ttu-id="1a665-136">網域</span><span class="sxs-lookup"><span data-stu-id="1a665-136">Domain</span></span> | <span data-ttu-id="1a665-137">幾何</span><span class="sxs-lookup"><span data-stu-id="1a665-137">Geometry</span></span> | <span data-ttu-id="1a665-138">像素</span><span class="sxs-lookup"><span data-stu-id="1a665-138">Pixel</span></span> | <span data-ttu-id="1a665-139">計算</span><span class="sxs-lookup"><span data-stu-id="1a665-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1a665-140">X</span><span class="sxs-lookup"><span data-stu-id="1a665-140">X</span></span>      | <span data-ttu-id="1a665-141">X</span><span class="sxs-lookup"><span data-stu-id="1a665-141">X</span></span>    | <span data-ttu-id="1a665-142">X</span><span class="sxs-lookup"><span data-stu-id="1a665-142">X</span></span>      | <span data-ttu-id="1a665-143">X</span><span class="sxs-lookup"><span data-stu-id="1a665-143">X</span></span>        | <span data-ttu-id="1a665-144">X</span><span class="sxs-lookup"><span data-stu-id="1a665-144">X</span></span>     | <span data-ttu-id="1a665-145">X</span><span class="sxs-lookup"><span data-stu-id="1a665-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a665-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1a665-146">Minimum Shader Model</span></span>

<span data-ttu-id="1a665-147">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="1a665-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1a665-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1a665-148">Shader Model</span></span>                                              | <span data-ttu-id="1a665-149">支援</span><span class="sxs-lookup"><span data-stu-id="1a665-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1a665-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1a665-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1a665-151">是</span><span class="sxs-lookup"><span data-stu-id="1a665-151">yes</span></span>       |
| [<span data-ttu-id="1a665-152">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1a665-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1a665-153">不可以</span><span class="sxs-lookup"><span data-stu-id="1a665-153">no</span></span>        |
| [<span data-ttu-id="1a665-154">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1a665-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1a665-155">不可以</span><span class="sxs-lookup"><span data-stu-id="1a665-155">no</span></span>        |
| [<span data-ttu-id="1a665-156">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1a665-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1a665-157">不可以</span><span class="sxs-lookup"><span data-stu-id="1a665-157">no</span></span>        |
| [<span data-ttu-id="1a665-158">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1a665-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1a665-159">不可以</span><span class="sxs-lookup"><span data-stu-id="1a665-159">no</span></span>        |
| [<span data-ttu-id="1a665-160">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1a665-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1a665-161">不可以</span><span class="sxs-lookup"><span data-stu-id="1a665-161">no</span></span>        |



 

<span data-ttu-id="1a665-162">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。</span><span class="sxs-lookup"><span data-stu-id="1a665-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a665-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a665-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a665-164">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1a665-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





