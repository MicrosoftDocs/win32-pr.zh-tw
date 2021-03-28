---
title: '新增 (sm4-asm) '
description: 2個向量的元件取向加入。
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507728"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="aa8a5-103">新增 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="aa8a5-103">add (sm4 - asm)</span></span>

<span data-ttu-id="aa8a5-104">2個向量的元件取向加入。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="aa8a5-105">加入 \[ \_ sat \] 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aa8a5-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="aa8a5-106">項目</span><span class="sxs-lookup"><span data-stu-id="aa8a5-106">Item</span></span>                                                            | <span data-ttu-id="aa8a5-107">描述</span><span class="sxs-lookup"><span data-stu-id="aa8a5-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="aa8a5-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="aa8a5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="aa8a5-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="aa8a5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aa8a5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="aa8a5-111">\[在 \] 要加入至 *src1* 的向量中。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="aa8a5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="aa8a5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="aa8a5-113">\[在 \] 要加入至 *src0* 的向量中。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="aa8a5-114">備註</span><span class="sxs-lookup"><span data-stu-id="aa8a5-114">Remarks</span></span>

<span data-ttu-id="aa8a5-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="aa8a5-116">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="aa8a5-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-117">**src0 src1->**</span></span> | <span data-ttu-id="aa8a5-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-118">**-inf**</span></span> | <span data-ttu-id="aa8a5-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-119">**-F**</span></span>     | <span data-ttu-id="aa8a5-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-120">**-denorm**</span></span> | <span data-ttu-id="aa8a5-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-121">**-0**</span></span> | <span data-ttu-id="aa8a5-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-122">**+0**</span></span> | <span data-ttu-id="aa8a5-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-123">**denorm**</span></span> | <span data-ttu-id="aa8a5-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-124">**+F**</span></span>     | <span data-ttu-id="aa8a5-125">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-125">**+inf**</span></span> | <span data-ttu-id="aa8a5-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-126">**NaN**</span></span> |
| <span data-ttu-id="aa8a5-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-127">**-inf**</span></span>           | <span data-ttu-id="aa8a5-128">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-128">-inf</span></span>     | <span data-ttu-id="aa8a5-129">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-129">-inf</span></span>       | <span data-ttu-id="aa8a5-130">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-130">-inf</span></span>        | <span data-ttu-id="aa8a5-131">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-131">-inf</span></span>   | <span data-ttu-id="aa8a5-132">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-132">-inf</span></span>   | <span data-ttu-id="aa8a5-133">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-133">-inf</span></span>       | <span data-ttu-id="aa8a5-134">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-134">-inf</span></span>       | <span data-ttu-id="aa8a5-135">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-135">NaN</span></span>      | <span data-ttu-id="aa8a5-136">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-136">NaN</span></span>     |
| <span data-ttu-id="aa8a5-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-137">**-F**</span></span>             | <span data-ttu-id="aa8a5-138">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-138">-inf</span></span>     | <span data-ttu-id="aa8a5-139">-F</span><span class="sxs-lookup"><span data-stu-id="aa8a5-139">-F</span></span>         | <span data-ttu-id="aa8a5-140">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-140">src0</span></span>        | <span data-ttu-id="aa8a5-141">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-141">src0</span></span>   | <span data-ttu-id="aa8a5-142">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-142">src0</span></span>   | <span data-ttu-id="aa8a5-143">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-143">src0</span></span>       | <span data-ttu-id="aa8a5-144">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-144">+-F or +-0</span></span> | <span data-ttu-id="aa8a5-145">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-145">+inf</span></span>     | <span data-ttu-id="aa8a5-146">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-146">NaN</span></span>     |
| <span data-ttu-id="aa8a5-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-147">**-denorm**</span></span>        | <span data-ttu-id="aa8a5-148">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-148">-inf</span></span>     | <span data-ttu-id="aa8a5-149">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-149">src1</span></span>       | <span data-ttu-id="aa8a5-150">-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-150">-0</span></span>          | <span data-ttu-id="aa8a5-151">-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-151">-0</span></span>     | <span data-ttu-id="aa8a5-152">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-152">+0</span></span>     | <span data-ttu-id="aa8a5-153">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-153">+0</span></span>         | <span data-ttu-id="aa8a5-154">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-154">src1</span></span>       | <span data-ttu-id="aa8a5-155">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-155">+inf</span></span>     | <span data-ttu-id="aa8a5-156">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-156">NaN</span></span>     |
| <span data-ttu-id="aa8a5-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-157">**-0**</span></span>             | <span data-ttu-id="aa8a5-158">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-158">-inf</span></span>     | <span data-ttu-id="aa8a5-159">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-159">src1</span></span>       | <span data-ttu-id="aa8a5-160">-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-160">-0</span></span>          | <span data-ttu-id="aa8a5-161">-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-161">-0</span></span>     | <span data-ttu-id="aa8a5-162">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-162">+0</span></span>     | <span data-ttu-id="aa8a5-163">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-163">+0</span></span>         | <span data-ttu-id="aa8a5-164">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-164">src1</span></span>       | <span data-ttu-id="aa8a5-165">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-165">+inf</span></span>     | <span data-ttu-id="aa8a5-166">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-166">NaN</span></span>     |
| <span data-ttu-id="aa8a5-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-167">**+0**</span></span>             | <span data-ttu-id="aa8a5-168">我的 inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-168">i-inf</span></span>    | <span data-ttu-id="aa8a5-169">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-169">src1</span></span>       | <span data-ttu-id="aa8a5-170">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-170">+0</span></span>          | <span data-ttu-id="aa8a5-171">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-171">+0</span></span>     | <span data-ttu-id="aa8a5-172">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-172">+0</span></span>     | <span data-ttu-id="aa8a5-173">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-173">+0</span></span>         | <span data-ttu-id="aa8a5-174">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-174">src1</span></span>       | <span data-ttu-id="aa8a5-175">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-175">+inf</span></span>     | <span data-ttu-id="aa8a5-176">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-176">NaN</span></span>     |
| <span data-ttu-id="aa8a5-177">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-177">**+denorm**</span></span>        | <span data-ttu-id="aa8a5-178">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-178">-inf</span></span>     | <span data-ttu-id="aa8a5-179">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-179">src1</span></span>       | <span data-ttu-id="aa8a5-180">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-180">+0</span></span>          | <span data-ttu-id="aa8a5-181">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-181">+0</span></span>     | <span data-ttu-id="aa8a5-182">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-182">+0</span></span>     | <span data-ttu-id="aa8a5-183">+0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-183">+0</span></span>         | <span data-ttu-id="aa8a5-184">src1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-184">src1</span></span>       | <span data-ttu-id="aa8a5-185">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-185">+inf</span></span>     | <span data-ttu-id="aa8a5-186">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-186">NaN</span></span>     |
| <span data-ttu-id="aa8a5-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-187">**+F**</span></span>             | <span data-ttu-id="aa8a5-188">-inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-188">-inf</span></span>     | <span data-ttu-id="aa8a5-189">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-189">+-F or +-0</span></span> | <span data-ttu-id="aa8a5-190">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-190">src0</span></span>        | <span data-ttu-id="aa8a5-191">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-191">src0</span></span>   | <span data-ttu-id="aa8a5-192">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-192">src0</span></span>   | <span data-ttu-id="aa8a5-193">src0</span><span class="sxs-lookup"><span data-stu-id="aa8a5-193">src0</span></span>       | <span data-ttu-id="aa8a5-194">+F</span><span class="sxs-lookup"><span data-stu-id="aa8a5-194">+F</span></span>         | <span data-ttu-id="aa8a5-195">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-195">+inf</span></span>     | <span data-ttu-id="aa8a5-196">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-196">NaN</span></span>     |
| <span data-ttu-id="aa8a5-197">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-197">**+inf**</span></span>           | <span data-ttu-id="aa8a5-198">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-198">NaN</span></span>      | <span data-ttu-id="aa8a5-199">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-199">+inf</span></span>       | <span data-ttu-id="aa8a5-200">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-200">+inf</span></span>        | <span data-ttu-id="aa8a5-201">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-201">+inf</span></span>   | <span data-ttu-id="aa8a5-202">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-202">+inf</span></span>   | <span data-ttu-id="aa8a5-203">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-203">+inf</span></span>       | <span data-ttu-id="aa8a5-204">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-204">+inf</span></span>       | <span data-ttu-id="aa8a5-205">+inf</span><span class="sxs-lookup"><span data-stu-id="aa8a5-205">+inf</span></span>     | <span data-ttu-id="aa8a5-206">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-206">NaN</span></span>     |
| <span data-ttu-id="aa8a5-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="aa8a5-207">**NaN**</span></span>            | <span data-ttu-id="aa8a5-208">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-208">NaN</span></span>      | <span data-ttu-id="aa8a5-209">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-209">NaN</span></span>        | <span data-ttu-id="aa8a5-210">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-210">NaN</span></span>         | <span data-ttu-id="aa8a5-211">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-211">NaN</span></span>    | <span data-ttu-id="aa8a5-212">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-212">NaN</span></span>    | <span data-ttu-id="aa8a5-213">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-213">NaN</span></span>        | <span data-ttu-id="aa8a5-214">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-214">NaN</span></span>        | <span data-ttu-id="aa8a5-215">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-215">NaN</span></span>      | <span data-ttu-id="aa8a5-216">NaN</span><span class="sxs-lookup"><span data-stu-id="aa8a5-216">NaN</span></span>     |



 

