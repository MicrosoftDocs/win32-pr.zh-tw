---
title: 'dfma (sm5-asm) '
description: 執行融合乘積的新增。
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313658"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="e22d3-103">dfma (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="e22d3-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="e22d3-104">執行融合乘積的新增。</span><span class="sxs-lookup"><span data-stu-id="e22d3-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="e22d3-105">dfma \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e22d3-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e22d3-106">項目</span><span class="sxs-lookup"><span data-stu-id="e22d3-106">Item</span></span>                                                            | <span data-ttu-id="e22d3-107">描述</span><span class="sxs-lookup"><span data-stu-id="e22d3-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22d3-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="e22d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e22d3-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="e22d3-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="e22d3-110">結果值必須正確到 0.5 ULP。</span><span class="sxs-lookup"><span data-stu-id="e22d3-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="e22d3-111">*目的地*  = *src0* \**src1*  + *src2 收取*</span><span class="sxs-lookup"><span data-stu-id="e22d3-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="e22d3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e22d3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e22d3-113">\[在 \] 要與 *src1* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="e22d3-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="e22d3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e22d3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e22d3-115">\[在 \] 要與 *src0* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="e22d3-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="e22d3-116"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="e22d3-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="e22d3-117">\[在 \] 要新增至 *src0* \* *src1* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="e22d3-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e22d3-118">備註</span><span class="sxs-lookup"><span data-stu-id="e22d3-118">Remarks</span></span>

<span data-ttu-id="e22d3-119">使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。</span><span class="sxs-lookup"><span data-stu-id="e22d3-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="e22d3-120">系統支援 DirectX 11.1。</span><span class="sxs-lookup"><span data-stu-id="e22d3-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="e22d3-121">系統包含 WDDM 1.2 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e22d3-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="e22d3-122">驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e22d3-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="e22d3-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e22d3-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e22d3-124">頂點</span><span class="sxs-lookup"><span data-stu-id="e22d3-124">Vertex</span></span> | <span data-ttu-id="e22d3-125">船體</span><span class="sxs-lookup"><span data-stu-id="e22d3-125">Hull</span></span> | <span data-ttu-id="e22d3-126">網域</span><span class="sxs-lookup"><span data-stu-id="e22d3-126">Domain</span></span> | <span data-ttu-id="e22d3-127">幾何</span><span class="sxs-lookup"><span data-stu-id="e22d3-127">Geometry</span></span> | <span data-ttu-id="e22d3-128">像素</span><span class="sxs-lookup"><span data-stu-id="e22d3-128">Pixel</span></span> | <span data-ttu-id="e22d3-129">計算</span><span class="sxs-lookup"><span data-stu-id="e22d3-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e22d3-130">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-130">X</span></span>      | <span data-ttu-id="e22d3-131">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-131">X</span></span>    | <span data-ttu-id="e22d3-132">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-132">X</span></span>      | <span data-ttu-id="e22d3-133">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-133">X</span></span>        | <span data-ttu-id="e22d3-134">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-134">X</span></span>     | <span data-ttu-id="e22d3-135">X</span><span class="sxs-lookup"><span data-stu-id="e22d3-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e22d3-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e22d3-136">Minimum Shader Model</span></span>

<span data-ttu-id="e22d3-137">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="e22d3-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e22d3-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e22d3-138">Shader Model</span></span>                                              | <span data-ttu-id="e22d3-139">支援</span><span class="sxs-lookup"><span data-stu-id="e22d3-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e22d3-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e22d3-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e22d3-141">是</span><span class="sxs-lookup"><span data-stu-id="e22d3-141">yes</span></span>       |
| [<span data-ttu-id="e22d3-142">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e22d3-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e22d3-143">不可以</span><span class="sxs-lookup"><span data-stu-id="e22d3-143">no</span></span>        |
| [<span data-ttu-id="e22d3-144">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e22d3-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e22d3-145">不可以</span><span class="sxs-lookup"><span data-stu-id="e22d3-145">no</span></span>        |
| [<span data-ttu-id="e22d3-146">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e22d3-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e22d3-147">不可以</span><span class="sxs-lookup"><span data-stu-id="e22d3-147">no</span></span>        |
| [<span data-ttu-id="e22d3-148">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e22d3-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e22d3-149">不可以</span><span class="sxs-lookup"><span data-stu-id="e22d3-149">no</span></span>        |
| [<span data-ttu-id="e22d3-150">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e22d3-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e22d3-151">不可以</span><span class="sxs-lookup"><span data-stu-id="e22d3-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e22d3-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="e22d3-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e22d3-153">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e22d3-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





