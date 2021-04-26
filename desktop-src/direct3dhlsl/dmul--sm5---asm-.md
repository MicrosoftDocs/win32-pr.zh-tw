---
title: 'dmul (sm5-asm) '
description: 元件的雙精確度乘積。
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999085"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="eaa29-103">dmul (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="eaa29-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="eaa29-104">元件的雙精確度乘積。</span><span class="sxs-lookup"><span data-stu-id="eaa29-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="eaa29-105">dmul \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="eaa29-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eaa29-106">項目</span><span class="sxs-lookup"><span data-stu-id="eaa29-106">Item</span></span>                                                            | <span data-ttu-id="eaa29-107">描述</span><span class="sxs-lookup"><span data-stu-id="eaa29-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa29-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="eaa29-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eaa29-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="eaa29-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="eaa29-110">*目的地*  = *src0* \**src1*</span><span class="sxs-lookup"><span data-stu-id="eaa29-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="eaa29-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eaa29-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eaa29-112">\[在 \] 要與 *src1* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="eaa29-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="eaa29-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="eaa29-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eaa29-114">\[在 \] 要與 *src0* 相乘的元件中。</span><span class="sxs-lookup"><span data-stu-id="eaa29-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="eaa29-115">備註</span><span class="sxs-lookup"><span data-stu-id="eaa29-115">Remarks</span></span>

<span data-ttu-id="eaa29-116">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="eaa29-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="eaa29-117">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="eaa29-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="eaa29-118">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="eaa29-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="eaa29-119">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="eaa29-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="eaa29-120">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="eaa29-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="eaa29-121">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="eaa29-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="eaa29-122">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="eaa29-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="eaa29-123">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="eaa29-123">F means finite-real number.</span></span>