<span data-ttu-id="aa8a5-217">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="aa8a5-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa8a5-218">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="aa8a5-218">Vertex Shader</span></span> | <span data-ttu-id="aa8a5-219">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="aa8a5-219">Geometry Shader</span></span> | <span data-ttu-id="aa8a5-220">像素著色器</span><span class="sxs-lookup"><span data-stu-id="aa8a5-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa8a5-221">x</span><span class="sxs-lookup"><span data-stu-id="aa8a5-221">x</span></span>             | <span data-ttu-id="aa8a5-222">x</span><span class="sxs-lookup"><span data-stu-id="aa8a5-222">x</span></span>               | <span data-ttu-id="aa8a5-223">x</span><span class="sxs-lookup"><span data-stu-id="aa8a5-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa8a5-224">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa8a5-224">Minimum Shader Model</span></span>

<span data-ttu-id="aa8a5-225">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="aa8a5-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa8a5-226">著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa8a5-226">Shader Model</span></span>                                              | <span data-ttu-id="aa8a5-227">支援</span><span class="sxs-lookup"><span data-stu-id="aa8a5-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa8a5-228">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="aa8a5-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa8a5-229">是</span><span class="sxs-lookup"><span data-stu-id="aa8a5-229">yes</span></span>       |
| [<span data-ttu-id="aa8a5-230">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="aa8a5-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa8a5-231">是</span><span class="sxs-lookup"><span data-stu-id="aa8a5-231">yes</span></span>       |
| [<span data-ttu-id="aa8a5-232">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="aa8a5-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa8a5-233">是</span><span class="sxs-lookup"><span data-stu-id="aa8a5-233">yes</span></span>       |
| [<span data-ttu-id="aa8a5-234">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa8a5-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa8a5-235">不可以</span><span class="sxs-lookup"><span data-stu-id="aa8a5-235">no</span></span>        |
| [<span data-ttu-id="aa8a5-236">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa8a5-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa8a5-237">不可以</span><span class="sxs-lookup"><span data-stu-id="aa8a5-237">no</span></span>        |
| [<span data-ttu-id="aa8a5-238">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa8a5-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa8a5-239">不可以</span><span class="sxs-lookup"><span data-stu-id="aa8a5-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa8a5-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa8a5-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8a5-241">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa8a5-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





