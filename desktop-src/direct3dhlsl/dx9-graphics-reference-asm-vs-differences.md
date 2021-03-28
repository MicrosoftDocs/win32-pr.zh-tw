---
title: 頂點著色器差異
description: 頂點著色器差異
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023607"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="639c4-103">頂點著色器差異</span><span class="sxs-lookup"><span data-stu-id="639c4-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="639c4-104">指令插槽</span><span class="sxs-lookup"><span data-stu-id="639c4-104">Instruction Slots</span></span>

<span data-ttu-id="639c4-105">每個版本都支援不同數目的最大指令插槽。</span><span class="sxs-lookup"><span data-stu-id="639c4-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="639c4-106">版本</span><span class="sxs-lookup"><span data-stu-id="639c4-106">Version</span></span>  | <span data-ttu-id="639c4-107">指令位置數目上限</span><span class="sxs-lookup"><span data-stu-id="639c4-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639c4-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="639c4-108">vs\_1\_1</span></span> | <span data-ttu-id="639c4-109">128</span><span class="sxs-lookup"><span data-stu-id="639c4-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="639c4-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="639c4-110">vs\_2\_0</span></span> | <span data-ttu-id="639c4-111">256</span><span class="sxs-lookup"><span data-stu-id="639c4-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="639c4-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="639c4-112">vs\_2\_x</span></span> | <span data-ttu-id="639c4-113">256</span><span class="sxs-lookup"><span data-stu-id="639c4-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="639c4-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="639c4-114">vs\_3\_0</span></span> | <span data-ttu-id="639c4-115">最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="639c4-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="639c4-116">請參閱 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)。</span><span class="sxs-lookup"><span data-stu-id="639c4-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="639c4-117">如需軟體著色器限制的詳細資訊，請參閱 [軟體著色](dx9-graphics-reference-asm-software-shaders.md)器。</span><span class="sxs-lookup"><span data-stu-id="639c4-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="639c4-118">流程式控制制的嵌套限制</span><span class="sxs-lookup"><span data-stu-id="639c4-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="639c4-119">請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。</span><span class="sxs-lookup"><span data-stu-id="639c4-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="639c4-120">vs \_ 1 \_ 1 功能</span><span class="sxs-lookup"><span data-stu-id="639c4-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="639c4-121">新的指示：</span><span class="sxs-lookup"><span data-stu-id="639c4-121">New instructions:</span></span>

<span data-ttu-id="639c4-122">請參閱 [指示-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md)。</span><span class="sxs-lookup"><span data-stu-id="639c4-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="639c4-123">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="639c4-123">New registers:</span></span>

<span data-ttu-id="639c4-124">請參閱暫存器 [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)。</span><span class="sxs-lookup"><span data-stu-id="639c4-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="639c4-125">vs \_ 2 \_ 0 功能</span><span class="sxs-lookup"><span data-stu-id="639c4-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="639c4-126">新功能︰</span><span class="sxs-lookup"><span data-stu-id="639c4-126">New features:</span></span>

-   <span data-ttu-id="639c4-127">靜態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="639c4-127">Static flow control</span></span>
-   <span data-ttu-id="639c4-128">[Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) 的四個元件都可以使用。</span><span class="sxs-lookup"><span data-stu-id="639c4-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="639c4-129">新的指示：</span><span class="sxs-lookup"><span data-stu-id="639c4-129">New instructions:</span></span>

