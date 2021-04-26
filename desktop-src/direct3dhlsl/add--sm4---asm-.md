---
title: '新增 (sm4-asm) '
description: 2個向量的元件取向加入。
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994975"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="e69a9-103">新增 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="e69a9-103">add (sm4 - asm)</span></span>

<span data-ttu-id="e69a9-104">2個向量的元件取向加入。</span><span class="sxs-lookup"><span data-stu-id="e69a9-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="e69a9-105">加入 \[ \_ sat \] 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e69a9-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e69a9-106">項目</span><span class="sxs-lookup"><span data-stu-id="e69a9-106">Item</span></span>                                                            | <span data-ttu-id="e69a9-107">描述</span><span class="sxs-lookup"><span data-stu-id="e69a9-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e69a9-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="e69a9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e69a9-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="e69a9-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e69a9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e69a9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e69a9-111">\[在 \] 要加入至 *src1* 的向量中。</span><span class="sxs-lookup"><span data-stu-id="e69a9-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="e69a9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e69a9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e69a9-113">\[在 \] 要加入至 *src0* 的向量中。</span><span class="sxs-lookup"><span data-stu-id="e69a9-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="e69a9-114">備註</span><span class="sxs-lookup"><span data-stu-id="e69a9-114">Remarks</span></span>

<span data-ttu-id="e69a9-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="e69a9-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="e69a9-116">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="e69a9-116">F means finite real number.</span></span>



