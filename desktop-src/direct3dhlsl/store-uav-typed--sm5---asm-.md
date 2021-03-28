---
title: 'store_uav_typed (sm5-asm) '
description: 隨機存取將專案寫入至具類型的未排序存取視圖 (UAV) 。
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022808"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="5ad6e-103">儲存 \_ uav \_ 類型 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="5ad6e-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="5ad6e-104">隨機存取將專案寫入至具類型的未排序存取視圖 (UAV) 。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="5ad6e-105">store \_ uav 具 \_ 類型的 dstUAV. Xyzw、dstAddress \[ . swizzle \] 、src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5ad6e-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="5ad6e-106">項目</span><span class="sxs-lookup"><span data-stu-id="5ad6e-106">Item</span></span>                                                                                                           | <span data-ttu-id="5ad6e-107">描述</span><span class="sxs-lookup"><span data-stu-id="5ad6e-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5ad6e-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="5ad6e-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="5ad6e-109">\[中的 \] 包含運算的結果。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="5ad6e-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="5ad6e-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="5ad6e-111">\[在 \] 要寫入的位址中。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="5ad6e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5ad6e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="5ad6e-113">\[在 \] 要寫入的元件中。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="5ad6e-114">備註</span><span class="sxs-lookup"><span data-stu-id="5ad6e-114">Remarks</span></span>

<span data-ttu-id="5ad6e-115">此指令會在 \* *dstAddress* 的位址執行從 *src0* 寫入至 *dstUAV* 的4個元件32位元素。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="5ad6e-116">*dstUAV* 是具類型的 UAV (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="5ad6e-117">UAV 的格式會決定格式轉換。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="5ad6e-118">從位址取得的32位不帶正負號整陣列件的數目，取決於在 *dstUAV* 中宣告之資源的維度。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="5ad6e-119">此位址是在元素中。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-119">This address is in elements.</span></span>

<span data-ttu-id="5ad6e-120">超出範圍定址表示不會將任何內容寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="5ad6e-121">*dstUAV* 一律有 xyzw 寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="5ad6e-122">必須撰寫所有的元件。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-122">All components must be written.</span></span>

<span data-ttu-id="5ad6e-123">它無效且未定義，無法在未宣告為具類型的 UAV 上使用這個指令。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="5ad6e-124">也就是說，在結構化或無類型的 UAV 上執行這項操作將會無效。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="5ad6e-125">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5ad6e-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ad6e-126">頂點</span><span class="sxs-lookup"><span data-stu-id="5ad6e-126">Vertex</span></span> | <span data-ttu-id="5ad6e-127">船體</span><span class="sxs-lookup"><span data-stu-id="5ad6e-127">Hull</span></span> | <span data-ttu-id="5ad6e-128">網域</span><span class="sxs-lookup"><span data-stu-id="5ad6e-128">Domain</span></span> | <span data-ttu-id="5ad6e-129">幾何</span><span class="sxs-lookup"><span data-stu-id="5ad6e-129">Geometry</span></span> | <span data-ttu-id="5ad6e-130">像素</span><span class="sxs-lookup"><span data-stu-id="5ad6e-130">Pixel</span></span> | <span data-ttu-id="5ad6e-131">計算</span><span class="sxs-lookup"><span data-stu-id="5ad6e-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5ad6e-132">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-132">X</span></span>     | <span data-ttu-id="5ad6e-133">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-133">X</span></span>       |



 

<span data-ttu-id="5ad6e-134">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="5ad6e-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="5ad6e-135">頂點</span><span class="sxs-lookup"><span data-stu-id="5ad6e-135">Vertex</span></span> | <span data-ttu-id="5ad6e-136">船體</span><span class="sxs-lookup"><span data-stu-id="5ad6e-136">Hull</span></span> | <span data-ttu-id="5ad6e-137">網域</span><span class="sxs-lookup"><span data-stu-id="5ad6e-137">Domain</span></span> | <span data-ttu-id="5ad6e-138">幾何</span><span class="sxs-lookup"><span data-stu-id="5ad6e-138">Geometry</span></span> | <span data-ttu-id="5ad6e-139">像素</span><span class="sxs-lookup"><span data-stu-id="5ad6e-139">Pixel</span></span> | <span data-ttu-id="5ad6e-140">計算</span><span class="sxs-lookup"><span data-stu-id="5ad6e-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5ad6e-141">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-141">X</span></span>      | <span data-ttu-id="5ad6e-142">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-142">X</span></span>    | <span data-ttu-id="5ad6e-143">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-143">X</span></span>      | <span data-ttu-id="5ad6e-144">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-144">X</span></span>        | <span data-ttu-id="5ad6e-145">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-145">X</span></span>     | <span data-ttu-id="5ad6e-146">X</span><span class="sxs-lookup"><span data-stu-id="5ad6e-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ad6e-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5ad6e-147">Minimum Shader Model</span></span>

<span data-ttu-id="5ad6e-148">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="5ad6e-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5ad6e-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5ad6e-149">Shader Model</span></span>                                              | <span data-ttu-id="5ad6e-150">支援</span><span class="sxs-lookup"><span data-stu-id="5ad6e-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ad6e-151">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5ad6e-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ad6e-152">是</span><span class="sxs-lookup"><span data-stu-id="5ad6e-152">yes</span></span>       |
| [<span data-ttu-id="5ad6e-153">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5ad6e-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ad6e-154">不可以</span><span class="sxs-lookup"><span data-stu-id="5ad6e-154">no</span></span>        |
| [<span data-ttu-id="5ad6e-155">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5ad6e-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ad6e-156">不可以</span><span class="sxs-lookup"><span data-stu-id="5ad6e-156">no</span></span>        |
| [<span data-ttu-id="5ad6e-157">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ad6e-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ad6e-158">不可以</span><span class="sxs-lookup"><span data-stu-id="5ad6e-158">no</span></span>        |
| [<span data-ttu-id="5ad6e-159">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ad6e-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ad6e-160">不可以</span><span class="sxs-lookup"><span data-stu-id="5ad6e-160">no</span></span>        |
| [<span data-ttu-id="5ad6e-161">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ad6e-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ad6e-162">不可以</span><span class="sxs-lookup"><span data-stu-id="5ad6e-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ad6e-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ad6e-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad6e-164">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ad6e-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





