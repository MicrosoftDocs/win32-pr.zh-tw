---
title: 'dadd (sm5-asm) '
description: 元件的雙精度浮點數相加。
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373718"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="96120-103">dadd (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="96120-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="96120-104">元件的雙精度浮點數相加。</span><span class="sxs-lookup"><span data-stu-id="96120-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="96120-105">dadd \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="96120-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="96120-106">項目</span><span class="sxs-lookup"><span data-stu-id="96120-106">Item</span></span>                                                            | <span data-ttu-id="96120-107">描述</span><span class="sxs-lookup"><span data-stu-id="96120-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="96120-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="96120-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="96120-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="96120-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="96120-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="96120-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="96120-111">\[在 \] 要以 *src1* 新增的元件中。</span><span class="sxs-lookup"><span data-stu-id="96120-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="96120-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="96120-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="96120-113">\[在 \] 要以 *src0* 新增的元件中</span><span class="sxs-lookup"><span data-stu-id="96120-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="96120-114">備註</span><span class="sxs-lookup"><span data-stu-id="96120-114">Remarks</span></span>

<span data-ttu-id="96120-115">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="96120-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="96120-116">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="96120-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="96120-117">下列是 swizzle 後的對應：</span><span class="sxs-lookup"><span data-stu-id="96120-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="96120-118">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="96120-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="96120-119">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="96120-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="96120-120">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="96120-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="96120-121">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="96120-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="96120-122">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="96120-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="96120-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="96120-123"><strong>src0</strong></span></span><br /><span data-ttu-id="96120-124">
<strong>src1-></strong></span><span class="sxs-lookup"><span data-stu-id="96120-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="96120-125"><strong>-inf</strong></span><span class="sxs-lookup"><span data-stu-id="96120-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="96120-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="96120-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="96120-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="96120-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="96120-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="96120-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="96120-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="96120-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="96120-130"><strong>+ inf</strong></span><span class="sxs-lookup"><span data-stu-id="96120-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="96120-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="96120-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96120-132"><strong>-inf</strong></span><span class="sxs-lookup"><span data-stu-id="96120-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="96120-133">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-133">-inf</span></span></td>
<td><span data-ttu-id="96120-134">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-134">-inf</span></span></td>
<td><span data-ttu-id="96120-135">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-135">-inf</span></span></td>
<td><span data-ttu-id="96120-136">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-136">-inf</span></span></td>
<td><span data-ttu-id="96120-137">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-137">-inf</span></span></td>
<td><span data-ttu-id="96120-138">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-138">NaN</span></span></td>
<td><span data-ttu-id="96120-139">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96120-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="96120-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="96120-141">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-141">-inf</span></span></td>
<td><span data-ttu-id="96120-142">-F</span><span class="sxs-lookup"><span data-stu-id="96120-142">-F</span></span></td>
<td><span data-ttu-id="96120-143">src0</span><span class="sxs-lookup"><span data-stu-id="96120-143">src0</span></span></td>
<td><span data-ttu-id="96120-144">src0</span><span class="sxs-lookup"><span data-stu-id="96120-144">src0</span></span></td>
<td><span data-ttu-id="96120-145">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="96120-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="96120-146">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-146">+inf</span></span></td>
<td><span data-ttu-id="96120-147">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96120-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="96120-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="96120-149">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-149">-inf</span></span></td>
<td><span data-ttu-id="96120-150">src1</span><span class="sxs-lookup"><span data-stu-id="96120-150">src1</span></span></td>
<td><span data-ttu-id="96120-151">-0</span><span class="sxs-lookup"><span data-stu-id="96120-151">-0</span></span></td>
<td><span data-ttu-id="96120-152">+0</span><span class="sxs-lookup"><span data-stu-id="96120-152">+0</span></span></td>
<td><span data-ttu-id="96120-153">src1</span><span class="sxs-lookup"><span data-stu-id="96120-153">src1</span></span></td>
<td><span data-ttu-id="96120-154">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-154">+inf</span></span></td>
<td><span data-ttu-id="96120-155">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96120-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="96120-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="96120-157">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-157">-inf</span></span></td>
<td><span data-ttu-id="96120-158">src1</span><span class="sxs-lookup"><span data-stu-id="96120-158">src1</span></span></td>
<td><span data-ttu-id="96120-159">+0</span><span class="sxs-lookup"><span data-stu-id="96120-159">+0</span></span></td>
<td><span data-ttu-id="96120-160">+0</span><span class="sxs-lookup"><span data-stu-id="96120-160">+0</span></span></td>
<td><span data-ttu-id="96120-161">src1</span><span class="sxs-lookup"><span data-stu-id="96120-161">src1</span></span></td>
<td><span data-ttu-id="96120-162">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-162">+inf</span></span></td>
<td><span data-ttu-id="96120-163">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96120-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="96120-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="96120-165">-inf</span><span class="sxs-lookup"><span data-stu-id="96120-165">-inf</span></span></td>
<td><span data-ttu-id="96120-166">+-F 或 +-0</span><span class="sxs-lookup"><span data-stu-id="96120-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="96120-167">src0</span><span class="sxs-lookup"><span data-stu-id="96120-167">src0</span></span></td>
<td><span data-ttu-id="96120-168">src0</span><span class="sxs-lookup"><span data-stu-id="96120-168">src0</span></span></td>
<td><span data-ttu-id="96120-169">+F</span><span class="sxs-lookup"><span data-stu-id="96120-169">+F</span></span></td>
<td><span data-ttu-id="96120-170">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-170">+inf</span></span></td>
<td><span data-ttu-id="96120-171">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96120-172"><strong>+ inf</strong></span><span class="sxs-lookup"><span data-stu-id="96120-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="96120-173">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-173">NaN</span></span></td>
<td><span data-ttu-id="96120-174">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-174">+inf</span></span></td>
<td><span data-ttu-id="96120-175">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-175">+inf</span></span></td>
<td><span data-ttu-id="96120-176">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-176">+inf</span></span></td>
<td><span data-ttu-id="96120-177">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-177">+inf</span></span></td>
<td><span data-ttu-id="96120-178">+inf</span><span class="sxs-lookup"><span data-stu-id="96120-178">+inf</span></span></td>
<td><span data-ttu-id="96120-179">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96120-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="96120-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="96120-181">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-181">NaN</span></span></td>
<td><span data-ttu-id="96120-182">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-182">NaN</span></span></td>
<td><span data-ttu-id="96120-183">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-183">NaN</span></span></td>
<td><span data-ttu-id="96120-184">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-184">NaN</span></span></td>
<td><span data-ttu-id="96120-185">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-185">NaN</span></span></td>
<td><span data-ttu-id="96120-186">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-186">NaN</span></span></td>
<td><span data-ttu-id="96120-187">NaN</span><span class="sxs-lookup"><span data-stu-id="96120-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="96120-188">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="96120-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="96120-189">頂點</span><span class="sxs-lookup"><span data-stu-id="96120-189">Vertex</span></span> | <span data-ttu-id="96120-190">船體</span><span class="sxs-lookup"><span data-stu-id="96120-190">Hull</span></span> | <span data-ttu-id="96120-191">網域</span><span class="sxs-lookup"><span data-stu-id="96120-191">Domain</span></span> | <span data-ttu-id="96120-192">幾何</span><span class="sxs-lookup"><span data-stu-id="96120-192">Geometry</span></span> | <span data-ttu-id="96120-193">像素</span><span class="sxs-lookup"><span data-stu-id="96120-193">Pixel</span></span> | <span data-ttu-id="96120-194">計算</span><span class="sxs-lookup"><span data-stu-id="96120-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="96120-195">X</span><span class="sxs-lookup"><span data-stu-id="96120-195">X</span></span>      | <span data-ttu-id="96120-196">X</span><span class="sxs-lookup"><span data-stu-id="96120-196">X</span></span>    | <span data-ttu-id="96120-197">X</span><span class="sxs-lookup"><span data-stu-id="96120-197">X</span></span>      | <span data-ttu-id="96120-198">X</span><span class="sxs-lookup"><span data-stu-id="96120-198">X</span></span>        | <span data-ttu-id="96120-199">X</span><span class="sxs-lookup"><span data-stu-id="96120-199">X</span></span>     | <span data-ttu-id="96120-200">X</span><span class="sxs-lookup"><span data-stu-id="96120-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="96120-201">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="96120-201">Minimum Shader Model</span></span>