| <span data-ttu-id="e69a9-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="e69a9-117">**src0 src1->**</span></span> | <span data-ttu-id="e69a9-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="e69a9-118">**-inf**</span></span> | <span data-ttu-id="e69a9-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="e69a9-119">**-F**</span></span>     | <span data-ttu-id="e69a9-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="e69a9-120">**-denorm**</span></span> | <span data-ttu-id="e69a9-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="e69a9-121">**-0**</span></span> | <span data-ttu-id="e69a9-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="e69a9-122">**+0**</span></span> | <span data-ttu-id="e69a9-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="e69a9-123">**denorm**</span></span> | <span data-ttu-id="e69a9-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="e69a9-124">**+F**</span></span>     | <span data-ttu-id="e69a9-125">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="e69a9-125">**+inf**</span></span> | <span data-ttu-id="e69a9-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e69a9-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="e69a9-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="e69a9-127">**-inf**</span></span>           | <span data-ttu-id="e69a9-128">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-128">-inf</span></span>     | <span data-ttu-id="e69a9-129">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-129">-inf</span></span>       | <span data-ttu-id="e69a9-130">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-130">-inf</span></span>        | <span data-ttu-id="e69a9-131">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-131">-inf</span></span>   | <span data-ttu-id="e69a9-132">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-132">-inf</span></span>   | <span data-ttu-id="e69a9-133">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-133">-inf</span></span>       | <span data-ttu-id="e69a9-134">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-134">-inf</span></span>       | <span data-ttu-id="e69a9-135">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-135">NaN</span></span>      | <span data-ttu-id="e69a9-136">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-136">NaN</span></span>     |
| <span data-ttu-id="e69a9-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="e69a9-137">**-F**</span></span>             | <span data-ttu-id="e69a9-138">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-138">-inf</span></span>     | <span data-ttu-id="e69a9-139">-F</span><span class="sxs-lookup"><span data-stu-id="e69a9-139">-F</span></span>         | <span data-ttu-id="e69a9-140">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-140">src0</span></span>        | <span data-ttu-id="e69a9-141">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-141">src0</span></span>   | <span data-ttu-id="e69a9-142">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-142">src0</span></span>   | <span data-ttu-id="e69a9-143">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-143">src0</span></span>       | <span data-ttu-id="e69a9-144">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-144">+-F or +-0</span></span> | <span data-ttu-id="e69a9-145">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-145">+inf</span></span>     | <span data-ttu-id="e69a9-146">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-146">NaN</span></span>     |
| <span data-ttu-id="e69a9-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="e69a9-147">**-denorm**</span></span>        | <span data-ttu-id="e69a9-148">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-148">-inf</span></span>     | <span data-ttu-id="e69a9-149">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-149">src1</span></span>       | <span data-ttu-id="e69a9-150">-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-150">-0</span></span>          | <span data-ttu-id="e69a9-151">-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-151">-0</span></span>     | <span data-ttu-id="e69a9-152">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-152">+0</span></span>     | <span data-ttu-id="e69a9-153">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-153">+0</span></span>         | <span data-ttu-id="e69a9-154">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-154">src1</span></span>       | <span data-ttu-id="e69a9-155">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-155">+inf</span></span>     | <span data-ttu-id="e69a9-156">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-156">NaN</span></span>     |
| <span data-ttu-id="e69a9-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="e69a9-157">**-0**</span></span>             | <span data-ttu-id="e69a9-158">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-158">-inf</span></span>     | <span data-ttu-id="e69a9-159">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-159">src1</span></span>       | <span data-ttu-id="e69a9-160">-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-160">-0</span></span>          | <span data-ttu-id="e69a9-161">-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-161">-0</span></span>     | <span data-ttu-id="e69a9-162">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-162">+0</span></span>     | <span data-ttu-id="e69a9-163">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-163">+0</span></span>         | <span data-ttu-id="e69a9-164">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-164">src1</span></span>       | <span data-ttu-id="e69a9-165">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-165">+inf</span></span>     | <span data-ttu-id="e69a9-166">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-166">NaN</span></span>     |
| <span data-ttu-id="e69a9-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="e69a9-167">**+0**</span></span>             | <span data-ttu-id="e69a9-168">我的 inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-168">i-inf</span></span>    | <span data-ttu-id="e69a9-169">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-169">src1</span></span>       | <span data-ttu-id="e69a9-170">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-170">+0</span></span>          | <span data-ttu-id="e69a9-171">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-171">+0</span></span>     | <span data-ttu-id="e69a9-172">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-172">+0</span></span>     | <span data-ttu-id="e69a9-173">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-173">+0</span></span>         | <span data-ttu-id="e69a9-174">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-174">src1</span></span>       | <span data-ttu-id="e69a9-175">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-175">+inf</span></span>     | <span data-ttu-id="e69a9-176">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-176">NaN</span></span>     |
| <span data-ttu-id="e69a9-177">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="e69a9-177">**+denorm**</span></span>        | <span data-ttu-id="e69a9-178">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-178">-inf</span></span>     | <span data-ttu-id="e69a9-179">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-179">src1</span></span>       | <span data-ttu-id="e69a9-180">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-180">+0</span></span>          | <span data-ttu-id="e69a9-181">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-181">+0</span></span>     | <span data-ttu-id="e69a9-182">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-182">+0</span></span>     | <span data-ttu-id="e69a9-183">+0</span><span class="sxs-lookup"><span data-stu-id="e69a9-183">+0</span></span>         | <span data-ttu-id="e69a9-184">src1</span><span class="sxs-lookup"><span data-stu-id="e69a9-184">src1</span></span>       | <span data-ttu-id="e69a9-185">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-185">+inf</span></span>     | <span data-ttu-id="e69a9-186">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-186">NaN</span></span>     |
| <span data-ttu-id="e69a9-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="e69a9-187">**+F**</span></span>             | <span data-ttu-id="e69a9-188">-inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-188">-inf</span></span>     | <span data-ttu-id="e69a9-189">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="e69a9-189">+-F or +-0</span></span> | <span data-ttu-id="e69a9-190">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-190">src0</span></span>        | <span data-ttu-id="e69a9-191">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-191">src0</span></span>   | <span data-ttu-id="e69a9-192">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-192">src0</span></span>   | <span data-ttu-id="e69a9-193">src0</span><span class="sxs-lookup"><span data-stu-id="e69a9-193">src0</span></span>       | <span data-ttu-id="e69a9-194">+F</span><span class="sxs-lookup"><span data-stu-id="e69a9-194">+F</span></span>         | <span data-ttu-id="e69a9-195">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-195">+inf</span></span>     | <span data-ttu-id="e69a9-196">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-196">NaN</span></span>     |
| <span data-ttu-id="e69a9-197">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="e69a9-197">**+inf**</span></span>           | <span data-ttu-id="e69a9-198">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-198">NaN</span></span>      | <span data-ttu-id="e69a9-199">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-199">+inf</span></span>       | <span data-ttu-id="e69a9-200">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-200">+inf</span></span>        | <span data-ttu-id="e69a9-201">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-201">+inf</span></span>   | <span data-ttu-id="e69a9-202">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-202">+inf</span></span>   | <span data-ttu-id="e69a9-203">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-203">+inf</span></span>       | <span data-ttu-id="e69a9-204">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-204">+inf</span></span>       | <span data-ttu-id="e69a9-205">+inf</span><span class="sxs-lookup"><span data-stu-id="e69a9-205">+inf</span></span>     | <span data-ttu-id="e69a9-206">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-206">NaN</span></span>     |
| <span data-ttu-id="e69a9-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e69a9-207">**NaN**</span></span>            | <span data-ttu-id="e69a9-208">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-208">NaN</span></span>      | <span data-ttu-id="e69a9-209">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-209">NaN</span></span>        | <span data-ttu-id="e69a9-210">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-210">NaN</span></span>         | <span data-ttu-id="e69a9-211">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-211">NaN</span></span>    | <span data-ttu-id="e69a9-212">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-212">NaN</span></span>    | <span data-ttu-id="e69a9-213">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-213">NaN</span></span>        | <span data-ttu-id="e69a9-214">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-214">NaN</span></span>        | <span data-ttu-id="e69a9-215">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-215">NaN</span></span>      | <span data-ttu-id="e69a9-216">NaN</span><span class="sxs-lookup"><span data-stu-id="e69a9-216">NaN</span></span>     |



 

