---
title: setp_comp-ps
description: 設定述詞註冊。 |setp_comp-ps
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196066"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="d141c-104">setp \_ comp-ps</span><span class="sxs-lookup"><span data-stu-id="d141c-104">setp\_comp - ps</span></span>

<span data-ttu-id="d141c-105">設定述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="d141c-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d141c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d141c-106">Syntax</span></span>



| <span data-ttu-id="d141c-107">setp \_ comp dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="d141c-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="d141c-108">其中：</span><span class="sxs-lookup"><span data-stu-id="d141c-108">Where:</span></span>

-   <span data-ttu-id="d141c-109">\_comp 是兩個來源暫存器之間的每個通道比較。</span><span class="sxs-lookup"><span data-stu-id="d141c-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="d141c-110">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d141c-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="d141c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d141c-111">Syntax</span></span> | <span data-ttu-id="d141c-112">比較</span><span class="sxs-lookup"><span data-stu-id="d141c-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="d141c-113">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="d141c-113">\_gt</span></span>   | <span data-ttu-id="d141c-114">大於</span><span class="sxs-lookup"><span data-stu-id="d141c-114">Greater than</span></span>          |
    | <span data-ttu-id="d141c-115">\_淺色</span><span class="sxs-lookup"><span data-stu-id="d141c-115">\_lt</span></span>   | <span data-ttu-id="d141c-116">小於</span><span class="sxs-lookup"><span data-stu-id="d141c-116">Less than</span></span>             |
    | <span data-ttu-id="d141c-117">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="d141c-117">\_ge</span></span>   | <span data-ttu-id="d141c-118">大於或等於</span><span class="sxs-lookup"><span data-stu-id="d141c-118">Greater than or equal</span></span> |
    | <span data-ttu-id="d141c-119">\_樂</span><span class="sxs-lookup"><span data-stu-id="d141c-119">\_le</span></span>   | <span data-ttu-id="d141c-120">小於或等於</span><span class="sxs-lookup"><span data-stu-id="d141c-120">Less than or equal</span></span>    |
    | <span data-ttu-id="d141c-121">\_情 商</span><span class="sxs-lookup"><span data-stu-id="d141c-121">\_eq</span></span>   | <span data-ttu-id="d141c-122">等於</span><span class="sxs-lookup"><span data-stu-id="d141c-122">Equal to</span></span>              |
    | <span data-ttu-id="d141c-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="d141c-123">\_ne</span></span>   | <span data-ttu-id="d141c-124">不等於</span><span class="sxs-lookup"><span data-stu-id="d141c-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="d141c-125">dst 是述詞 [登錄 register，](dx9-graphics-reference-asm-ps-registers-predicate.md) p0。</span><span class="sxs-lookup"><span data-stu-id="d141c-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="d141c-126">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d141c-126">src0 is a source register.</span></span>
-   <span data-ttu-id="d141c-127">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d141c-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d141c-128">備註</span><span class="sxs-lookup"><span data-stu-id="d141c-128">Remarks</span></span>



| <span data-ttu-id="d141c-129">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="d141c-129">Pixel shader versions</span></span> | <span data-ttu-id="d141c-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="d141c-130">1\_1</span></span> | <span data-ttu-id="d141c-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="d141c-131">1\_2</span></span> | <span data-ttu-id="d141c-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d141c-132">1\_3</span></span> | <span data-ttu-id="d141c-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="d141c-133">1\_4</span></span> | <span data-ttu-id="d141c-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d141c-134">2\_0</span></span> | <span data-ttu-id="d141c-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d141c-135">2\_x</span></span> | <span data-ttu-id="d141c-136">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d141c-136">2\_sw</span></span> | <span data-ttu-id="d141c-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d141c-137">3\_0</span></span> | <span data-ttu-id="d141c-138">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d141c-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d141c-139">setp \_ 複合</span><span class="sxs-lookup"><span data-stu-id="d141c-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="d141c-140">x</span><span class="sxs-lookup"><span data-stu-id="d141c-140">x</span></span>    | <span data-ttu-id="d141c-141">x</span><span class="sxs-lookup"><span data-stu-id="d141c-141">x</span></span>     | <span data-ttu-id="d141c-142">x</span><span class="sxs-lookup"><span data-stu-id="d141c-142">x</span></span>    | <span data-ttu-id="d141c-143">x</span><span class="sxs-lookup"><span data-stu-id="d141c-143">x</span></span>     |



 