| <span data-ttu-id="eaa29-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="eaa29-124">**src0 src1->**</span></span> | <span data-ttu-id="eaa29-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="eaa29-125">**-inf**</span></span> | <span data-ttu-id="eaa29-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="eaa29-126">**-F**</span></span> | <span data-ttu-id="eaa29-127">**-1。0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-127">**-1.0**</span></span> | <span data-ttu-id="eaa29-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-128">**-0**</span></span> | <span data-ttu-id="eaa29-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-129">**+0**</span></span> | <span data-ttu-id="eaa29-130">**+ 1。0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-130">**+1.0**</span></span> | <span data-ttu-id="eaa29-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="eaa29-131">**+F**</span></span> | <span data-ttu-id="eaa29-132">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="eaa29-132">**+inf**</span></span> | <span data-ttu-id="eaa29-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eaa29-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="eaa29-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="eaa29-134">**-inf**</span></span>           | <span data-ttu-id="eaa29-135">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-135">+inf</span></span>     | <span data-ttu-id="eaa29-136">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-136">+inf</span></span>   | <span data-ttu-id="eaa29-137">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-137">+inf</span></span>     | <span data-ttu-id="eaa29-138">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-138">NaN</span></span>    | <span data-ttu-id="eaa29-139">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-139">NaN</span></span>    | <span data-ttu-id="eaa29-140">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-140">-inf</span></span>     | <span data-ttu-id="eaa29-141">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-141">-inf</span></span>   | <span data-ttu-id="eaa29-142">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-142">-inf</span></span>     | <span data-ttu-id="eaa29-143">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-143">NaN</span></span>     |
| <span data-ttu-id="eaa29-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="eaa29-144">**-F**</span></span>             | <span data-ttu-id="eaa29-145">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-145">+inf</span></span>     | <span data-ttu-id="eaa29-146">+F</span><span class="sxs-lookup"><span data-stu-id="eaa29-146">+F</span></span>     | <span data-ttu-id="eaa29-147">-src0</span><span class="sxs-lookup"><span data-stu-id="eaa29-147">-src0</span></span>    | <span data-ttu-id="eaa29-148">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-148">+0</span></span>     | <span data-ttu-id="eaa29-149">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-149">-0</span></span>     | <span data-ttu-id="eaa29-150">src0</span><span class="sxs-lookup"><span data-stu-id="eaa29-150">src0</span></span>     | <span data-ttu-id="eaa29-151">-F</span><span class="sxs-lookup"><span data-stu-id="eaa29-151">-F</span></span>     | <span data-ttu-id="eaa29-152">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-152">-inf</span></span>     | <span data-ttu-id="eaa29-153">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-153">NaN</span></span>     |
| <span data-ttu-id="eaa29-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="eaa29-154">**-1.0F**</span></span>          | <span data-ttu-id="eaa29-155">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-155">+inf</span></span>     | <span data-ttu-id="eaa29-156">-src1</span><span class="sxs-lookup"><span data-stu-id="eaa29-156">-src1</span></span>  | <span data-ttu-id="eaa29-157">+ 1。0</span><span class="sxs-lookup"><span data-stu-id="eaa29-157">+1.0</span></span>     | <span data-ttu-id="eaa29-158">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-158">+0</span></span>     | <span data-ttu-id="eaa29-159">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-159">-0</span></span>     | <span data-ttu-id="eaa29-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="eaa29-160">-1.0</span></span>     | <span data-ttu-id="eaa29-161">-src1</span><span class="sxs-lookup"><span data-stu-id="eaa29-161">-src1</span></span>  | <span data-ttu-id="eaa29-162">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-162">-inf</span></span>     | <span data-ttu-id="eaa29-163">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-163">NaN</span></span>     |
| <span data-ttu-id="eaa29-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-164">**-0**</span></span>             | <span data-ttu-id="eaa29-165">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-165">NaN</span></span>      | <span data-ttu-id="eaa29-166">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-166">+0</span></span>     | <span data-ttu-id="eaa29-167">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-167">+0</span></span>       | <span data-ttu-id="eaa29-168">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-168">+0</span></span>     | <span data-ttu-id="eaa29-169">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-169">-0</span></span>     | <span data-ttu-id="eaa29-170">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-170">-0</span></span>       | <span data-ttu-id="eaa29-171">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-171">-0</span></span>     | <span data-ttu-id="eaa29-172">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-172">NaN</span></span>      | <span data-ttu-id="eaa29-173">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-173">NaN</span></span>     |
| <span data-ttu-id="eaa29-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-174">**+0**</span></span>             | <span data-ttu-id="eaa29-175">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-175">NaN</span></span>      | <span data-ttu-id="eaa29-176">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-176">-0</span></span>     | <span data-ttu-id="eaa29-177">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-177">-0</span></span>       | <span data-ttu-id="eaa29-178">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-178">-0</span></span>     | <span data-ttu-id="eaa29-179">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-179">+0</span></span>     | <span data-ttu-id="eaa29-180">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-180">+0</span></span>       | <span data-ttu-id="eaa29-181">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-181">+0</span></span>     | <span data-ttu-id="eaa29-182">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-182">NaN</span></span>      | <span data-ttu-id="eaa29-183">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-183">NaN</span></span>     |
| <span data-ttu-id="eaa29-184">**+ 1。0**</span><span class="sxs-lookup"><span data-stu-id="eaa29-184">**+1.0**</span></span>           | <span data-ttu-id="eaa29-185">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-185">-inf</span></span>     | <span data-ttu-id="eaa29-186">src1</span><span class="sxs-lookup"><span data-stu-id="eaa29-186">src1</span></span>   | <span data-ttu-id="eaa29-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="eaa29-187">-1.0</span></span>     | <span data-ttu-id="eaa29-188">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-188">-0</span></span>     | <span data-ttu-id="eaa29-189">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-189">+0</span></span>     | <span data-ttu-id="eaa29-190">+1</span><span class="sxs-lookup"><span data-stu-id="eaa29-190">+1</span></span>       | <span data-ttu-id="eaa29-191">src1</span><span class="sxs-lookup"><span data-stu-id="eaa29-191">src1</span></span>   | <span data-ttu-id="eaa29-192">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-192">+inf</span></span>     | <span data-ttu-id="eaa29-193">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-193">NaN</span></span>     |
| <span data-ttu-id="eaa29-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="eaa29-194">**+F**</span></span>             | <span data-ttu-id="eaa29-195">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-195">-inf</span></span>     | <span data-ttu-id="eaa29-196">-F</span><span class="sxs-lookup"><span data-stu-id="eaa29-196">-F</span></span>     | <span data-ttu-id="eaa29-197">-src0</span><span class="sxs-lookup"><span data-stu-id="eaa29-197">-src0</span></span>    | <span data-ttu-id="eaa29-198">-0</span><span class="sxs-lookup"><span data-stu-id="eaa29-198">-0</span></span>     | <span data-ttu-id="eaa29-199">+0</span><span class="sxs-lookup"><span data-stu-id="eaa29-199">+0</span></span>     | <span data-ttu-id="eaa29-200">src0</span><span class="sxs-lookup"><span data-stu-id="eaa29-200">src0</span></span>     | <span data-ttu-id="eaa29-201">+F</span><span class="sxs-lookup"><span data-stu-id="eaa29-201">+F</span></span>     | <span data-ttu-id="eaa29-202">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-202">+inf</span></span>     | <span data-ttu-id="eaa29-203">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-203">NaN</span></span>     |
| <span data-ttu-id="eaa29-204">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="eaa29-204">**+inf**</span></span>           | <span data-ttu-id="eaa29-205">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-205">-inf</span></span>     | <span data-ttu-id="eaa29-206">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-206">-inf</span></span>   | <span data-ttu-id="eaa29-207">-inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-207">-inf</span></span>     | <span data-ttu-id="eaa29-208">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-208">NaN</span></span>    | <span data-ttu-id="eaa29-209">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-209">NaN</span></span>    | <span data-ttu-id="eaa29-210">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-210">+inf</span></span>     | <span data-ttu-id="eaa29-211">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-211">+inf</span></span>   | <span data-ttu-id="eaa29-212">+inf</span><span class="sxs-lookup"><span data-stu-id="eaa29-212">+inf</span></span>     | <span data-ttu-id="eaa29-213">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-213">NaN</span></span>     |
| <span data-ttu-id="eaa29-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eaa29-214">**NaN**</span></span>            | <span data-ttu-id="eaa29-215">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-215">NaN</span></span>      | <span data-ttu-id="eaa29-216">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-216">NaN</span></span>    | <span data-ttu-id="eaa29-217">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-217">NaN</span></span>      | <span data-ttu-id="eaa29-218">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-218">NaN</span></span>    | <span data-ttu-id="eaa29-219">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-219">NaN</span></span>    | <span data-ttu-id="eaa29-220">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-220">NaN</span></span>      | <span data-ttu-id="eaa29-221">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-221">NaN</span></span>    | <span data-ttu-id="eaa29-222">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-222">NaN</span></span>      | <span data-ttu-id="eaa29-223">NaN</span><span class="sxs-lookup"><span data-stu-id="eaa29-223">NaN</span></span>     |



 

