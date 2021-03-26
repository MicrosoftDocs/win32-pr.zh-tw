---
title: 圖元著色器差異
description: 圖元著色器差異
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375689"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="9f3b5-103">圖元著色器差異</span><span class="sxs-lookup"><span data-stu-id="9f3b5-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="9f3b5-104">指令插槽</span><span class="sxs-lookup"><span data-stu-id="9f3b5-104">Instruction Slots</span></span>

<span data-ttu-id="9f3b5-105">每個版本都支援不同數目的最大指令插槽。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="9f3b5-106">版本</span><span class="sxs-lookup"><span data-stu-id="9f3b5-106">Version</span></span>  | <span data-ttu-id="9f3b5-107">指令位置數目上限</span><span class="sxs-lookup"><span data-stu-id="9f3b5-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3b5-108">ps \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9f3b5-108">ps\_1\_1</span></span> | <span data-ttu-id="9f3b5-109">4材質 + 8 算術</span><span class="sxs-lookup"><span data-stu-id="9f3b5-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="9f3b5-110">ps \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9f3b5-110">ps\_1\_2</span></span> | <span data-ttu-id="9f3b5-111">4材質 + 8 算術</span><span class="sxs-lookup"><span data-stu-id="9f3b5-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="9f3b5-112">ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9f3b5-112">ps\_1\_3</span></span> | <span data-ttu-id="9f3b5-113">4材質 + 8 算術</span><span class="sxs-lookup"><span data-stu-id="9f3b5-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="9f3b5-114">ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9f3b5-114">ps\_1\_4</span></span> | <span data-ttu-id="9f3b5-115">6個材質 + 每個階段8個算術</span><span class="sxs-lookup"><span data-stu-id="9f3b5-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="9f3b5-116">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f3b5-116">ps\_2\_0</span></span> | <span data-ttu-id="9f3b5-117">32材質 + 64 算術</span><span class="sxs-lookup"><span data-stu-id="9f3b5-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="9f3b5-118">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9f3b5-118">ps\_2\_x</span></span> | <span data-ttu-id="9f3b5-119">最小值為96，最多可達 D3DCAPS9 中的插槽數目。D3DPSHADERCAPS2 \_ 0. NumInstructionSlots。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="9f3b5-120">請參閱 D3DPSHADERCAPS2 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="9f3b5-121">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f3b5-121">ps\_3\_0</span></span> | <span data-ttu-id="9f3b5-122">最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="9f3b5-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="9f3b5-123">請參閱 D3DPSHADERCAPS2 \_ 0。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="9f3b5-124">如需軟體著色器限制的詳細資訊，請參閱 [軟體著色](dx9-graphics-reference-asm-software-shaders.md)器。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="9f3b5-125">流程式控制制的嵌套限制</span><span class="sxs-lookup"><span data-stu-id="9f3b5-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="9f3b5-126">請參閱 [流程式控制制限制](dx9-graphics-reference-asm-ps-instructions-flow-control.md)。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="9f3b5-127">ps \_ 1 \_ x 功能</span><span class="sxs-lookup"><span data-stu-id="9f3b5-127">ps\_1\_x Features</span></span>

<span data-ttu-id="9f3b5-128">新的指示：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-128">New instructions:</span></span>

