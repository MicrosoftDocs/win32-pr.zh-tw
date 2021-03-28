---
title: 'dmul (sm5-asm) '
description: 元件的雙精確度乘積。
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990750"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="0a312-103">dmul (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="0a312-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="0a312-104">元件的雙精確度乘積。</span><span class="sxs-lookup"><span data-stu-id="0a312-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="0a312-105">dmul \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0a312-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0a312-106">項目</span><span class="sxs-lookup"><span data-stu-id="0a312-106">Item</span></span>                                                            | <span data-ttu-id="0a312-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a312-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a312-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="0a312-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0a312-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="0a312-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="0a312-110">*目的地*  = *src0* \**src1*</span><span class="sxs-lookup"><span data-stu-id="0a312-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="0a312-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0a312-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0a312-112">\[在 \] 要與 *src1* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="0a312-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="0a312-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0a312-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0a312-114">\[在 \] 要與 *src0* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="0a312-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="0a312-115">備註</span><span class="sxs-lookup"><span data-stu-id="0a312-115">Remarks</span></span>

<span data-ttu-id="0a312-116">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="0a312-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="0a312-117">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="0a312-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="0a312-118">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="0a312-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="0a312-119">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="0a312-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="0a312-120">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="0a312-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="0a312-121">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="0a312-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="0a312-122">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="0a312-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="0a312-123">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="0a312-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="0a312-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="0a312-124">**src0 src1->**</span></span> | <span data-ttu-id="0a312-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="0a312-125">**-inf**</span></span> | <span data-ttu-id="0a312-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="0a312-126">**-F**</span></span> | <span data-ttu-id="0a312-127">**-1。0**</span><span class="sxs-lookup"><span data-stu-id="0a312-127">**-1.0**</span></span> | <span data-ttu-id="0a312-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="0a312-128">**-0**</span></span> | <span data-ttu-id="0a312-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="0a312-129">**+0**</span></span> | <span data-ttu-id="0a312-130">**+ 1。0**</span><span class="sxs-lookup"><span data-stu-id="0a312-130">**+1.0**</span></span> | <span data-ttu-id="0a312-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0a312-131">**+F**</span></span> | <span data-ttu-id="0a312-132">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="0a312-132">**+inf**</span></span> | <span data-ttu-id="0a312-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0a312-133">**NaN**</span></span> |
| <span data-ttu-id="0a312-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="0a312-134">**-inf**</span></span>           | <span data-ttu-id="0a312-135">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-135">+inf</span></span>     | <span data-ttu-id="0a312-136">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-136">+inf</span></span>   | <span data-ttu-id="0a312-137">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-137">+inf</span></span>     | <span data-ttu-id="0a312-138">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-138">NaN</span></span>    | <span data-ttu-id="0a312-139">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-139">NaN</span></span>    | <span data-ttu-id="0a312-140">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-140">-inf</span></span>     | <span data-ttu-id="0a312-141">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-141">-inf</span></span>   | <span data-ttu-id="0a312-142">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-142">-inf</span></span>     | <span data-ttu-id="0a312-143">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-143">NaN</span></span>     |
| <span data-ttu-id="0a312-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="0a312-144">**-F**</span></span>             | <span data-ttu-id="0a312-145">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-145">+inf</span></span>     | <span data-ttu-id="0a312-146">+F</span><span class="sxs-lookup"><span data-stu-id="0a312-146">+F</span></span>     | <span data-ttu-id="0a312-147">-src0</span><span class="sxs-lookup"><span data-stu-id="0a312-147">-src0</span></span>    | <span data-ttu-id="0a312-148">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-148">+0</span></span>     | <span data-ttu-id="0a312-149">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-149">-0</span></span>     | <span data-ttu-id="0a312-150">src0</span><span class="sxs-lookup"><span data-stu-id="0a312-150">src0</span></span>     | <span data-ttu-id="0a312-151">-F</span><span class="sxs-lookup"><span data-stu-id="0a312-151">-F</span></span>     | <span data-ttu-id="0a312-152">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-152">-inf</span></span>     | <span data-ttu-id="0a312-153">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-153">NaN</span></span>     |
| <span data-ttu-id="0a312-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="0a312-154">**-1.0F**</span></span>          | <span data-ttu-id="0a312-155">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-155">+inf</span></span>     | <span data-ttu-id="0a312-156">-src1</span><span class="sxs-lookup"><span data-stu-id="0a312-156">-src1</span></span>  | <span data-ttu-id="0a312-157">+ 1。0</span><span class="sxs-lookup"><span data-stu-id="0a312-157">+1.0</span></span>     | <span data-ttu-id="0a312-158">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-158">+0</span></span>     | <span data-ttu-id="0a312-159">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-159">-0</span></span>     | <span data-ttu-id="0a312-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="0a312-160">-1.0</span></span>     | <span data-ttu-id="0a312-161">-src1</span><span class="sxs-lookup"><span data-stu-id="0a312-161">-src1</span></span>  | <span data-ttu-id="0a312-162">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-162">-inf</span></span>     | <span data-ttu-id="0a312-163">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-163">NaN</span></span>     |
| <span data-ttu-id="0a312-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="0a312-164">**-0**</span></span>             | <span data-ttu-id="0a312-165">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-165">NaN</span></span>      | <span data-ttu-id="0a312-166">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-166">+0</span></span>     | <span data-ttu-id="0a312-167">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-167">+0</span></span>       | <span data-ttu-id="0a312-168">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-168">+0</span></span>     | <span data-ttu-id="0a312-169">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-169">-0</span></span>     | <span data-ttu-id="0a312-170">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-170">-0</span></span>       | <span data-ttu-id="0a312-171">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-171">-0</span></span>     | <span data-ttu-id="0a312-172">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-172">NaN</span></span>      | <span data-ttu-id="0a312-173">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-173">NaN</span></span>     |
| <span data-ttu-id="0a312-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="0a312-174">**+0**</span></span>             | <span data-ttu-id="0a312-175">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-175">NaN</span></span>      | <span data-ttu-id="0a312-176">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-176">-0</span></span>     | <span data-ttu-id="0a312-177">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-177">-0</span></span>       | <span data-ttu-id="0a312-178">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-178">-0</span></span>     | <span data-ttu-id="0a312-179">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-179">+0</span></span>     | <span data-ttu-id="0a312-180">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-180">+0</span></span>       | <span data-ttu-id="0a312-181">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-181">+0</span></span>     | <span data-ttu-id="0a312-182">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-182">NaN</span></span>      | <span data-ttu-id="0a312-183">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-183">NaN</span></span>     |
| <span data-ttu-id="0a312-184">**+ 1。0**</span><span class="sxs-lookup"><span data-stu-id="0a312-184">**+1.0**</span></span>           | <span data-ttu-id="0a312-185">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-185">-inf</span></span>     | <span data-ttu-id="0a312-186">src1</span><span class="sxs-lookup"><span data-stu-id="0a312-186">src1</span></span>   | <span data-ttu-id="0a312-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="0a312-187">-1.0</span></span>     | <span data-ttu-id="0a312-188">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-188">-0</span></span>     | <span data-ttu-id="0a312-189">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-189">+0</span></span>     | <span data-ttu-id="0a312-190">+1</span><span class="sxs-lookup"><span data-stu-id="0a312-190">+1</span></span>       | <span data-ttu-id="0a312-191">src1</span><span class="sxs-lookup"><span data-stu-id="0a312-191">src1</span></span>   | <span data-ttu-id="0a312-192">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-192">+inf</span></span>     | <span data-ttu-id="0a312-193">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-193">NaN</span></span>     |
| <span data-ttu-id="0a312-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0a312-194">**+F**</span></span>             | <span data-ttu-id="0a312-195">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-195">-inf</span></span>     | <span data-ttu-id="0a312-196">-F</span><span class="sxs-lookup"><span data-stu-id="0a312-196">-F</span></span>     | <span data-ttu-id="0a312-197">-src0</span><span class="sxs-lookup"><span data-stu-id="0a312-197">-src0</span></span>    | <span data-ttu-id="0a312-198">-0</span><span class="sxs-lookup"><span data-stu-id="0a312-198">-0</span></span>     | <span data-ttu-id="0a312-199">+0</span><span class="sxs-lookup"><span data-stu-id="0a312-199">+0</span></span>     | <span data-ttu-id="0a312-200">src0</span><span class="sxs-lookup"><span data-stu-id="0a312-200">src0</span></span>     | <span data-ttu-id="0a312-201">+F</span><span class="sxs-lookup"><span data-stu-id="0a312-201">+F</span></span>     | <span data-ttu-id="0a312-202">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-202">+inf</span></span>     | <span data-ttu-id="0a312-203">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-203">NaN</span></span>     |
| <span data-ttu-id="0a312-204">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="0a312-204">**+inf**</span></span>           | <span data-ttu-id="0a312-205">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-205">-inf</span></span>     | <span data-ttu-id="0a312-206">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-206">-inf</span></span>   | <span data-ttu-id="0a312-207">-inf</span><span class="sxs-lookup"><span data-stu-id="0a312-207">-inf</span></span>     | <span data-ttu-id="0a312-208">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-208">NaN</span></span>    | <span data-ttu-id="0a312-209">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-209">NaN</span></span>    | <span data-ttu-id="0a312-210">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-210">+inf</span></span>     | <span data-ttu-id="0a312-211">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-211">+inf</span></span>   | <span data-ttu-id="0a312-212">+inf</span><span class="sxs-lookup"><span data-stu-id="0a312-212">+inf</span></span>     | <span data-ttu-id="0a312-213">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-213">NaN</span></span>     |
| <span data-ttu-id="0a312-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0a312-214">**NaN**</span></span>            | <span data-ttu-id="0a312-215">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-215">NaN</span></span>      | <span data-ttu-id="0a312-216">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-216">NaN</span></span>    | <span data-ttu-id="0a312-217">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-217">NaN</span></span>      | <span data-ttu-id="0a312-218">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-218">NaN</span></span>    | <span data-ttu-id="0a312-219">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-219">NaN</span></span>    | <span data-ttu-id="0a312-220">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-220">NaN</span></span>      | <span data-ttu-id="0a312-221">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-221">NaN</span></span>    | <span data-ttu-id="0a312-222">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-222">NaN</span></span>      | <span data-ttu-id="0a312-223">NaN</span><span class="sxs-lookup"><span data-stu-id="0a312-223">NaN</span></span>     |



 

