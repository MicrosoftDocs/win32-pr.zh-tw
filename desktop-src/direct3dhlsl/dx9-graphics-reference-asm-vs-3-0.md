---
title: vs_3_0
description: 深入瞭解 vs_3_0，這是一個可程式化的頂點著色器，由一組在頂點資料上操作的指令所組成。
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011071"
---
# <a name="vs_3_0"></a><span data-ttu-id="2b336-103">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2b336-103">vs\_3\_0</span></span>

<span data-ttu-id="2b336-104">可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="2b336-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="2b336-105">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="2b336-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="2b336-106">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="2b336-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="2b336-107">頂點著色器版本與 \_ 3 \_ 0：擴充 vs 2 x 所支援的功能集 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2b336-107">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="2b336-108">Vs \_ 2 X 中需要設定端點的每個功能 \_ ，在 vs 3 0 中都有提供 \_ ， \_ 而不需要端點。</span><span class="sxs-lookup"><span data-stu-id="2b336-108">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="2b336-109">[指示-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="2b336-109">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="2b336-110">暫存器[-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)會列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="2b336-110">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="2b336-111">[頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="2b336-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="2b336-112">[頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="2b336-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="2b336-113">[[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="2b336-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="2b336-114">[目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="2b336-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="2b336-115">新功能</span><span class="sxs-lookup"><span data-stu-id="2b336-115">New Features</span></span>

<span data-ttu-id="2b336-116">\_下列各節列出頂點著色器版本與 3 0 的新功能 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2b336-116">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="2b336-117">索引暫存器</span><span class="sxs-lookup"><span data-stu-id="2b336-117">Indexing Registers</span></span>

<span data-ttu-id="2b336-118">在先前的著色器模型中，只能編制常數暫存器 bank 的索引。</span><span class="sxs-lookup"><span data-stu-id="2b336-118">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="2b336-119">在此模型中，您可以使用迴圈計數器 register (aL) 來編制下列註冊銀行的索引：</span><span class="sxs-lookup"><span data-stu-id="2b336-119">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="2b336-120">輸入 register (v \#) </span><span class="sxs-lookup"><span data-stu-id="2b336-120">Input register (v\#)</span></span>
-   <span data-ttu-id="2b336-121">Output register (o \#) </span><span class="sxs-lookup"><span data-stu-id="2b336-121">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="2b336-122">頂點紋理</span><span class="sxs-lookup"><span data-stu-id="2b336-122">Vertex Textures</span></span>

<span data-ttu-id="2b336-123">此著色器模型支援使用 texldl 在頂點著色器中進行紋理查閱。</span><span class="sxs-lookup"><span data-stu-id="2b336-123">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="2b336-124">頂點引擎有四個紋理取樣器階段 (有別于置換圖取樣器和圖元引擎中的材質取樣器) ，可用來在這些階段設定紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="2b336-124">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="2b336-125">請參閱 [vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理 ](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)。</span><span class="sxs-lookup"><span data-stu-id="2b336-125">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="2b336-126">頂點資料流程頻率</span><span class="sxs-lookup"><span data-stu-id="2b336-126">Vertex Stream Frequency</span></span>

<span data-ttu-id="2b336-127">這項功能可讓您以不同于每個頂點一次的速率初始化輸入暫存器的子集。</span><span class="sxs-lookup"><span data-stu-id="2b336-127">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="2b336-128">請參閱 [繪圖非索引幾何](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)。</span><span class="sxs-lookup"><span data-stu-id="2b336-128">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="2b336-129">著色器輸出</span><span class="sxs-lookup"><span data-stu-id="2b336-129">Shader Output</span></span>

<span data-ttu-id="2b336-130">與 vs \_ 2 \_ 0 類似，著色器的輸出會隨著靜態流程式控制制而有所不同。</span><span class="sxs-lookup"><span data-stu-id="2b336-130">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="2b336-131">請小心使用動態分支，因為這可能會導致著色器輸出依頂點而異。</span><span class="sxs-lookup"><span data-stu-id="2b336-131">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="2b336-132">這將會在不同的硬體上產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="2b336-132">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="2b336-133">動態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="2b336-133">Dynamic flow control</span></span>

<span data-ttu-id="2b336-134">支援所有動態流程式控制制指令。</span><span class="sxs-lookup"><span data-stu-id="2b336-134">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="2b336-135">允許的最大嵌套深度值為24。</span><span class="sxs-lookup"><span data-stu-id="2b336-135">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="2b336-136"> (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ) 。</span><span class="sxs-lookup"><span data-stu-id="2b336-136">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="2b336-137">臨時暫存器</span><span class="sxs-lookup"><span data-stu-id="2b336-137">Temporary Registers</span></span>

<span data-ttu-id="2b336-138">支援 (r) 的總計32暫存暫存器 \# 。</span><span class="sxs-lookup"><span data-stu-id="2b336-138">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="2b336-139">靜態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="2b336-139">Static Flow Control</span></span>

<span data-ttu-id="2b336-140">[迴圈-vs](loop---vs.md)rep 的最大嵌套深度為 / [](rep---vs.md) 4。</span><span class="sxs-lookup"><span data-stu-id="2b336-140">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="2b336-141">[Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz pred-vs](callnz-pred---vs.md)的最大嵌套深度為4。</span><span class="sxs-lookup"><span data-stu-id="2b336-141">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="2b336-142">[若為 bool-vs](if-bool---vs.md)，則允許的最大嵌套深度值為24。</span><span class="sxs-lookup"><span data-stu-id="2b336-142">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="2b336-143"> (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ) 。</span><span class="sxs-lookup"><span data-stu-id="2b336-143">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="2b336-144">預測</span><span class="sxs-lookup"><span data-stu-id="2b336-144">Predication</span></span>

<span data-ttu-id="2b336-145">支援指令 predication。</span><span class="sxs-lookup"><span data-stu-id="2b336-145">Instruction predication is supported.</span></span> <span data-ttu-id="2b336-146">使用 [setp \_ comp-vs](setp-comp---vs.md) 來設定述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="2b336-146">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="2b336-147">指令計數</span><span class="sxs-lookup"><span data-stu-id="2b336-147">Instruction Count</span></span>

<span data-ttu-id="2b336-148">每個頂點著色器都允許從512到 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)中 MaxVertexShader30InstructionSlots 的位置數目。</span><span class="sxs-lookup"><span data-stu-id="2b336-148">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="2b336-149">因為迴圈/rep 支援，所以執行的指令數目可能會更高。不過，這會由 D3DCAPS9 中的 MaxVShaderInstructionsExecuted 限制，其中至少應為0xFFFF。</span><span class="sxs-lookup"><span data-stu-id="2b336-149">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="2b336-150">裝置 Cap</span><span class="sxs-lookup"><span data-stu-id="2b336-150">Device Caps</span></span>

<span data-ttu-id="2b336-151">如果支援頂點著色器 3 \_ 0，硬體 (中最少) 支援下列 caps：</span><span class="sxs-lookup"><span data-stu-id="2b336-151">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b336-152">筆蓋</span><span class="sxs-lookup"><span data-stu-id="2b336-152">Cap</span></span></th>
<th><span data-ttu-id="2b336-153">功能</span><span class="sxs-lookup"><span data-stu-id="2b336-153">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b336-154">著色器 caps</span><span class="sxs-lookup"><span data-stu-id="2b336-154">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="2b336-155">DynamicFlowControlDepth 是24</span><span class="sxs-lookup"><span data-stu-id="2b336-155">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="2b336-156">NumTemps 為32</span><span class="sxs-lookup"><span data-stu-id="2b336-156">NumTemps is 32</span></span></li>
<li><span data-ttu-id="2b336-157">StaticFlowControlDepth 為4</span><span class="sxs-lookup"><span data-stu-id="2b336-157">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="2b336-158">支援 Predication。</span><span class="sxs-lookup"><span data-stu-id="2b336-158">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b336-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="2b336-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="2b336-160">8K</span><span class="sxs-lookup"><span data-stu-id="2b336-160">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b336-161">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="2b336-161">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="2b336-162">3_0</span><span class="sxs-lookup"><span data-stu-id="2b336-162">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b336-163">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="2b336-163">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="2b336-164">256</span><span class="sxs-lookup"><span data-stu-id="2b336-164">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b336-165">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="2b336-165">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="2b336-166">512</span><span class="sxs-lookup"><span data-stu-id="2b336-166">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b336-167">霧化支援</span><span class="sxs-lookup"><span data-stu-id="2b336-167">Fog support</span></span></td>
<td><span data-ttu-id="2b336-168">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="2b336-168">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b336-169">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="2b336-169">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="2b336-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="2b336-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="2b336-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="2b336-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b336-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="2b336-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="2b336-173">頂點宣告中的頂點元素可以共用相同的資料流程位移。</span><span class="sxs-lookup"><span data-stu-id="2b336-173">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b336-174">頂點格式</span><span class="sxs-lookup"><span data-stu-id="2b336-174">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="2b336-175">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="2b336-175">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="2b336-176">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="2b336-176">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="2b336-177">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="2b336-177">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="2b336-178">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="2b336-178">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="2b336-179">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="2b336-179">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="2b336-180">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="2b336-180">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2b336-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b336-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b336-182">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="2b336-182">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 