<span data-ttu-id="eaa29-224">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="eaa29-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eaa29-225">頂點</span><span class="sxs-lookup"><span data-stu-id="eaa29-225">Vertex</span></span> | <span data-ttu-id="eaa29-226">船體</span><span class="sxs-lookup"><span data-stu-id="eaa29-226">Hull</span></span> | <span data-ttu-id="eaa29-227">網域</span><span class="sxs-lookup"><span data-stu-id="eaa29-227">Domain</span></span> | <span data-ttu-id="eaa29-228">幾何</span><span class="sxs-lookup"><span data-stu-id="eaa29-228">Geometry</span></span> | <span data-ttu-id="eaa29-229">像素</span><span class="sxs-lookup"><span data-stu-id="eaa29-229">Pixel</span></span> | <span data-ttu-id="eaa29-230">計算</span><span class="sxs-lookup"><span data-stu-id="eaa29-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eaa29-231">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-231">X</span></span>      | <span data-ttu-id="eaa29-232">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-232">X</span></span>    | <span data-ttu-id="eaa29-233">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-233">X</span></span>      | <span data-ttu-id="eaa29-234">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-234">X</span></span>        | <span data-ttu-id="eaa29-235">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-235">X</span></span>     | <span data-ttu-id="eaa29-236">X</span><span class="sxs-lookup"><span data-stu-id="eaa29-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eaa29-237">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="eaa29-237">Minimum Shader Model</span></span>

<span data-ttu-id="eaa29-238">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="eaa29-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eaa29-239">著色器模型</span><span class="sxs-lookup"><span data-stu-id="eaa29-239">Shader Model</span></span>                                              | <span data-ttu-id="eaa29-240">支援</span><span class="sxs-lookup"><span data-stu-id="eaa29-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eaa29-241">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="eaa29-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eaa29-242">是</span><span class="sxs-lookup"><span data-stu-id="eaa29-242">yes</span></span>       |
| [<span data-ttu-id="eaa29-243">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="eaa29-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eaa29-244">否</span><span class="sxs-lookup"><span data-stu-id="eaa29-244">no</span></span>        |
| [<span data-ttu-id="eaa29-245">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="eaa29-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eaa29-246">否</span><span class="sxs-lookup"><span data-stu-id="eaa29-246">no</span></span>        |
| [<span data-ttu-id="eaa29-247">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eaa29-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eaa29-248">否</span><span class="sxs-lookup"><span data-stu-id="eaa29-248">no</span></span>        |
| [<span data-ttu-id="eaa29-249">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eaa29-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eaa29-250">否</span><span class="sxs-lookup"><span data-stu-id="eaa29-250">no</span></span>        |
| [<span data-ttu-id="eaa29-251">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eaa29-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eaa29-252">否</span><span class="sxs-lookup"><span data-stu-id="eaa29-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eaa29-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="eaa29-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa29-254">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eaa29-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