<span data-ttu-id="0a312-224">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="0a312-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0a312-225">頂點</span><span class="sxs-lookup"><span data-stu-id="0a312-225">Vertex</span></span> | <span data-ttu-id="0a312-226">船體</span><span class="sxs-lookup"><span data-stu-id="0a312-226">Hull</span></span> | <span data-ttu-id="0a312-227">網域</span><span class="sxs-lookup"><span data-stu-id="0a312-227">Domain</span></span> | <span data-ttu-id="0a312-228">幾何</span><span class="sxs-lookup"><span data-stu-id="0a312-228">Geometry</span></span> | <span data-ttu-id="0a312-229">像素</span><span class="sxs-lookup"><span data-stu-id="0a312-229">Pixel</span></span> | <span data-ttu-id="0a312-230">計算</span><span class="sxs-lookup"><span data-stu-id="0a312-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0a312-231">X</span><span class="sxs-lookup"><span data-stu-id="0a312-231">X</span></span>      | <span data-ttu-id="0a312-232">X</span><span class="sxs-lookup"><span data-stu-id="0a312-232">X</span></span>    | <span data-ttu-id="0a312-233">X</span><span class="sxs-lookup"><span data-stu-id="0a312-233">X</span></span>      | <span data-ttu-id="0a312-234">X</span><span class="sxs-lookup"><span data-stu-id="0a312-234">X</span></span>        | <span data-ttu-id="0a312-235">X</span><span class="sxs-lookup"><span data-stu-id="0a312-235">X</span></span>     | <span data-ttu-id="0a312-236">X</span><span class="sxs-lookup"><span data-stu-id="0a312-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0a312-237">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a312-237">Minimum Shader Model</span></span>