-   <span data-ttu-id="639c4-130">設定指示- [defb-vs](defb---vs.md)、 [defi-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="639c4-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="639c4-131">算術指示- [abs-vs](abs---vs.md)、 [crs-vs](crs---vs.md)、 [lrp-vs](lrp---vs.md)、 [mova-vs](mova---vs.md)、 [nrm-vs](nrm---vs.md)、 [pow-vs](pow---vs.md)、 [登錄-vs](sgn---vs.md)、 [sincos-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="639c4-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="639c4-132">靜態流程式控制制指示-- [call-vs](call---vs.md)、 [callnz bool-vs](callnz-bool---vs.md)、 [else-vs](else---vs.md)、 [endif-vs](endif---vs.md)、 [endloop-vs](endloop---vs.md)、 [endrep-vs](endrep---vs.md)、 [bool-vs](if-bool---vs.md)、 [label-vs](label---vs.md)、[迴圈-](loop---vs.md)vs、 [rep-vs](rep---vs.md)、 [ret](ret---vs.md) -vs</span><span class="sxs-lookup"><span data-stu-id="639c4-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="639c4-133">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="639c4-133">New registers:</span></span>

-   <span data-ttu-id="639c4-134">[常數 Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \#) </span><span class="sxs-lookup"><span data-stu-id="639c4-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="639c4-135">[常數整數 Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (我 \#) </span><span class="sxs-lookup"><span data-stu-id="639c4-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="639c4-136">[迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) </span><span class="sxs-lookup"><span data-stu-id="639c4-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="639c4-137">vs \_ 2 \_ x 功能</span><span class="sxs-lookup"><span data-stu-id="639c4-137">vs\_2\_x Features</span></span>

<span data-ttu-id="639c4-138"> (D3DCAPS9 的新功能。VS20Caps) ：</span><span class="sxs-lookup"><span data-stu-id="639c4-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="639c4-139">動態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="639c4-139">Dynamic flow control</span></span>
-   <span data-ttu-id="639c4-140">動態和靜態流程式控制制指示的嵌套</span><span class="sxs-lookup"><span data-stu-id="639c4-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="639c4-141"> (r) 增加的[暫存](dx9-graphics-reference-asm-vs-registers-temporary.md)登錄數目 \#</span><span class="sxs-lookup"><span data-stu-id="639c4-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="639c4-142">預測</span><span class="sxs-lookup"><span data-stu-id="639c4-142">Predication</span></span>

<span data-ttu-id="639c4-143">新的指示：</span><span class="sxs-lookup"><span data-stu-id="639c4-143">New Instructions:</span></span>

-   <span data-ttu-id="639c4-144">動態流程式控制制指示- [break-vs](break---vs.md)、 [break \_ comp-vs](break-comp---vs.md)、 [breakp-vs](breakp---vs.md)、 [callnz pred-vs](callnz-pred---vs.md)、 [if \_ ](if-comp---vs.md) [pred-vs](if-pred---vs.md)、 [setp \_ comp-](setp-comp---vs.md) vs</span><span class="sxs-lookup"><span data-stu-id="639c4-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="639c4-145">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="639c4-145">New registers:</span></span>

-   <span data-ttu-id="639c4-146">述詞[Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0) </span><span class="sxs-lookup"><span data-stu-id="639c4-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="639c4-147">vs \_ 3 \_ 0 功能</span><span class="sxs-lookup"><span data-stu-id="639c4-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="639c4-148">新功能：</span><span class="sxs-lookup"><span data-stu-id="639c4-148">New features :</span></span>

-   <span data-ttu-id="639c4-149">紋理查閱</span><span class="sxs-lookup"><span data-stu-id="639c4-149">Texture lookup</span></span>
-   <span data-ttu-id="639c4-150">可編制索引的 [輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) 暫存器 (o \#) </span><span class="sxs-lookup"><span data-stu-id="639c4-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="639c4-151"> (r [](dx9-graphics-reference-asm-vs-registers-temporary.md) \#) 增加到32的暫存登錄數目</span><span class="sxs-lookup"><span data-stu-id="639c4-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="639c4-152">新的指示：</span><span class="sxs-lookup"><span data-stu-id="639c4-152">New instructions:</span></span>

-   <span data-ttu-id="639c4-153">設定指令- [dcl \_ samplerType (sm3-vs asm) ](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="639c4-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="639c4-154">材質指令- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="639c4-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="639c4-155">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="639c4-155">New registers:</span></span>

-   <span data-ttu-id="639c4-156">[ (Direct3D 9 asm 的取樣器-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \#) </span><span class="sxs-lookup"><span data-stu-id="639c4-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="639c4-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="639c4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="639c4-158">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="639c4-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 