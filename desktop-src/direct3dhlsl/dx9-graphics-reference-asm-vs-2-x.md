---
title: vs_2_x
description: 可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463464"
---
# <a name="vs_2_x"></a><span data-ttu-id="ef033-105">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef033-105">vs\_2\_x</span></span>

<span data-ttu-id="ef033-106">可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="ef033-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="ef033-107">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="ef033-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="ef033-108">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="ef033-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="ef033-109">頂點著色器版本與 \_ 2 \_ x 擴充 vs 2 0 所支援的功能集 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ef033-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="ef033-110">每個額外的功能都會以 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)中 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)結構的對應端點表示。</span><span class="sxs-lookup"><span data-stu-id="ef033-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="ef033-111">若要使用這些 caps 所表示的任何增強功能，必須將頂點著色器版本指定為 vs \_ 2 \_ x。</span><span class="sxs-lookup"><span data-stu-id="ef033-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="ef033-112">[指示-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="ef033-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="ef033-113">暫存器[-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md)列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="ef033-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="ef033-114">[頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="ef033-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="ef033-115">[頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="ef033-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="ef033-116">[[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="ef033-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="ef033-117">[目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="ef033-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="ef033-118">新功能</span><span class="sxs-lookup"><span data-stu-id="ef033-118">New Features</span></span>

<span data-ttu-id="ef033-119">新功能如下：</span><span class="sxs-lookup"><span data-stu-id="ef033-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="ef033-120">動態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="ef033-120">Dynamic Flow Control</span></span>

<span data-ttu-id="ef033-121">如果 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0，則支援下列動態流程式控制制指示：</span><span class="sxs-lookup"><span data-stu-id="ef033-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="ef033-122">如果是 \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="ef033-123">中斷-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="ef033-124">中斷 \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="ef033-125">如果也設定了 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ，則支援下列額外的流程式控制制指示：</span><span class="sxs-lookup"><span data-stu-id="ef033-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="ef033-126">setp \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="ef033-127">如果 pred-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="ef033-128">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="ef033-129">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="ef033-130">動態流程式控制制深度的值範圍是0到24，等於動態流程式控制制指示的嵌套深度 (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ef033-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="ef033-131">如果此上限為零，則裝置不支援動態流程式控制制指示。</span><span class="sxs-lookup"><span data-stu-id="ef033-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="ef033-132">臨時暫存器數目</span><span class="sxs-lookup"><span data-stu-id="ef033-132">Number of Temporary Registers</span></span>

<span data-ttu-id="ef033-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) 代表裝置所支援的 [暫存](dx9-graphics-reference-asm-vs-registers-temporary.md)登錄數目。</span><span class="sxs-lookup"><span data-stu-id="ef033-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="ef033-134">此上限的值範圍是12到32。</span><span class="sxs-lookup"><span data-stu-id="ef033-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="ef033-135">靜態流程式控制制的嵌套深度</span><span class="sxs-lookup"><span data-stu-id="ef033-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="ef033-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)代表兩種靜態流程式控制制指令類型的嵌套深度：[迴圈-vs](loop---vs.md) / [rep-vs](rep---vs.md)和[call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md)， / [如果 bool-vs](if-bool---vs.md). 迴圈-vs/rep-vs 指令可以嵌套到 D3DVS20CAPS 深層。</span><span class="sxs-lookup"><span data-stu-id="ef033-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="ef033-137">相對地，call-vs/callnz bool-vs 指令可以嵌套至 D3DVS20CAPS 深層。</span><span class="sxs-lookup"><span data-stu-id="ef033-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="ef033-138">如果同時設定了 D3DVS20CAPS，則 [callnz pred-vs](callnz-pred---vs.md) 會計算呼叫-vs/callnz bool-vs/if bool-vs (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ef033-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="ef033-139">預測</span><span class="sxs-lookup"><span data-stu-id="ef033-139">Predication</span></span>

<span data-ttu-id="ef033-140">如果設定了 [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ，則裝置支援 [setp 的 \_ comp](setp-comp---vs.md) 與指令 predication。</span><span class="sxs-lookup"><span data-stu-id="ef033-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="ef033-141">如果 D3DVS20CAPS 也大於0，則支援下列額外的動態流程式控制制指示：</span><span class="sxs-lookup"><span data-stu-id="ef033-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="ef033-142">如果 pred-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="ef033-143">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="ef033-144">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="ef033-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="ef033-145">指令計數</span><span class="sxs-lookup"><span data-stu-id="ef033-145">Instruction Count</span></span>

<span data-ttu-id="ef033-146">每個頂點著色器最多可以儲存256指令。</span><span class="sxs-lookup"><span data-stu-id="ef033-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="ef033-147">執行的指令數目可能會更高 (因為迴圈/rep 支援) ，且受限於 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)的上限，其應至少為0xffff。</span><span class="sxs-lookup"><span data-stu-id="ef033-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef033-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef033-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef033-149">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ef033-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 