<span data-ttu-id="d141c-144">此指示的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="d141c-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="d141c-145">針對可根據目的地寫入遮罩寫入的每個通道，請在 src0 與 src1 的對應通道之間儲存比較作業的布林結果，) 之後 (的來源修飾詞 swizzles 已解決。</span><span class="sxs-lookup"><span data-stu-id="d141c-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="d141c-146">來源暫存器允許指定任意元件 swizzles。</span><span class="sxs-lookup"><span data-stu-id="d141c-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="d141c-147">目的地登錄允許任意的寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="d141c-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="d141c-148">Dst 註冊必須是述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="d141c-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="d141c-149">套用述詞註冊</span><span class="sxs-lookup"><span data-stu-id="d141c-149">Applying the Predicate Register</span></span>

<span data-ttu-id="d141c-150">當述詞登錄使用 setp comp 初始化之後 \_ ，就可以用它來控制每個元件的指令。</span><span class="sxs-lookup"><span data-stu-id="d141c-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="d141c-151">語法如下：</span><span class="sxs-lookup"><span data-stu-id="d141c-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="d141c-152">其中：</span><span class="sxs-lookup"><span data-stu-id="d141c-152">Where:</span></span>

-   <span data-ttu-id="d141c-153">\[!\] 是選擇性的布林值</span><span class="sxs-lookup"><span data-stu-id="d141c-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="d141c-154">p0 是述詞註冊</span><span class="sxs-lookup"><span data-stu-id="d141c-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="d141c-155">\[swizzle \] 是選擇性的 swizzle，可套用至述詞登錄的內容，再使用它來遮罩指令。</span><span class="sxs-lookup"><span data-stu-id="d141c-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="d141c-156">可用的 swizzles 為：. xyzw (預設值，但未指定) 或任何複寫 swizzle：. x/. y/g、. z/. b 或. a/w。</span><span class="sxs-lookup"><span data-stu-id="d141c-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="d141c-157">指令為任何 aritmetic 或材質指令。</span><span class="sxs-lookup"><span data-stu-id="d141c-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="d141c-158">這不可以是靜態或動態的流程式控制制指令。</span><span class="sxs-lookup"><span data-stu-id="d141c-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="d141c-159">dest、src0、.。。是指令所需的暫存器</span><span class="sxs-lookup"><span data-stu-id="d141c-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="d141c-160">假設述詞登錄已設定為 (true、true、false、false) 元件值，則可以套用至這個指令：</span><span class="sxs-lookup"><span data-stu-id="d141c-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="d141c-161">若要執行2個元件，請新增。</span><span class="sxs-lookup"><span data-stu-id="d141c-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="d141c-162">系統將不會寫入 r1 的 z 和 w 元件，因為述詞註冊在元件 z 和 w 中包含 false。</span><span class="sxs-lookup"><span data-stu-id="d141c-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="d141c-163">將述詞暫存器套用至算術或材質指令會將其指示位置計數增加1。</span><span class="sxs-lookup"><span data-stu-id="d141c-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="d141c-164">[如果 pred-ps](if-pred---ps.md)、 [callnz pred-ps](callnz-pred---ps.md)和[breakp ps](break-p---ps.md)指示，也可以將述詞登錄套用至。</span><span class="sxs-lookup"><span data-stu-id="d141c-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="d141c-165">使用述詞註冊時，這些流程式控制制指示不會增加指令位置計數。</span><span class="sxs-lookup"><span data-stu-id="d141c-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d141c-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="d141c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d141c-167">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="d141c-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