<span data-ttu-id="0a312-238">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="0a312-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0a312-239">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a312-239">Shader Model</span></span>                                              | <span data-ttu-id="0a312-240">支援</span><span class="sxs-lookup"><span data-stu-id="0a312-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0a312-241">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0a312-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0a312-242">是</span><span class="sxs-lookup"><span data-stu-id="0a312-242">yes</span></span>       |
| [<span data-ttu-id="0a312-243">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="0a312-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0a312-244">不可以</span><span class="sxs-lookup"><span data-stu-id="0a312-244">no</span></span>        |
| [<span data-ttu-id="0a312-245">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="0a312-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0a312-246">不可以</span><span class="sxs-lookup"><span data-stu-id="0a312-246">no</span></span>        |
| [<span data-ttu-id="0a312-247">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a312-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0a312-248">不可以</span><span class="sxs-lookup"><span data-stu-id="0a312-248">no</span></span>        |
| [<span data-ttu-id="0a312-249">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a312-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0a312-250">不可以</span><span class="sxs-lookup"><span data-stu-id="0a312-250">no</span></span>        |
| [<span data-ttu-id="0a312-251">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a312-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0a312-252">不可以</span><span class="sxs-lookup"><span data-stu-id="0a312-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0a312-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a312-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a312-254">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a312-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





