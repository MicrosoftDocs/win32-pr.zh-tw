---
title: 'ddiv (sm5-asm) '
description: 計算元件的雙精確度除法。
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990731"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="2c491-103">ddiv (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="2c491-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="2c491-104">計算元件的雙精確度除法。</span><span class="sxs-lookup"><span data-stu-id="2c491-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="2c491-105">ddiv \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2c491-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2c491-106">項目</span><span class="sxs-lookup"><span data-stu-id="2c491-106">Item</span></span>                                                            | <span data-ttu-id="2c491-107">描述</span><span class="sxs-lookup"><span data-stu-id="2c491-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c491-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="2c491-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2c491-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="2c491-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="2c491-110">結果值必須正確到 0.5 ULP。</span><span class="sxs-lookup"><span data-stu-id="2c491-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="2c491-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2c491-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2c491-112">\[被 \] 除數。</span><span class="sxs-lookup"><span data-stu-id="2c491-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="2c491-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2c491-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2c491-114">\[\]除數。</span><span class="sxs-lookup"><span data-stu-id="2c491-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="2c491-115">備註</span><span class="sxs-lookup"><span data-stu-id="2c491-115">Remarks</span></span>

<span data-ttu-id="2c491-116">每當使用除法運算子搭配雙精度浮點數時，HLSL 編譯器就會發出 DDIV 指令。</span><span class="sxs-lookup"><span data-stu-id="2c491-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="2c491-117">此指令的精確度將必須為 0.5 ULP。</span><span class="sxs-lookup"><span data-stu-id="2c491-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="2c491-118">使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。</span><span class="sxs-lookup"><span data-stu-id="2c491-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="2c491-119">系統支援 DirectX 11.1。</span><span class="sxs-lookup"><span data-stu-id="2c491-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="2c491-120">系統包含 WDDM 1.2 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2c491-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="2c491-121">驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2c491-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="2c491-122">下表顯示使用各種不同的數位類別來執行指令時所 btained 的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="2c491-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="2c491-123">在此表中，F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="2c491-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="2c491-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="2c491-124">**src0 src1 ->**</span></span> | <span data-ttu-id="2c491-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2c491-125">**-inf**</span></span> | <span data-ttu-id="2c491-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="2c491-126">**-F**</span></span> | <span data-ttu-id="2c491-127">**-1。0**</span><span class="sxs-lookup"><span data-stu-id="2c491-127">**-1.0**</span></span> | <span data-ttu-id="2c491-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="2c491-128">**-0**</span></span> | <span data-ttu-id="2c491-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="2c491-129">**+0**</span></span> | <span data-ttu-id="2c491-130">**+ 1。0**</span><span class="sxs-lookup"><span data-stu-id="2c491-130">**+1.0**</span></span> | <span data-ttu-id="2c491-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2c491-131">**+F**</span></span> | <span data-ttu-id="2c491-132">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="2c491-132">**+inf**</span></span> | <span data-ttu-id="2c491-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2c491-133">**NaN**</span></span> |
| <span data-ttu-id="2c491-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2c491-134">**-inf**</span></span>            | <span data-ttu-id="2c491-135">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-135">NaN</span></span>      | <span data-ttu-id="2c491-136">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-136">+inf</span></span>   | <span data-ttu-id="2c491-137">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-137">+inf</span></span>     | <span data-ttu-id="2c491-138">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-138">+inf</span></span>   | <span data-ttu-id="2c491-139">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-139">-inf</span></span>   | <span data-ttu-id="2c491-140">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-140">-inf</span></span>     | <span data-ttu-id="2c491-141">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-141">-inf</span></span>   | <span data-ttu-id="2c491-142">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-142">NaN</span></span>      | <span data-ttu-id="2c491-143">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-143">NaN</span></span>     |
| <span data-ttu-id="2c491-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="2c491-144">**-F**</span></span>              | <span data-ttu-id="2c491-145">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-145">+0</span></span>       | <span data-ttu-id="2c491-146">+F</span><span class="sxs-lookup"><span data-stu-id="2c491-146">+F</span></span>     | <span data-ttu-id="2c491-147">-src0</span><span class="sxs-lookup"><span data-stu-id="2c491-147">-src0</span></span>    | <span data-ttu-id="2c491-148">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-148">+inf</span></span>   | <span data-ttu-id="2c491-149">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-149">-inf</span></span>   | <span data-ttu-id="2c491-150">src0</span><span class="sxs-lookup"><span data-stu-id="2c491-150">src0</span></span>     | <span data-ttu-id="2c491-151">-F</span><span class="sxs-lookup"><span data-stu-id="2c491-151">-F</span></span>     | <span data-ttu-id="2c491-152">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-152">-0</span></span>       | <span data-ttu-id="2c491-153">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-153">NaN</span></span>     |
| <span data-ttu-id="2c491-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="2c491-154">**-0**</span></span>              | <span data-ttu-id="2c491-155">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-155">+0</span></span>       | <span data-ttu-id="2c491-156">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-156">+0</span></span>     | <span data-ttu-id="2c491-157">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-157">+0</span></span>       | <span data-ttu-id="2c491-158">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-158">NaN</span></span>    | <span data-ttu-id="2c491-159">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-159">NaN</span></span>    | <span data-ttu-id="2c491-160">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-160">-0</span></span>       | <span data-ttu-id="2c491-161">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-161">-0</span></span>     | <span data-ttu-id="2c491-162">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-162">-0</span></span>       | <span data-ttu-id="2c491-163">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-163">NaN</span></span>     |
| <span data-ttu-id="2c491-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="2c491-164">**+0**</span></span>              | <span data-ttu-id="2c491-165">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-165">-0</span></span>       | <span data-ttu-id="2c491-166">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-166">-0</span></span>     | <span data-ttu-id="2c491-167">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-167">-0</span></span>       | <span data-ttu-id="2c491-168">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-168">NaN</span></span>    | <span data-ttu-id="2c491-169">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-169">NaN</span></span>    | <span data-ttu-id="2c491-170">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-170">+0</span></span>       | <span data-ttu-id="2c491-171">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-171">+0</span></span>     | <span data-ttu-id="2c491-172">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-172">+0</span></span>       | <span data-ttu-id="2c491-173">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-173">NaN</span></span>     |
| <span data-ttu-id="2c491-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2c491-174">**+F**</span></span>              | <span data-ttu-id="2c491-175">-0</span><span class="sxs-lookup"><span data-stu-id="2c491-175">-0</span></span>       | <span data-ttu-id="2c491-176">-F</span><span class="sxs-lookup"><span data-stu-id="2c491-176">-F</span></span>     | <span data-ttu-id="2c491-177">-src0</span><span class="sxs-lookup"><span data-stu-id="2c491-177">-src0</span></span>    | <span data-ttu-id="2c491-178">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-178">-inf</span></span>   | <span data-ttu-id="2c491-179">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-179">+inf</span></span>   | <span data-ttu-id="2c491-180">src0</span><span class="sxs-lookup"><span data-stu-id="2c491-180">src0</span></span>     | <span data-ttu-id="2c491-181">+F</span><span class="sxs-lookup"><span data-stu-id="2c491-181">+F</span></span>     | <span data-ttu-id="2c491-182">+0</span><span class="sxs-lookup"><span data-stu-id="2c491-182">+0</span></span>       | <span data-ttu-id="2c491-183">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-183">NaN</span></span>     |
| <span data-ttu-id="2c491-184">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="2c491-184">**+inf**</span></span>            | <span data-ttu-id="2c491-185">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-185">NaN</span></span>      | <span data-ttu-id="2c491-186">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-186">-inf</span></span>   | <span data-ttu-id="2c491-187">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-187">-inf</span></span>     | <span data-ttu-id="2c491-188">-inf</span><span class="sxs-lookup"><span data-stu-id="2c491-188">-inf</span></span>   | <span data-ttu-id="2c491-189">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-189">+inf</span></span>   | <span data-ttu-id="2c491-190">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-190">+inf</span></span>     | <span data-ttu-id="2c491-191">+inf</span><span class="sxs-lookup"><span data-stu-id="2c491-191">+inf</span></span>   | <span data-ttu-id="2c491-192">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-192">NaN</span></span>      | <span data-ttu-id="2c491-193">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-193">NaN</span></span>     |
| <span data-ttu-id="2c491-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2c491-194">**NaN**</span></span>             | <span data-ttu-id="2c491-195">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-195">NaN</span></span>      | <span data-ttu-id="2c491-196">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-196">NaN</span></span>    | <span data-ttu-id="2c491-197">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-197">NaN</span></span>      | <span data-ttu-id="2c491-198">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-198">NaN</span></span>    | <span data-ttu-id="2c491-199">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-199">NaN</span></span>    | <span data-ttu-id="2c491-200">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-200">NaN</span></span>      | <span data-ttu-id="2c491-201">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-201">NaN</span></span>    | <span data-ttu-id="2c491-202">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-202">NaN</span></span>      | <span data-ttu-id="2c491-203">NaN</span><span class="sxs-lookup"><span data-stu-id="2c491-203">NaN</span></span>     |



 

