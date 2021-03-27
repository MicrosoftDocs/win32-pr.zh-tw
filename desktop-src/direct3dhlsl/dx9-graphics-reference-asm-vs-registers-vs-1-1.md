---
title: 註冊-vs_1_1
description: 本章節包含頂點著色器第1版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6776fef206f9ced0608e86cbf596585399d4a12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840463"
---
# <a name="registers---vs_1_1"></a><span data-ttu-id="3badd-103">註冊-vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3badd-103">Registers - vs\_1\_1</span></span>

<span data-ttu-id="3badd-104">本章節包含頂點著色器第1版所實之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3badd-104">This section contains reference information for the input and output registers implemented by vertex shader version 1\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="3badd-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-105">Input Registers</span></span>



| <span data-ttu-id="3badd-106">註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-106">Register</span></span> | <span data-ttu-id="3badd-107">名稱</span><span class="sxs-lookup"><span data-stu-id="3badd-107">Name</span></span>                                                                                  | <span data-ttu-id="3badd-108">Count</span><span class="sxs-lookup"><span data-stu-id="3badd-108">Count</span></span>      | <span data-ttu-id="3badd-109">R/W</span><span class="sxs-lookup"><span data-stu-id="3badd-109">R/W</span></span> | <span data-ttu-id="3badd-110">\# 讀取埠</span><span class="sxs-lookup"><span data-stu-id="3badd-110">\# Read ports</span></span> | <span data-ttu-id="3badd-111">\# 讀取/inst</span><span class="sxs-lookup"><span data-stu-id="3badd-111">\# Reads / inst</span></span> | <span data-ttu-id="3badd-112">維度</span><span class="sxs-lookup"><span data-stu-id="3badd-112">Dimension</span></span>  | <span data-ttu-id="3badd-113">RelAddr</span><span class="sxs-lookup"><span data-stu-id="3badd-113">RelAddr</span></span> | <span data-ttu-id="3badd-114">Defaults</span><span class="sxs-lookup"><span data-stu-id="3badd-114">Defaults</span></span>     | <span data-ttu-id="3badd-115">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="3badd-115">Requires DCL</span></span> |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| <span data-ttu-id="3badd-116">a0</span><span class="sxs-lookup"><span data-stu-id="3badd-116">a0</span></span>       | [<span data-ttu-id="3badd-117">位址註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-117">Address Register</span></span>](dx9-graphics-reference-asm-vs-registers-address.md)               | <span data-ttu-id="3badd-118">1</span><span class="sxs-lookup"><span data-stu-id="3badd-118">1</span></span>          | <span data-ttu-id="3badd-119">R/W</span><span class="sxs-lookup"><span data-stu-id="3badd-119">R/W</span></span> | <span data-ttu-id="3badd-120">1</span><span class="sxs-lookup"><span data-stu-id="3badd-120">1</span></span>             | <span data-ttu-id="3badd-121">無限制</span><span class="sxs-lookup"><span data-stu-id="3badd-121">Unlimited</span></span>       | <span data-ttu-id="3badd-122">請參閱附注3</span><span class="sxs-lookup"><span data-stu-id="3badd-122">See note 3</span></span> | <span data-ttu-id="3badd-123">否</span><span class="sxs-lookup"><span data-stu-id="3badd-123">No</span></span>      | <span data-ttu-id="3badd-124">None</span><span class="sxs-lookup"><span data-stu-id="3badd-124">None</span></span>         | <span data-ttu-id="3badd-125">No</span><span class="sxs-lookup"><span data-stu-id="3badd-125">No</span></span>           |
| <span data-ttu-id="3badd-126">c\#</span><span class="sxs-lookup"><span data-stu-id="3badd-126">c\#</span></span>      | [<span data-ttu-id="3badd-127">常數 Float Register</span><span class="sxs-lookup"><span data-stu-id="3badd-127">Constant Float Register</span></span>](dx9-graphics-reference-asm-vs-registers-constant-float.md) | <span data-ttu-id="3badd-128">請參閱附註 2</span><span class="sxs-lookup"><span data-stu-id="3badd-128">See note 2</span></span> | <span data-ttu-id="3badd-129">R</span><span class="sxs-lookup"><span data-stu-id="3badd-129">R</span></span>   | <span data-ttu-id="3badd-130">1</span><span class="sxs-lookup"><span data-stu-id="3badd-130">1</span></span>             | <span data-ttu-id="3badd-131">無限制</span><span class="sxs-lookup"><span data-stu-id="3badd-131">Unlimited</span></span>       | <span data-ttu-id="3badd-132">4</span><span class="sxs-lookup"><span data-stu-id="3badd-132">4</span></span>          | <span data-ttu-id="3badd-133">a0. x</span><span class="sxs-lookup"><span data-stu-id="3badd-133">a0.x</span></span>    | <span data-ttu-id="3badd-134"> (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="3badd-134">(0, 0, 0, 0)</span></span> | <span data-ttu-id="3badd-135">No</span><span class="sxs-lookup"><span data-stu-id="3badd-135">No</span></span>           |
| <span data-ttu-id="3badd-136">V\#</span><span class="sxs-lookup"><span data-stu-id="3badd-136">v\#</span></span>      | [<span data-ttu-id="3badd-137">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-137">Input Register</span></span>](dx9-graphics-reference-asm-vs-registers-input.md)                   | <span data-ttu-id="3badd-138">16</span><span class="sxs-lookup"><span data-stu-id="3badd-138">16</span></span>         | <span data-ttu-id="3badd-139">R</span><span class="sxs-lookup"><span data-stu-id="3badd-139">R</span></span>   | <span data-ttu-id="3badd-140">1</span><span class="sxs-lookup"><span data-stu-id="3badd-140">1</span></span>             | <span data-ttu-id="3badd-141">無限制</span><span class="sxs-lookup"><span data-stu-id="3badd-141">Unlimited</span></span>       | <span data-ttu-id="3badd-142">4</span><span class="sxs-lookup"><span data-stu-id="3badd-142">4</span></span>          | <span data-ttu-id="3badd-143">否</span><span class="sxs-lookup"><span data-stu-id="3badd-143">No</span></span>      | <span data-ttu-id="3badd-144">請參閱附注1</span><span class="sxs-lookup"><span data-stu-id="3badd-144">See note 1</span></span>   | <span data-ttu-id="3badd-145">Yes</span><span class="sxs-lookup"><span data-stu-id="3badd-145">Yes</span></span>          |
| <span data-ttu-id="3badd-146">R\#</span><span class="sxs-lookup"><span data-stu-id="3badd-146">r\#</span></span>      | [<span data-ttu-id="3badd-147">暫時註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-147">Temporary Register</span></span>](dx9-graphics-reference-asm-vs-registers-temporary.md)           | <span data-ttu-id="3badd-148">12</span><span class="sxs-lookup"><span data-stu-id="3badd-148">12</span></span>         | <span data-ttu-id="3badd-149">R/W</span><span class="sxs-lookup"><span data-stu-id="3badd-149">R/W</span></span> | <span data-ttu-id="3badd-150">3</span><span class="sxs-lookup"><span data-stu-id="3badd-150">3</span></span>             | <span data-ttu-id="3badd-151">無限制</span><span class="sxs-lookup"><span data-stu-id="3badd-151">Unlimited</span></span>       | <span data-ttu-id="3badd-152">4</span><span class="sxs-lookup"><span data-stu-id="3badd-152">4</span></span>          | <span data-ttu-id="3badd-153">否</span><span class="sxs-lookup"><span data-stu-id="3badd-153">No</span></span>      | <span data-ttu-id="3badd-154">None</span><span class="sxs-lookup"><span data-stu-id="3badd-154">None</span></span>         | <span data-ttu-id="3badd-155">No</span><span class="sxs-lookup"><span data-stu-id="3badd-155">No</span></span>           |



 

