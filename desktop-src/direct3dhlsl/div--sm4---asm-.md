---
title: 'div (sm4-asm) '
description: 元件的細分。
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022814"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="1fcbf-103">div (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="1fcbf-103">div (sm4 - asm)</span></span>

<span data-ttu-id="1fcbf-104">元件的細分。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-104">Component-wise divide.</span></span>



| <span data-ttu-id="1fcbf-105">div \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1fcbf-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1fcbf-106">項目</span><span class="sxs-lookup"><span data-stu-id="1fcbf-106">Item</span></span>                                                            | <span data-ttu-id="1fcbf-107">描述</span><span class="sxs-lookup"><span data-stu-id="1fcbf-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="1fcbf-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="1fcbf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1fcbf-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="1fcbf-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1fcbf-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1fcbf-111">\[被 \] 除數。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="1fcbf-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1fcbf-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1fcbf-113">\[\]除數。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="1fcbf-114">備註</span><span class="sxs-lookup"><span data-stu-id="1fcbf-114">Remarks</span></span>

<span data-ttu-id="1fcbf-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="1fcbf-116">您應該記下兩個允許的除法除法： a/b 和 \* (1/b) 。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="1fcbf-117">其中一個結果是，下表有一些例外狀況，適用于大型分母值 (大於 8.5070592 e + 37) ，其中 1/分母為 denorm。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="1fcbf-118">因為實值可能會以 \* (1/b) （而不是直接）來執行，而且 1/ \[ 大值是可能會排清的 \] denorm，所以資料表中的某些案例會產生不同的結果。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="1fcbf-119">例如， (+/-) INF/ (+/-) \[ 值 > 8.5070592 e + 37 \] 可能在某些實作為上產生 NaN，但在其他執行上 (+/-) INF</span><span class="sxs-lookup"><span data-stu-id="1fcbf-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="1fcbf-120">在此表中，F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="1fcbf-121">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-121">**src0 src1 ->**</span></span> | <span data-ttu-id="1fcbf-122">**-inf**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-122">**-inf**</span></span> | <span data-ttu-id="1fcbf-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-123">**-F**</span></span>     | <span data-ttu-id="1fcbf-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-124">**-denorm**</span></span> | <span data-ttu-id="1fcbf-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-125">**-0**</span></span> | <span data-ttu-id="1fcbf-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-126">**+0**</span></span> | <span data-ttu-id="1fcbf-127">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-127">**+denorm**</span></span> | <span data-ttu-id="1fcbf-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-128">**+F**</span></span>     | <span data-ttu-id="1fcbf-129">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-129">**+inf**</span></span> | <span data-ttu-id="1fcbf-130">**南**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-130">**Nan**</span></span> |
| <span data-ttu-id="1fcbf-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-131">**-inf**</span></span>            | <span data-ttu-id="1fcbf-132">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-132">-inf</span></span>     | <span data-ttu-id="1fcbf-133">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-133">-inf</span></span>       | <span data-ttu-id="1fcbf-134">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-134">-inf</span></span>        | <span data-ttu-id="1fcbf-135">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-135">-inf</span></span>   | <span data-ttu-id="1fcbf-136">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-136">-inf</span></span>   | <span data-ttu-id="1fcbf-137">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-137">-inf</span></span>        | <span data-ttu-id="1fcbf-138">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-138">-inf</span></span>       | <span data-ttu-id="1fcbf-139">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-139">NaN</span></span>      | <span data-ttu-id="1fcbf-140">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-140">NaN</span></span>     |
| <span data-ttu-id="1fcbf-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-141">**-F**</span></span>              | <span data-ttu-id="1fcbf-142">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-142">-inf</span></span>     | <span data-ttu-id="1fcbf-143">-F</span><span class="sxs-lookup"><span data-stu-id="1fcbf-143">-F</span></span>         | <span data-ttu-id="1fcbf-144">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-144">src0</span></span>        | <span data-ttu-id="1fcbf-145">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-145">src0</span></span>   | <span data-ttu-id="1fcbf-146">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-146">src0</span></span>   | <span data-ttu-id="1fcbf-147">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-147">src0</span></span>        | <span data-ttu-id="1fcbf-148">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-148">+-F or +-0</span></span> | <span data-ttu-id="1fcbf-149">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-149">+inf</span></span>     | <span data-ttu-id="1fcbf-150">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-150">NaN</span></span>     |
| <span data-ttu-id="1fcbf-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-151">**-denorm**</span></span>         | <span data-ttu-id="1fcbf-152">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-152">-inf</span></span>     | <span data-ttu-id="1fcbf-153">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-153">src1</span></span>       | <span data-ttu-id="1fcbf-154">-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-154">-0</span></span>          | <span data-ttu-id="1fcbf-155">-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-155">-0</span></span>     | <span data-ttu-id="1fcbf-156">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-156">+0</span></span>     | <span data-ttu-id="1fcbf-157">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-157">+0</span></span>          | <span data-ttu-id="1fcbf-158">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-158">src1</span></span>       | <span data-ttu-id="1fcbf-159">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-159">+inf</span></span>     | <span data-ttu-id="1fcbf-160">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-160">NaN</span></span>     |
| <span data-ttu-id="1fcbf-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-161">**-0**</span></span>              | <span data-ttu-id="1fcbf-162">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-162">-inf</span></span>     | <span data-ttu-id="1fcbf-163">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-163">src1</span></span>       | <span data-ttu-id="1fcbf-164">-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-164">-0</span></span>          | <span data-ttu-id="1fcbf-165">-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-165">-0</span></span>     | <span data-ttu-id="1fcbf-166">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-166">+0</span></span>     | <span data-ttu-id="1fcbf-167">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-167">+0</span></span>          | <span data-ttu-id="1fcbf-168">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-168">src1</span></span>       | <span data-ttu-id="1fcbf-169">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-169">+inf</span></span>     | <span data-ttu-id="1fcbf-170">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-170">NaN</span></span>     |
| <span data-ttu-id="1fcbf-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-171">**+0**</span></span>              | <span data-ttu-id="1fcbf-172">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-172">-inf</span></span>     | <span data-ttu-id="1fcbf-173">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-173">src1</span></span>       | <span data-ttu-id="1fcbf-174">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-174">+0</span></span>          | <span data-ttu-id="1fcbf-175">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-175">+0</span></span>     | <span data-ttu-id="1fcbf-176">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-176">+0</span></span>     | <span data-ttu-id="1fcbf-177">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-177">+0</span></span>          | <span data-ttu-id="1fcbf-178">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-178">src1</span></span>       | <span data-ttu-id="1fcbf-179">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-179">+inf</span></span>     | <span data-ttu-id="1fcbf-180">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-180">NaN</span></span>     |
| <span data-ttu-id="1fcbf-181">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-181">**+denorm**</span></span>         | <span data-ttu-id="1fcbf-182">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-182">-inf</span></span>     | <span data-ttu-id="1fcbf-183">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-183">src1</span></span>       | <span data-ttu-id="1fcbf-184">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-184">+0</span></span>          | <span data-ttu-id="1fcbf-185">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-185">+0</span></span>     | <span data-ttu-id="1fcbf-186">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-186">+0</span></span>     | <span data-ttu-id="1fcbf-187">+0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-187">+0</span></span>          | <span data-ttu-id="1fcbf-188">src1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-188">src1</span></span>       | <span data-ttu-id="1fcbf-189">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-189">+inf</span></span>     | <span data-ttu-id="1fcbf-190">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-190">NaN</span></span>     |
| <span data-ttu-id="1fcbf-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-191">**+F**</span></span>              | <span data-ttu-id="1fcbf-192">-inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-192">-inf</span></span>     | <span data-ttu-id="1fcbf-193">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-193">+-F or +-0</span></span> | <span data-ttu-id="1fcbf-194">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-194">src0</span></span>        | <span data-ttu-id="1fcbf-195">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-195">src0</span></span>   | <span data-ttu-id="1fcbf-196">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-196">src0</span></span>   | <span data-ttu-id="1fcbf-197">src0</span><span class="sxs-lookup"><span data-stu-id="1fcbf-197">src0</span></span>        | <span data-ttu-id="1fcbf-198">+F</span><span class="sxs-lookup"><span data-stu-id="1fcbf-198">+F</span></span>         | <span data-ttu-id="1fcbf-199">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-199">+inf</span></span>     | <span data-ttu-id="1fcbf-200">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-200">NaN</span></span>     |
| <span data-ttu-id="1fcbf-201">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-201">**+inf**</span></span>            | <span data-ttu-id="1fcbf-202">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-202">NaN</span></span>      | <span data-ttu-id="1fcbf-203">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-203">+inf</span></span>       | <span data-ttu-id="1fcbf-204">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-204">+inf</span></span>        | <span data-ttu-id="1fcbf-205">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-205">+inf</span></span>   | <span data-ttu-id="1fcbf-206">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-206">+inf</span></span>   | <span data-ttu-id="1fcbf-207">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-207">+inf</span></span>        | <span data-ttu-id="1fcbf-208">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-208">+inf</span></span>       | <span data-ttu-id="1fcbf-209">+inf</span><span class="sxs-lookup"><span data-stu-id="1fcbf-209">+inf</span></span>     | <span data-ttu-id="1fcbf-210">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-210">NaN</span></span>     |
| <span data-ttu-id="1fcbf-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="1fcbf-211">**NaN**</span></span>             | <span data-ttu-id="1fcbf-212">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-212">NaN</span></span>      | <span data-ttu-id="1fcbf-213">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-213">NaN</span></span>        | <span data-ttu-id="1fcbf-214">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-214">NaN</span></span>         | <span data-ttu-id="1fcbf-215">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-215">NaN</span></span>    | <span data-ttu-id="1fcbf-216">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-216">NaN</span></span>    | <span data-ttu-id="1fcbf-217">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-217">NaN</span></span>         | <span data-ttu-id="1fcbf-218">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-218">NaN</span></span>        | <span data-ttu-id="1fcbf-219">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-219">NaN</span></span>      | <span data-ttu-id="1fcbf-220">NaN</span><span class="sxs-lookup"><span data-stu-id="1fcbf-220">NaN</span></span>     |



 

