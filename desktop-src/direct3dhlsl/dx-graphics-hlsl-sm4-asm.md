---
title: 著色器模型4元件
description: 著色器模型4元件
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021485"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="c6645-103">著色器模型4元件</span><span class="sxs-lookup"><span data-stu-id="c6645-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="c6645-104">著色器模型4需要您在 HLSL 中編寫著色器。</span><span class="sxs-lookup"><span data-stu-id="c6645-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="c6645-105">不過，著色器編譯器會將 HLSL 程式碼編譯為在裝置上執行的元件。</span><span class="sxs-lookup"><span data-stu-id="c6645-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="c6645-106">如果您使用適用于 Windows 的 PIX 來對著色器進行偵測，您可以選擇在 HLSL 或元件中顯示著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="c6645-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="c6645-107">本節列出在您對著色器進行偵錯工具時，可能會遇到的著色器模型4和著色器模型4.1 元件指示。</span><span class="sxs-lookup"><span data-stu-id="c6645-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="c6645-108">指令修飾詞</span><span class="sxs-lookup"><span data-stu-id="c6645-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="c6645-109">add</span><span class="sxs-lookup"><span data-stu-id="c6645-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="c6645-110">and</span><span class="sxs-lookup"><span data-stu-id="c6645-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="c6645-111">break</span><span class="sxs-lookup"><span data-stu-id="c6645-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="c6645-112">breakc</span><span class="sxs-lookup"><span data-stu-id="c6645-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="c6645-113">call</span><span class="sxs-lookup"><span data-stu-id="c6645-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="c6645-114">callc</span><span class="sxs-lookup"><span data-stu-id="c6645-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="c6645-115">case</span><span class="sxs-lookup"><span data-stu-id="c6645-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="c6645-116">繼續</span><span class="sxs-lookup"><span data-stu-id="c6645-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="c6645-117">continuec</span><span class="sxs-lookup"><span data-stu-id="c6645-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="c6645-118">削減</span><span class="sxs-lookup"><span data-stu-id="c6645-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="c6645-119">dcl \_ constantBuffer</span><span class="sxs-lookup"><span data-stu-id="c6645-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="c6645-120">dcl \_ globalFlags</span><span class="sxs-lookup"><span data-stu-id="c6645-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="c6645-121">dcl \_ immediateConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="c6645-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="c6645-122">dcl \_ indexableTemp</span><span class="sxs-lookup"><span data-stu-id="c6645-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="c6645-123">dcl \_ indexRange</span><span class="sxs-lookup"><span data-stu-id="c6645-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="c6645-124">dcl \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="c6645-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="c6645-125">dcl \_ 輸入 \_ sv</span><span class="sxs-lookup"><span data-stu-id="c6645-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="c6645-126">dcl \_ 輸入 vPrim</span><span class="sxs-lookup"><span data-stu-id="c6645-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="c6645-127">dcl \_ maxOutputVertexCount</span><span class="sxs-lookup"><span data-stu-id="c6645-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="c6645-128">dcl \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="c6645-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="c6645-129">dcl \_ 輸出 \_ oDepth</span><span class="sxs-lookup"><span data-stu-id="c6645-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="c6645-130">dcl \_ 輸出 \_ sgv</span><span class="sxs-lookup"><span data-stu-id="c6645-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="c6645-131">dcl \_ 輸出 \_ siv</span><span class="sxs-lookup"><span data-stu-id="c6645-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="c6645-132">dcl \_ outputTopology</span><span class="sxs-lookup"><span data-stu-id="c6645-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="c6645-133">dcl \_ 資源</span><span class="sxs-lookup"><span data-stu-id="c6645-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="c6645-134">dcl \_ 取樣器</span><span class="sxs-lookup"><span data-stu-id="c6645-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="c6645-135">dcl \_ 溫度</span><span class="sxs-lookup"><span data-stu-id="c6645-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="c6645-136">預設值</span><span class="sxs-lookup"><span data-stu-id="c6645-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="c6645-137">deriv \_ rtx</span><span class="sxs-lookup"><span data-stu-id="c6645-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="c6645-138">deriv \_ rty</span><span class="sxs-lookup"><span data-stu-id="c6645-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="c6645-139">丟棄</span><span class="sxs-lookup"><span data-stu-id="c6645-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="c6645-140">div</span><span class="sxs-lookup"><span data-stu-id="c6645-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="c6645-141">dp2</span><span class="sxs-lookup"><span data-stu-id="c6645-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="c6645-142">dp3</span><span class="sxs-lookup"><span data-stu-id="c6645-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="c6645-143">dp4</span><span class="sxs-lookup"><span data-stu-id="c6645-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="c6645-144">else</span><span class="sxs-lookup"><span data-stu-id="c6645-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="c6645-145">發出</span><span class="sxs-lookup"><span data-stu-id="c6645-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="c6645-146">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="c6645-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="c6645-147">endif</span><span class="sxs-lookup"><span data-stu-id="c6645-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="c6645-148">endloop</span><span class="sxs-lookup"><span data-stu-id="c6645-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="c6645-149">endswitch</span><span class="sxs-lookup"><span data-stu-id="c6645-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="c6645-150">eq</span><span class="sxs-lookup"><span data-stu-id="c6645-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="c6645-151">exp</span><span class="sxs-lookup"><span data-stu-id="c6645-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="c6645-152">Frc</span><span class="sxs-lookup"><span data-stu-id="c6645-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="c6645-153">ftoi</span><span class="sxs-lookup"><span data-stu-id="c6645-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="c6645-154">ftou</span><span class="sxs-lookup"><span data-stu-id="c6645-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="c6645-155">ge</span><span class="sxs-lookup"><span data-stu-id="c6645-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="c6645-156">iadd</span><span class="sxs-lookup"><span data-stu-id="c6645-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="c6645-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="c6645-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="c6645-158">ieq</span><span class="sxs-lookup"><span data-stu-id="c6645-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="c6645-159">if</span><span class="sxs-lookup"><span data-stu-id="c6645-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="c6645-160">Ige</span><span class="sxs-lookup"><span data-stu-id="c6645-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="c6645-161">ilt</span><span class="sxs-lookup"><span data-stu-id="c6645-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="c6645-162">imad</span><span class="sxs-lookup"><span data-stu-id="c6645-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="c6645-163">imin</span><span class="sxs-lookup"><span data-stu-id="c6645-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="c6645-164">imul</span><span class="sxs-lookup"><span data-stu-id="c6645-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="c6645-165">視窗</span><span class="sxs-lookup"><span data-stu-id="c6645-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="c6645-166">ineg</span><span class="sxs-lookup"><span data-stu-id="c6645-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="c6645-167">ishl</span><span class="sxs-lookup"><span data-stu-id="c6645-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="c6645-168">ishr</span><span class="sxs-lookup"><span data-stu-id="c6645-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="c6645-169">itof</span><span class="sxs-lookup"><span data-stu-id="c6645-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="c6645-170">label</span><span class="sxs-lookup"><span data-stu-id="c6645-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="c6645-171">Ld</span><span class="sxs-lookup"><span data-stu-id="c6645-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="c6645-172">日誌</span><span class="sxs-lookup"><span data-stu-id="c6645-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="c6645-173">loop</span><span class="sxs-lookup"><span data-stu-id="c6645-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="c6645-174">lt</span><span class="sxs-lookup"><span data-stu-id="c6645-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="c6645-175">瘋狂</span><span class="sxs-lookup"><span data-stu-id="c6645-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="c6645-176">max</span><span class="sxs-lookup"><span data-stu-id="c6645-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="c6645-177">min</span><span class="sxs-lookup"><span data-stu-id="c6645-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="c6645-178">平均線</span><span class="sxs-lookup"><span data-stu-id="c6645-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="c6645-179">movc</span><span class="sxs-lookup"><span data-stu-id="c6645-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="c6645-180">mul</span><span class="sxs-lookup"><span data-stu-id="c6645-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="c6645-181">ne</span><span class="sxs-lookup"><span data-stu-id="c6645-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="c6645-182">nop</span><span class="sxs-lookup"><span data-stu-id="c6645-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="c6645-183">not</span><span class="sxs-lookup"><span data-stu-id="c6645-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="c6645-184">or</span><span class="sxs-lookup"><span data-stu-id="c6645-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="c6645-185">resinfo</span><span class="sxs-lookup"><span data-stu-id="c6645-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="c6645-186">Ret</span><span class="sxs-lookup"><span data-stu-id="c6645-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="c6645-187">retc</span><span class="sxs-lookup"><span data-stu-id="c6645-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="c6645-188">四捨五入 \_</span><span class="sxs-lookup"><span data-stu-id="c6645-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="c6645-189">四捨五入 \_</span><span class="sxs-lookup"><span data-stu-id="c6645-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="c6645-190">四捨五入 \_ pi</span><span class="sxs-lookup"><span data-stu-id="c6645-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="c6645-191">圓形 \_ z</span><span class="sxs-lookup"><span data-stu-id="c6645-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="c6645-192">rsq</span><span class="sxs-lookup"><span data-stu-id="c6645-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="c6645-193">樣品</span><span class="sxs-lookup"><span data-stu-id="c6645-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="c6645-194">範例 \_ b</span><span class="sxs-lookup"><span data-stu-id="c6645-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="c6645-195">範例 \_ c</span><span class="sxs-lookup"><span data-stu-id="c6645-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="c6645-196">範例 \_ c \_ lz</span><span class="sxs-lookup"><span data-stu-id="c6645-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="c6645-197">範例 \_ d</span><span class="sxs-lookup"><span data-stu-id="c6645-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="c6645-198">範例 \_ l</span><span class="sxs-lookup"><span data-stu-id="c6645-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="c6645-199">sincos</span><span class="sxs-lookup"><span data-stu-id="c6645-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="c6645-200">sqrt</span><span class="sxs-lookup"><span data-stu-id="c6645-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="c6645-201">switch</span><span class="sxs-lookup"><span data-stu-id="c6645-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="c6645-202">udiv</span><span class="sxs-lookup"><span data-stu-id="c6645-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="c6645-203">uge</span><span class="sxs-lookup"><span data-stu-id="c6645-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="c6645-204">u）</span><span class="sxs-lookup"><span data-stu-id="c6645-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="c6645-205">umad</span><span class="sxs-lookup"><span data-stu-id="c6645-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="c6645-206">umax</span><span class="sxs-lookup"><span data-stu-id="c6645-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="c6645-207">umin</span><span class="sxs-lookup"><span data-stu-id="c6645-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="c6645-208">umul</span><span class="sxs-lookup"><span data-stu-id="c6645-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="c6645-209">ushr</span><span class="sxs-lookup"><span data-stu-id="c6645-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="c6645-210">utof</span><span class="sxs-lookup"><span data-stu-id="c6645-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="c6645-211">Xor</span><span class="sxs-lookup"><span data-stu-id="c6645-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="c6645-212">著色器模型4.1 元件</span><span class="sxs-lookup"><span data-stu-id="c6645-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="c6645-213">著色器模型4.1 支援所有著色器模型4.0 指令和下列其他指示：</span><span class="sxs-lookup"><span data-stu-id="c6645-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="c6645-214">gather4</span><span class="sxs-lookup"><span data-stu-id="c6645-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="c6645-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="c6645-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="c6645-216">Lod</span><span class="sxs-lookup"><span data-stu-id="c6645-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="c6645-217">sampleinfo</span><span class="sxs-lookup"><span data-stu-id="c6645-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="c6645-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="c6645-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c6645-219">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6645-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6645-220">Asm 著色器參考</span><span class="sxs-lookup"><span data-stu-id="c6645-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="c6645-221">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c6645-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