<span data-ttu-id="3badd-156">注意：</span><span class="sxs-lookup"><span data-stu-id="3badd-156">Notes:</span></span>

1.  <span data-ttu-id="3badd-157">部分 (0、0、0、1) -如果只有一部分的通道已更新，則其餘的通道會預設為 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="3badd-157">Partial (0, 0, 0, 1) - If only a subset of channels are updated, the remaining channels will default to (0, 0, 0, 1).</span></span>
2.  <span data-ttu-id="3badd-158">等於 D3DCAPS9。Vs \_ 1 1) 的 MaxVertexShaderConst (至少 96 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3badd-158">Equal to D3DCAPS9.MaxVertexShaderConst (at least 96 for vs\_1\_1).</span></span>
3.  <span data-ttu-id="3badd-159">只有. x 通道可供使用。</span><span class="sxs-lookup"><span data-stu-id="3badd-159">Only .x channel is available.</span></span>

## <a name="output-registers"></a><span data-ttu-id="3badd-160">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-160">Output Registers</span></span>



| <span data-ttu-id="3badd-161">註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-161">Register</span></span> | <span data-ttu-id="3badd-162">名稱</span><span class="sxs-lookup"><span data-stu-id="3badd-162">Name</span></span>                        | <span data-ttu-id="3badd-163">Count</span><span class="sxs-lookup"><span data-stu-id="3badd-163">Count</span></span> | <span data-ttu-id="3badd-164">R/W</span><span class="sxs-lookup"><span data-stu-id="3badd-164">R/W</span></span> | <span data-ttu-id="3badd-165">維度</span><span class="sxs-lookup"><span data-stu-id="3badd-165">Dimension</span></span> | <span data-ttu-id="3badd-166">RelAddr</span><span class="sxs-lookup"><span data-stu-id="3badd-166">RelAddr</span></span> | <span data-ttu-id="3badd-167">Defaults</span><span class="sxs-lookup"><span data-stu-id="3badd-167">Defaults</span></span> | <span data-ttu-id="3badd-168">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="3badd-168">Requires DCL</span></span> |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| <span data-ttu-id="3badd-169">oPos</span><span class="sxs-lookup"><span data-stu-id="3badd-169">oPos</span></span>     | <span data-ttu-id="3badd-170">位置註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-170">Position Register</span></span>           | <span data-ttu-id="3badd-171">1</span><span class="sxs-lookup"><span data-stu-id="3badd-171">1</span></span>     | <span data-ttu-id="3badd-172">W</span><span class="sxs-lookup"><span data-stu-id="3badd-172">W</span></span>   | <span data-ttu-id="3badd-173">4</span><span class="sxs-lookup"><span data-stu-id="3badd-173">4</span></span>         | <span data-ttu-id="3badd-174">否</span><span class="sxs-lookup"><span data-stu-id="3badd-174">No</span></span>      | <span data-ttu-id="3badd-175">None</span><span class="sxs-lookup"><span data-stu-id="3badd-175">None</span></span>     | <span data-ttu-id="3badd-176">No</span><span class="sxs-lookup"><span data-stu-id="3badd-176">No</span></span>           |
| <span data-ttu-id="3badd-177">oFog</span><span class="sxs-lookup"><span data-stu-id="3badd-177">oFog</span></span>     | <span data-ttu-id="3badd-178">霧化暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-178">Fog Register</span></span>                | <span data-ttu-id="3badd-179">1</span><span class="sxs-lookup"><span data-stu-id="3badd-179">1</span></span>     | <span data-ttu-id="3badd-180">W</span><span class="sxs-lookup"><span data-stu-id="3badd-180">W</span></span>   | <span data-ttu-id="3badd-181">1</span><span class="sxs-lookup"><span data-stu-id="3badd-181">1</span></span>         | <span data-ttu-id="3badd-182">否</span><span class="sxs-lookup"><span data-stu-id="3badd-182">No</span></span>      | <span data-ttu-id="3badd-183">None</span><span class="sxs-lookup"><span data-stu-id="3badd-183">None</span></span>     | <span data-ttu-id="3badd-184">No</span><span class="sxs-lookup"><span data-stu-id="3badd-184">No</span></span>           |
| <span data-ttu-id="3badd-185">選擇</span><span class="sxs-lookup"><span data-stu-id="3badd-185">oPts</span></span>     | <span data-ttu-id="3badd-186">點大小暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-186">Point Size Register</span></span>         | <span data-ttu-id="3badd-187">1</span><span class="sxs-lookup"><span data-stu-id="3badd-187">1</span></span>     | <span data-ttu-id="3badd-188">W</span><span class="sxs-lookup"><span data-stu-id="3badd-188">W</span></span>   | <span data-ttu-id="3badd-189">1</span><span class="sxs-lookup"><span data-stu-id="3badd-189">1</span></span>         | <span data-ttu-id="3badd-190">否</span><span class="sxs-lookup"><span data-stu-id="3badd-190">No</span></span>      | <span data-ttu-id="3badd-191">None</span><span class="sxs-lookup"><span data-stu-id="3badd-191">None</span></span>     | <span data-ttu-id="3badd-192">No</span><span class="sxs-lookup"><span data-stu-id="3badd-192">No</span></span>           |
| <span data-ttu-id="3badd-193">Od\#</span><span class="sxs-lookup"><span data-stu-id="3badd-193">oD\#</span></span>     | <span data-ttu-id="3badd-194">色彩註冊;請參閱附注1</span><span class="sxs-lookup"><span data-stu-id="3badd-194">Color Register; See note 1</span></span>  | <span data-ttu-id="3badd-195">2</span><span class="sxs-lookup"><span data-stu-id="3badd-195">2</span></span>     | <span data-ttu-id="3badd-196">W</span><span class="sxs-lookup"><span data-stu-id="3badd-196">W</span></span>   | <span data-ttu-id="3badd-197">4</span><span class="sxs-lookup"><span data-stu-id="3badd-197">4</span></span>         | <span data-ttu-id="3badd-198">否</span><span class="sxs-lookup"><span data-stu-id="3badd-198">No</span></span>      | <span data-ttu-id="3badd-199">None</span><span class="sxs-lookup"><span data-stu-id="3badd-199">None</span></span>     | <span data-ttu-id="3badd-200">No</span><span class="sxs-lookup"><span data-stu-id="3badd-200">No</span></span>           |
| <span data-ttu-id="3badd-201">oT\#</span><span class="sxs-lookup"><span data-stu-id="3badd-201">oT\#</span></span>     | <span data-ttu-id="3badd-202">材質座標註冊</span><span class="sxs-lookup"><span data-stu-id="3badd-202">Texture Coordinate Register</span></span> | <span data-ttu-id="3badd-203">8</span><span class="sxs-lookup"><span data-stu-id="3badd-203">8</span></span>     | <span data-ttu-id="3badd-204">W</span><span class="sxs-lookup"><span data-stu-id="3badd-204">W</span></span>   | <span data-ttu-id="3badd-205">4</span><span class="sxs-lookup"><span data-stu-id="3badd-205">4</span></span>         | <span data-ttu-id="3badd-206">否</span><span class="sxs-lookup"><span data-stu-id="3badd-206">No</span></span>      | <span data-ttu-id="3badd-207">None</span><span class="sxs-lookup"><span data-stu-id="3badd-207">None</span></span>     | <span data-ttu-id="3badd-208">No</span><span class="sxs-lookup"><span data-stu-id="3badd-208">No</span></span>           |



 

<span data-ttu-id="3badd-209">注意：</span><span class="sxs-lookup"><span data-stu-id="3badd-209">Notes:</span></span>

-   <span data-ttu-id="3badd-210">oD0 是擴散色彩輸出;oD1 是反射色彩輸出。</span><span class="sxs-lookup"><span data-stu-id="3badd-210">oD0 is the diffuse color output; oD1 is the specular color output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3badd-211">相關主題</span><span class="sxs-lookup"><span data-stu-id="3badd-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3badd-212">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="3badd-212">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