<span data-ttu-id="1fcbf-221">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1fcbf-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1fcbf-222">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="1fcbf-222">Vertex Shader</span></span> | <span data-ttu-id="1fcbf-223">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="1fcbf-223">Geometry Shader</span></span> | <span data-ttu-id="1fcbf-224">像素著色器</span><span class="sxs-lookup"><span data-stu-id="1fcbf-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1fcbf-225">x</span><span class="sxs-lookup"><span data-stu-id="1fcbf-225">x</span></span>             | <span data-ttu-id="1fcbf-226">x</span><span class="sxs-lookup"><span data-stu-id="1fcbf-226">x</span></span>               | <span data-ttu-id="1fcbf-227">x</span><span class="sxs-lookup"><span data-stu-id="1fcbf-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1fcbf-228">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fcbf-228">Minimum Shader Model</span></span>

<span data-ttu-id="1fcbf-229">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1fcbf-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1fcbf-230">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fcbf-230">Shader Model</span></span>                                              | <span data-ttu-id="1fcbf-231">支援</span><span class="sxs-lookup"><span data-stu-id="1fcbf-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1fcbf-232">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1fcbf-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1fcbf-233">是</span><span class="sxs-lookup"><span data-stu-id="1fcbf-233">yes</span></span>       |
| [<span data-ttu-id="1fcbf-234">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1fcbf-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1fcbf-235">是</span><span class="sxs-lookup"><span data-stu-id="1fcbf-235">yes</span></span>       |
| [<span data-ttu-id="1fcbf-236">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1fcbf-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1fcbf-237">是</span><span class="sxs-lookup"><span data-stu-id="1fcbf-237">yes</span></span>       |
| [<span data-ttu-id="1fcbf-238">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fcbf-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1fcbf-239">不可以</span><span class="sxs-lookup"><span data-stu-id="1fcbf-239">no</span></span>        |
| [<span data-ttu-id="1fcbf-240">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fcbf-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1fcbf-241">不可以</span><span class="sxs-lookup"><span data-stu-id="1fcbf-241">no</span></span>        |
| [<span data-ttu-id="1fcbf-242">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fcbf-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1fcbf-243">不可以</span><span class="sxs-lookup"><span data-stu-id="1fcbf-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1fcbf-244">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fcbf-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fcbf-245">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fcbf-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