<span data-ttu-id="e69a9-217">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e69a9-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e69a9-218">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="e69a9-218">Vertex Shader</span></span> | <span data-ttu-id="e69a9-219">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="e69a9-219">Geometry Shader</span></span> | <span data-ttu-id="e69a9-220">像素著色器</span><span class="sxs-lookup"><span data-stu-id="e69a9-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e69a9-221">x</span><span class="sxs-lookup"><span data-stu-id="e69a9-221">x</span></span>             | <span data-ttu-id="e69a9-222">x</span><span class="sxs-lookup"><span data-stu-id="e69a9-222">x</span></span>               | <span data-ttu-id="e69a9-223">x</span><span class="sxs-lookup"><span data-stu-id="e69a9-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e69a9-224">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e69a9-224">Minimum Shader Model</span></span>

<span data-ttu-id="e69a9-225">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e69a9-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e69a9-226">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e69a9-226">Shader Model</span></span>                                              | <span data-ttu-id="e69a9-227">支援</span><span class="sxs-lookup"><span data-stu-id="e69a9-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e69a9-228">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e69a9-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e69a9-229">是</span><span class="sxs-lookup"><span data-stu-id="e69a9-229">yes</span></span>       |
| [<span data-ttu-id="e69a9-230">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e69a9-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e69a9-231">是</span><span class="sxs-lookup"><span data-stu-id="e69a9-231">yes</span></span>       |
| [<span data-ttu-id="e69a9-232">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e69a9-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e69a9-233">是</span><span class="sxs-lookup"><span data-stu-id="e69a9-233">yes</span></span>       |
| [<span data-ttu-id="e69a9-234">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e69a9-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e69a9-235">否</span><span class="sxs-lookup"><span data-stu-id="e69a9-235">no</span></span>        |
| [<span data-ttu-id="e69a9-236">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e69a9-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e69a9-237">否</span><span class="sxs-lookup"><span data-stu-id="e69a9-237">no</span></span>        |
| [<span data-ttu-id="e69a9-238">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e69a9-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e69a9-239">否</span><span class="sxs-lookup"><span data-stu-id="e69a9-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e69a9-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="e69a9-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e69a9-241">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e69a9-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