<span data-ttu-id="96120-202">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="96120-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="96120-203">著色器模型</span><span class="sxs-lookup"><span data-stu-id="96120-203">Shader Model</span></span>                                              | <span data-ttu-id="96120-204">支援</span><span class="sxs-lookup"><span data-stu-id="96120-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="96120-205">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="96120-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="96120-206">是</span><span class="sxs-lookup"><span data-stu-id="96120-206">yes</span></span>       |
| [<span data-ttu-id="96120-207">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="96120-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="96120-208">不可以</span><span class="sxs-lookup"><span data-stu-id="96120-208">no</span></span>        |
| [<span data-ttu-id="96120-209">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="96120-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="96120-210">不可以</span><span class="sxs-lookup"><span data-stu-id="96120-210">no</span></span>        |
| [<span data-ttu-id="96120-211">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="96120-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="96120-212">不可以</span><span class="sxs-lookup"><span data-stu-id="96120-212">no</span></span>        |
| [<span data-ttu-id="96120-213">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="96120-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="96120-214">不可以</span><span class="sxs-lookup"><span data-stu-id="96120-214">no</span></span>        |
| [<span data-ttu-id="96120-215">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="96120-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="96120-216">不可以</span><span class="sxs-lookup"><span data-stu-id="96120-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="96120-217">相關主題</span><span class="sxs-lookup"><span data-stu-id="96120-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96120-218">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="96120-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





