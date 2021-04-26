---
title: 'drcp (sm5-asm) '
description: 將元件雙向的雙精確度計算為反向。
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998335"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="45142-103">drcp (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="45142-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="45142-104">將元件雙向的雙精確度計算為反向。</span><span class="sxs-lookup"><span data-stu-id="45142-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="45142-105">rcp \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="45142-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="45142-106">項目</span><span class="sxs-lookup"><span data-stu-id="45142-106">Item</span></span>                                                            | <span data-ttu-id="45142-107">描述</span><span class="sxs-lookup"><span data-stu-id="45142-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45142-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="45142-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="45142-109">\[在 \] 結果的位址中</span><span class="sxs-lookup"><span data-stu-id="45142-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="45142-110">*目的地*  = **1.0**  / *src0*。</span><span class="sxs-lookup"><span data-stu-id="45142-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="45142-111">結果值必須正確到 1.0 ULP</span><span class="sxs-lookup"><span data-stu-id="45142-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="45142-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="45142-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="45142-113">\[\]要採用的數位。</span><span class="sxs-lookup"><span data-stu-id="45142-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="45142-114">備註</span><span class="sxs-lookup"><span data-stu-id="45142-114">Remarks</span></span>

<span data-ttu-id="45142-115">只有在使用 double 作為引數時，才會透過 rcp () 內建明確呼叫 DRCP 指令來發出 HLSL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="45142-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="45142-116">此指令的精確度必須為 1.0 ULP。</span><span class="sxs-lookup"><span data-stu-id="45142-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="45142-117">使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。</span><span class="sxs-lookup"><span data-stu-id="45142-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="45142-118">系統支援 DirectX 11.1。</span><span class="sxs-lookup"><span data-stu-id="45142-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="45142-119">系統包含 WDDM 1.2 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="45142-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="45142-120">驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="45142-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="45142-121">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="45142-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="45142-122">在此表中，F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="45142-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="45142-123">**Src**-></span><span class="sxs-lookup"><span data-stu-id="45142-123">**src**-></span></span>  | <span data-ttu-id="45142-124">**-inf**</span><span class="sxs-lookup"><span data-stu-id="45142-124">**-inf**</span></span> | <span data-ttu-id="45142-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="45142-125">**-F**</span></span> | <span data-ttu-id="45142-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="45142-126">**-0**</span></span> | <span data-ttu-id="45142-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="45142-127">**+0**</span></span> | <span data-ttu-id="45142-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="45142-128">**+F**</span></span> | <span data-ttu-id="45142-129">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="45142-129">**+inf**</span></span> | <span data-ttu-id="45142-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="45142-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="45142-131">**目標**-></span><span class="sxs-lookup"><span data-stu-id="45142-131">**dest**-></span></span> | <span data-ttu-id="45142-132">-0</span><span class="sxs-lookup"><span data-stu-id="45142-132">-0</span></span>       | <span data-ttu-id="45142-133">-F</span><span class="sxs-lookup"><span data-stu-id="45142-133">-F</span></span>     | <span data-ttu-id="45142-134">-inf</span><span class="sxs-lookup"><span data-stu-id="45142-134">-inf</span></span>   | <span data-ttu-id="45142-135">+inf</span><span class="sxs-lookup"><span data-stu-id="45142-135">+inf</span></span>   | <span data-ttu-id="45142-136">+F</span><span class="sxs-lookup"><span data-stu-id="45142-136">+F</span></span>     | <span data-ttu-id="45142-137">+0</span><span class="sxs-lookup"><span data-stu-id="45142-137">+0</span></span>       | <span data-ttu-id="45142-138">NaN</span><span class="sxs-lookup"><span data-stu-id="45142-138">NaN</span></span>     |



 

<span data-ttu-id="45142-139">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="45142-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="45142-140">頂點</span><span class="sxs-lookup"><span data-stu-id="45142-140">Vertex</span></span> | <span data-ttu-id="45142-141">船體</span><span class="sxs-lookup"><span data-stu-id="45142-141">Hull</span></span> | <span data-ttu-id="45142-142">網域</span><span class="sxs-lookup"><span data-stu-id="45142-142">Domain</span></span> | <span data-ttu-id="45142-143">幾何</span><span class="sxs-lookup"><span data-stu-id="45142-143">Geometry</span></span> | <span data-ttu-id="45142-144">像素</span><span class="sxs-lookup"><span data-stu-id="45142-144">Pixel</span></span> | <span data-ttu-id="45142-145">計算</span><span class="sxs-lookup"><span data-stu-id="45142-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="45142-146">X</span><span class="sxs-lookup"><span data-stu-id="45142-146">X</span></span>      | <span data-ttu-id="45142-147">X</span><span class="sxs-lookup"><span data-stu-id="45142-147">X</span></span>    | <span data-ttu-id="45142-148">X</span><span class="sxs-lookup"><span data-stu-id="45142-148">X</span></span>      | <span data-ttu-id="45142-149">X</span><span class="sxs-lookup"><span data-stu-id="45142-149">X</span></span>        | <span data-ttu-id="45142-150">X</span><span class="sxs-lookup"><span data-stu-id="45142-150">X</span></span>     | <span data-ttu-id="45142-151">X</span><span class="sxs-lookup"><span data-stu-id="45142-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="45142-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="45142-152">Minimum Shader Model</span></span>

<span data-ttu-id="45142-153">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="45142-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="45142-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="45142-154">Shader Model</span></span>                                              | <span data-ttu-id="45142-155">支援</span><span class="sxs-lookup"><span data-stu-id="45142-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="45142-156">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="45142-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="45142-157">是</span><span class="sxs-lookup"><span data-stu-id="45142-157">yes</span></span>       |
| [<span data-ttu-id="45142-158">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="45142-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="45142-159">否</span><span class="sxs-lookup"><span data-stu-id="45142-159">no</span></span>        |
| [<span data-ttu-id="45142-160">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="45142-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="45142-161">否</span><span class="sxs-lookup"><span data-stu-id="45142-161">no</span></span>        |
| [<span data-ttu-id="45142-162">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="45142-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="45142-163">否</span><span class="sxs-lookup"><span data-stu-id="45142-163">no</span></span>        |
| [<span data-ttu-id="45142-164">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="45142-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="45142-165">否</span><span class="sxs-lookup"><span data-stu-id="45142-165">no</span></span>        |
| [<span data-ttu-id="45142-166">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="45142-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="45142-167">否</span><span class="sxs-lookup"><span data-stu-id="45142-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="45142-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="45142-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45142-169">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="45142-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





