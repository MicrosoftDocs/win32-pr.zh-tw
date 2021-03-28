---
title: ps_2_x
description: 可程式化的圖元著色器是由一組操作圖元資料的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990975"
---
# <a name="ps_2_x"></a><span data-ttu-id="2af86-105">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2af86-105">ps\_2\_x</span></span>

<span data-ttu-id="2af86-106">可程式化的圖元著色器是由一組操作圖元資料的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="2af86-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="2af86-107">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="2af86-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="2af86-108">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="2af86-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="2af86-109">[ps \_ 2 \_ x 指示](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="2af86-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="2af86-110">[ps \_ 2 \_ x 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) 程式會列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="2af86-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="2af86-111">[](dx9-graphics-reference-asm-ps-registers-modifiers.md)修飾詞用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="2af86-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="2af86-112">[目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="2af86-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="2af86-113">[圖元著色器來源暫存器](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) 修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="2af86-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="2af86-114">[[來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="2af86-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="2af86-115">動態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="2af86-115">Dynamic Flow Control</span></span>

<span data-ttu-id="2af86-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)代表動態流程式控制制指示的嵌套深度：[如果](if-bool---ps.md)[是，則為，如果是 \_](if-comp---ps.md) [ \_ pred](if-pred---ps.md)、[斷路](break---ps.md)和 break，[則 \_](break-comp---ps.md)為。</span><span class="sxs-lookup"><span data-stu-id="2af86-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="2af86-117">此值等於 if comp 區塊的嵌套深度 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2af86-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="2af86-118">如果此上限為零，則裝置不支援動態流程式控制制指示。</span><span class="sxs-lookup"><span data-stu-id="2af86-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="2af86-119">臨時暫存器數目</span><span class="sxs-lookup"><span data-stu-id="2af86-119">Number of Temporary Registers</span></span>

<span data-ttu-id="2af86-120">裝置支援的臨時暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="2af86-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="2af86-121">範圍是從12到32。</span><span class="sxs-lookup"><span data-stu-id="2af86-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="2af86-122">靜態流程式控制制的嵌套深度</span><span class="sxs-lookup"><span data-stu-id="2af86-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="2af86-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)代表兩種靜態流程式控制制指令類型的嵌套深度：[迴圈](loop---ps.md)  / [代表](rep---ps.md)和 [呼叫](call---ps.md)  / [callnz](callnz-bool---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="2af86-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="2af86-124">迴圈/rep 指令可以嵌套至 **StaticFlowControlDepth** 深層。</span><span class="sxs-lookup"><span data-stu-id="2af86-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="2af86-125">呼叫/callnz 指令可以獨立地嵌套至 **StaticFlowControlDepth** 深層。</span><span class="sxs-lookup"><span data-stu-id="2af86-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="2af86-126">指令位置數目</span><span class="sxs-lookup"><span data-stu-id="2af86-126">Number of Instruction Slots</span></span>

<span data-ttu-id="2af86-127">指令位置數目的範圍可從96到最大值512，並由 [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)指定。</span><span class="sxs-lookup"><span data-stu-id="2af86-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="2af86-128">**MaxPixelShaderInstructionsExecuted** 會定義可執行檔指令總數。</span><span class="sxs-lookup"><span data-stu-id="2af86-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="2af86-129">這可能會大於迴圈和副程式呼叫所造成的指令位置數目。</span><span class="sxs-lookup"><span data-stu-id="2af86-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="2af86-130">任意 Swizzle</span><span class="sxs-lookup"><span data-stu-id="2af86-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="2af86-131">如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，則會支援任意 swizzle。</span><span class="sxs-lookup"><span data-stu-id="2af86-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="2af86-132">請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)。</span><span class="sxs-lookup"><span data-stu-id="2af86-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="2af86-133">漸層指令</span><span class="sxs-lookup"><span data-stu-id="2af86-133">Gradient Instructions</span></span>

<span data-ttu-id="2af86-134">如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就會支援漸層指令。</span><span class="sxs-lookup"><span data-stu-id="2af86-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="2af86-135">請參閱 [dsx-ps](dsx---ps.md)、 [dsy-](dsy---ps.md)ps 和 [texldd-ps](texldd---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="2af86-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="2af86-136">預測</span><span class="sxs-lookup"><span data-stu-id="2af86-136">Predication</span></span>

<span data-ttu-id="2af86-137">如果已設定 [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，則支援指示 PREDICATION。</span><span class="sxs-lookup"><span data-stu-id="2af86-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="2af86-138">請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="2af86-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="2af86-139">相依讀取限制</span><span class="sxs-lookup"><span data-stu-id="2af86-139">Dependent Read Limit</span></span>

<span data-ttu-id="2af86-140">如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就不會有相依的讀取限制。</span><span class="sxs-lookup"><span data-stu-id="2af86-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="2af86-141">材質指令限制</span><span class="sxs-lookup"><span data-stu-id="2af86-141">Texture Instruction Limit</span></span>

<span data-ttu-id="2af86-142">如果設定了 [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) ，就不會有紋理指示的限制。</span><span class="sxs-lookup"><span data-stu-id="2af86-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="2af86-143">取樣器計數</span><span class="sxs-lookup"><span data-stu-id="2af86-143">Sampler Count</span></span>

<span data-ttu-id="2af86-144">可用的紋理取樣器數目是16。</span><span class="sxs-lookup"><span data-stu-id="2af86-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2af86-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="2af86-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af86-146">圖元著色器</span><span class="sxs-lookup"><span data-stu-id="2af86-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 