<span data-ttu-id="2c491-204">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2c491-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c491-205">頂點</span><span class="sxs-lookup"><span data-stu-id="2c491-205">Vertex</span></span> | <span data-ttu-id="2c491-206">船體</span><span class="sxs-lookup"><span data-stu-id="2c491-206">Hull</span></span> | <span data-ttu-id="2c491-207">網域</span><span class="sxs-lookup"><span data-stu-id="2c491-207">Domain</span></span> | <span data-ttu-id="2c491-208">幾何</span><span class="sxs-lookup"><span data-stu-id="2c491-208">Geometry</span></span> | <span data-ttu-id="2c491-209">像素</span><span class="sxs-lookup"><span data-stu-id="2c491-209">Pixel</span></span> | <span data-ttu-id="2c491-210">計算</span><span class="sxs-lookup"><span data-stu-id="2c491-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c491-211">X</span><span class="sxs-lookup"><span data-stu-id="2c491-211">X</span></span>      | <span data-ttu-id="2c491-212">X</span><span class="sxs-lookup"><span data-stu-id="2c491-212">X</span></span>    | <span data-ttu-id="2c491-213">X</span><span class="sxs-lookup"><span data-stu-id="2c491-213">X</span></span>      | <span data-ttu-id="2c491-214">X</span><span class="sxs-lookup"><span data-stu-id="2c491-214">X</span></span>        | <span data-ttu-id="2c491-215">X</span><span class="sxs-lookup"><span data-stu-id="2c491-215">X</span></span>     | <span data-ttu-id="2c491-216">X</span><span class="sxs-lookup"><span data-stu-id="2c491-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c491-217">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2c491-217">Minimum Shader Model</span></span>