<span data-ttu-id="9f3b5-129">請參閱 [ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4 指示](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="9f3b5-130">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-130">New registers:</span></span>

<span data-ttu-id="9f3b5-131">請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="9f3b5-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="9f3b5-132">ps \_ 2 \_ 0 功能</span><span class="sxs-lookup"><span data-stu-id="9f3b5-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="9f3b5-133">新功能︰</span><span class="sxs-lookup"><span data-stu-id="9f3b5-133">New features:</span></span>

-   <span data-ttu-id="9f3b5-134">三個新的 swizzles-. yzxw、. zxyw、. wzyx</span><span class="sxs-lookup"><span data-stu-id="9f3b5-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="9f3b5-135"> (r) 增加至12的[暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md)數目 \#</span><span class="sxs-lookup"><span data-stu-id="9f3b5-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="9f3b5-136">[常數浮點數](dx9-graphics-reference-asm-ps-registers-constant-float.md)暫存器 (c \#) 增加到32的數目</span><span class="sxs-lookup"><span data-stu-id="9f3b5-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="9f3b5-137"> (t) 增加為8的[材質座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)暫存器數目 \#</span><span class="sxs-lookup"><span data-stu-id="9f3b5-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="9f3b5-138">新的指示：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-138">New instructions:</span></span>

-   <span data-ttu-id="9f3b5-139">設定指示- [dcl- (sm2、sm3-ps asm) ](dcl---ps.md)、 [dcl \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-140">算術指示- [abs-ps](abs---ps.md)、 [crs-ps](crs---ps.md)、 [dp2add/ps](dp2add---ps.md)、 [exp-ps](exp---ps.md)、 [frc-ps](frc---ps.md)、 [log-ps](log---ps.md)、 [m3x2-ps](m3x2---ps.md)、 [m3x3-ps](m3x3---ps.md)、 [m3x4-ps](m3x4---ps.md)、 [m4x3-ps](m4x3---ps.md)、 [m4x4](m4x4---ps.md) [-ps](nrm---ps.md)、 [max-](max---ps.md) [ps、](min---ps.md) [rcp-ps](rcp---ps.md) [、nrm-](rsq---ps.md)ps、 [](pow---ps.md) [pow-](sincos---ps.md) ps</span><span class="sxs-lookup"><span data-stu-id="9f3b5-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-141">材質指示- [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md) (不同的語法) 、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="9f3b5-142">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-142">New registers:</span></span>

-   <span data-ttu-id="9f3b5-143">[ (Direct3D 9 asm-ps)  (s 的取樣 ](dx9-graphics-reference-asm-ps-registers-sampler.md) 器 \#) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="9f3b5-144">ps \_ 2 \_ x 功能</span><span class="sxs-lookup"><span data-stu-id="9f3b5-144">ps\_2\_x Features</span></span>

<span data-ttu-id="9f3b5-145">新功能 (請參閱 [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)。 ) ：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="9f3b5-146">動態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="9f3b5-146">Dynamic flow control</span></span>
-   <span data-ttu-id="9f3b5-147">靜態流程式控制制</span><span class="sxs-lookup"><span data-stu-id="9f3b5-147">Static flow control</span></span>
-   <span data-ttu-id="9f3b5-148">動態和靜態流程式控制制指示的嵌套</span><span class="sxs-lookup"><span data-stu-id="9f3b5-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="9f3b5-149"> (r) 增加的[暫存](dx9-graphics-reference-asm-ps-registers-temporary.md)登錄數目 \#</span><span class="sxs-lookup"><span data-stu-id="9f3b5-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="9f3b5-150">任意來源 swizzle</span><span class="sxs-lookup"><span data-stu-id="9f3b5-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="9f3b5-151">漸層指令</span><span class="sxs-lookup"><span data-stu-id="9f3b5-151">Gradient instructions</span></span>
-   <span data-ttu-id="9f3b5-152">預測</span><span class="sxs-lookup"><span data-stu-id="9f3b5-152">Predication</span></span>
-   <span data-ttu-id="9f3b5-153">沒有相依材質讀取限制</span><span class="sxs-lookup"><span data-stu-id="9f3b5-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="9f3b5-154">沒有紋理指示限制</span><span class="sxs-lookup"><span data-stu-id="9f3b5-154">No texture instruction limit</span></span>

<span data-ttu-id="9f3b5-155">新的指示：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-155">New instructions:</span></span>

-   <span data-ttu-id="9f3b5-156">靜態流程式控制制指示- [如果 bool-ps](if-bool---ps.md)、 [call](call---ps.md)、 [callnz bool-ps](callnz-bool---ps.md)、 [else-ps](else---ps.md)、 [endif-ps](endif---ps.md)、 [rep-ps](rep---ps.md)、 [endrep-ps](endrep---ps.md)、 [label-ps](label---ps.md)、 [ret-ps](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-157">動態流程式控制制指示-[斷路-ps](break---ps.md)、 [break、 \_ ps](break-comp---ps.md)、 [breakp-ps](break-p---ps.md)、 [callnz pred-ps](callnz-pred---ps.md)（如果[ \_ ](if-comp---ps.md) [pred-ps](if-pred---ps.md)、 [setp \_ comp ps](setp-comp---ps.md) ）</span><span class="sxs-lookup"><span data-stu-id="9f3b5-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-158">算術指示- [dsx-ps](dsx---ps.md)、 [dsy-ps](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-159">材質指令- [texldd-ps](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="9f3b5-160">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-160">New registers:</span></span>

-   <span data-ttu-id="9f3b5-161">述詞[Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="9f3b5-162">ps \_ 3 \_ 0 功能</span><span class="sxs-lookup"><span data-stu-id="9f3b5-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="9f3b5-163">新功能︰</span><span class="sxs-lookup"><span data-stu-id="9f3b5-163">New features:</span></span>

-   <span data-ttu-id="9f3b5-164">合併10個 [輸入 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \#) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="9f3b5-165">[](dx9-graphics-reference-asm-ps-registers-input-color.md) \# 使用[迴圈計數器 register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL (v) 可編制索引的輸入色彩暫存器) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="9f3b5-166"> (r [](dx9-graphics-reference-asm-ps-registers-temporary.md) \#) 增加到32的暫存登錄數目</span><span class="sxs-lookup"><span data-stu-id="9f3b5-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="9f3b5-167"> (c) 增加到224的[常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)的數目 \#</span><span class="sxs-lookup"><span data-stu-id="9f3b5-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="9f3b5-168">新的指示：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-168">New instructions:</span></span>

-   <span data-ttu-id="9f3b5-169">設定指令- [dcl \_ 語義 (sm3-ps asm) ](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-170">靜態流程指示- [迴圈-ps](loop---ps.md)、 [endloop-ps](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="9f3b5-171">算術指令- [sincos-ps](sincos---ps.md) (新的語法) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="9f3b5-172">材質指令- [texldl-ps](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="9f3b5-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="9f3b5-173">新的暫存器：</span><span class="sxs-lookup"><span data-stu-id="9f3b5-173">New registers:</span></span>

-   <span data-ttu-id="9f3b5-174">[輸入 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \#) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="9f3b5-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="9f3b5-176">[臉部報名](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace) </span><span class="sxs-lookup"><span data-stu-id="9f3b5-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f3b5-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f3b5-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f3b5-178">圖元著色器</span><span class="sxs-lookup"><span data-stu-id="9f3b5-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 