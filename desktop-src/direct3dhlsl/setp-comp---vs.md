---
title: setp_comp-vs
description: 設定述詞註冊。 |setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386384"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="d8364-104">setp \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="d8364-104">setp\_comp - vs</span></span>

<span data-ttu-id="d8364-105">設定述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="d8364-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8364-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8364-106">Syntax</span></span>



| <span data-ttu-id="d8364-107">setp \_ comp dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="d8364-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="d8364-108">其中：</span><span class="sxs-lookup"><span data-stu-id="d8364-108">Where:</span></span>

-   <span data-ttu-id="d8364-109">\_comp 是兩個來源暫存器之間的每個通道比較。</span><span class="sxs-lookup"><span data-stu-id="d8364-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="d8364-110">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d8364-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="d8364-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8364-111">Syntax</span></span> | <span data-ttu-id="d8364-112">比較</span><span class="sxs-lookup"><span data-stu-id="d8364-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="d8364-113">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="d8364-113">\_gt</span></span>   | <span data-ttu-id="d8364-114">大於</span><span class="sxs-lookup"><span data-stu-id="d8364-114">Greater than</span></span>          |
    | <span data-ttu-id="d8364-115">\_淺色</span><span class="sxs-lookup"><span data-stu-id="d8364-115">\_lt</span></span>   | <span data-ttu-id="d8364-116">小於</span><span class="sxs-lookup"><span data-stu-id="d8364-116">Less than</span></span>             |
    | <span data-ttu-id="d8364-117">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="d8364-117">\_ge</span></span>   | <span data-ttu-id="d8364-118">大於或等於</span><span class="sxs-lookup"><span data-stu-id="d8364-118">Greater than or equal</span></span> |
    | <span data-ttu-id="d8364-119">\_樂</span><span class="sxs-lookup"><span data-stu-id="d8364-119">\_le</span></span>   | <span data-ttu-id="d8364-120">小於或等於</span><span class="sxs-lookup"><span data-stu-id="d8364-120">Less than or equal</span></span>    |
    | <span data-ttu-id="d8364-121">\_情 商</span><span class="sxs-lookup"><span data-stu-id="d8364-121">\_eq</span></span>   | <span data-ttu-id="d8364-122">等於</span><span class="sxs-lookup"><span data-stu-id="d8364-122">Equal to</span></span>              |
    | <span data-ttu-id="d8364-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="d8364-123">\_ne</span></span>   | <span data-ttu-id="d8364-124">不等於</span><span class="sxs-lookup"><span data-stu-id="d8364-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="d8364-125">dst 是述詞 [登錄 register，](dx9-graphics-reference-asm-vs-registers-predicate.md) p0。</span><span class="sxs-lookup"><span data-stu-id="d8364-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="d8364-126">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d8364-126">src0 is a source register.</span></span>
-   <span data-ttu-id="d8364-127">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d8364-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8364-128">備註</span><span class="sxs-lookup"><span data-stu-id="d8364-128">Remarks</span></span>



| <span data-ttu-id="d8364-129">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="d8364-129">Vertex shader versions</span></span> | <span data-ttu-id="d8364-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="d8364-130">1\_1</span></span> | <span data-ttu-id="d8364-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8364-131">2\_0</span></span> | <span data-ttu-id="d8364-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d8364-132">2\_x</span></span> | <span data-ttu-id="d8364-133">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8364-133">2\_sw</span></span> | <span data-ttu-id="d8364-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8364-134">3\_0</span></span> | <span data-ttu-id="d8364-135">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8364-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d8364-136">setp \_ 複合</span><span class="sxs-lookup"><span data-stu-id="d8364-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="d8364-137">x</span><span class="sxs-lookup"><span data-stu-id="d8364-137">x</span></span>    | <span data-ttu-id="d8364-138">x</span><span class="sxs-lookup"><span data-stu-id="d8364-138">x</span></span>     | <span data-ttu-id="d8364-139">x</span><span class="sxs-lookup"><span data-stu-id="d8364-139">x</span></span>    | <span data-ttu-id="d8364-140">x</span><span class="sxs-lookup"><span data-stu-id="d8364-140">x</span></span>     |



 

<span data-ttu-id="d8364-141">此指示的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="d8364-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="d8364-142">針對可根據目的地寫入遮罩寫入的每個通道，請在 src0 與 src1 的對應通道之間儲存比較作業的布林結果，) 之後 (的來源修飾詞 swizzles 已解決。</span><span class="sxs-lookup"><span data-stu-id="d8364-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="d8364-143">來源暫存器允許指定任意元件 swizzles。</span><span class="sxs-lookup"><span data-stu-id="d8364-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="d8364-144">目的地登錄允許任意的寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="d8364-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="d8364-145">Dest 註冊必須是述詞登錄。</span><span class="sxs-lookup"><span data-stu-id="d8364-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="d8364-146">套用述詞註冊</span><span class="sxs-lookup"><span data-stu-id="d8364-146">Applying the Predicate Register</span></span>

<span data-ttu-id="d8364-147">使用 setp 初始化述詞註冊之後，就可以使用它來控制每個元件的指令。</span><span class="sxs-lookup"><span data-stu-id="d8364-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="d8364-148">語法如下：</span><span class="sxs-lookup"><span data-stu-id="d8364-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="d8364-149">其中：</span><span class="sxs-lookup"><span data-stu-id="d8364-149">Where:</span></span>

-   <span data-ttu-id="d8364-150">\[!\] 是選擇性的布林值</span><span class="sxs-lookup"><span data-stu-id="d8364-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="d8364-151">p0 是述詞註冊</span><span class="sxs-lookup"><span data-stu-id="d8364-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="d8364-152">\[swizzle \] 是選擇性的 swizzle，可套用至述詞登錄的內容，再使用它來遮罩指令。</span><span class="sxs-lookup"><span data-stu-id="d8364-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="d8364-153">可用的 swizzles 為：. xyzw (預設值，但未指定) 或任何複寫 swizzle：. x/. y/g、. z/. b 或. a/w。</span><span class="sxs-lookup"><span data-stu-id="d8364-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="d8364-154">指令為任何 aritmetic 或材質指令。</span><span class="sxs-lookup"><span data-stu-id="d8364-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="d8364-155">這不可以是靜態或動態的流程式控制制指令。</span><span class="sxs-lookup"><span data-stu-id="d8364-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="d8364-156">dest、srcReg、.。。是指令所需的暫存器</span><span class="sxs-lookup"><span data-stu-id="d8364-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="d8364-157">假設述詞登錄已設定為 (true、true、false、false) 元件值，則可以套用至這個指令：</span><span class="sxs-lookup"><span data-stu-id="d8364-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="d8364-158">若要執行2個元件，請新增。</span><span class="sxs-lookup"><span data-stu-id="d8364-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="d8364-159">因為述詞註冊在元件 z 和 w 中包含 false，所以不會寫入 r2 的 x 和 y 元件。</span><span class="sxs-lookup"><span data-stu-id="d8364-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="d8364-160">將述詞暫存器套用至算術或材質指令會將其指示位置計數增加1。</span><span class="sxs-lookup"><span data-stu-id="d8364-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="d8364-161">[如果 pred-vs](if-pred---vs.md)、 [callnz pred-vs](callnz-pred---vs.md)和[breakp-vs](breakp---vs.md)指令，也可以將述詞登錄套用至。</span><span class="sxs-lookup"><span data-stu-id="d8364-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="d8364-162">使用述詞註冊時，這些流程式控制制指示不會增加指令位置計數。</span><span class="sxs-lookup"><span data-stu-id="d8364-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8364-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8364-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8364-164">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="d8364-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