<span data-ttu-id="2c491-218">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="2c491-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c491-219">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2c491-219">Shader Model</span></span>                                              | <span data-ttu-id="2c491-220">支援</span><span class="sxs-lookup"><span data-stu-id="2c491-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c491-221">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2c491-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c491-222">是</span><span class="sxs-lookup"><span data-stu-id="2c491-222">yes</span></span>       |
| [<span data-ttu-id="2c491-223">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2c491-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c491-224">不可以</span><span class="sxs-lookup"><span data-stu-id="2c491-224">no</span></span>        |
| [<span data-ttu-id="2c491-225">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2c491-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c491-226">不可以</span><span class="sxs-lookup"><span data-stu-id="2c491-226">no</span></span>        |
| [<span data-ttu-id="2c491-227">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2c491-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c491-228">不可以</span><span class="sxs-lookup"><span data-stu-id="2c491-228">no</span></span>        |
| [<span data-ttu-id="2c491-229">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2c491-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c491-230">不可以</span><span class="sxs-lookup"><span data-stu-id="2c491-230">no</span></span>        |
| [<span data-ttu-id="2c491-231">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2c491-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c491-232">不可以</span><span class="sxs-lookup"><span data-stu-id="2c491-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c491-233">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c491-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c491-234">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2c491-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





