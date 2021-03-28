---
title: if_comp-vs
description: 啟動 if bool-vs .。。else-vs .。。endif-vs block，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990703"
---
# <a name="if_comp---vs"></a><span data-ttu-id="cd7c9-104">如果是 \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="cd7c9-104">if\_comp - vs</span></span>

<span data-ttu-id="cd7c9-105">啟動 [if bool-vs](if-bool---vs.md).。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) block，具有以可在著色器中計算之值為基礎的條件。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="cd7c9-106">此指令是用來根據條件略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7c9-107">Syntax</span></span>



| <span data-ttu-id="cd7c9-108">if \_ comp src0、src1</span><span class="sxs-lookup"><span data-stu-id="cd7c9-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="cd7c9-109">其中：</span><span class="sxs-lookup"><span data-stu-id="cd7c9-109">Where:</span></span>

-   <span data-ttu-id="cd7c9-110">\_comp 是兩個來源暫存器之間的比較。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="cd7c9-111">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="cd7c9-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="cd7c9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7c9-112">Syntax</span></span> | <span data-ttu-id="cd7c9-113">比較</span><span class="sxs-lookup"><span data-stu-id="cd7c9-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="cd7c9-114">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="cd7c9-114">\_gt</span></span>   | <span data-ttu-id="cd7c9-115">大於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-115">Greater than</span></span>          |
    | <span data-ttu-id="cd7c9-116">\_淺色</span><span class="sxs-lookup"><span data-stu-id="cd7c9-116">\_lt</span></span>   | <span data-ttu-id="cd7c9-117">小於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-117">Less than</span></span>             |
    | <span data-ttu-id="cd7c9-118">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="cd7c9-118">\_ge</span></span>   | <span data-ttu-id="cd7c9-119">大於或等於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-119">Greater than or equal</span></span> |
    | <span data-ttu-id="cd7c9-120">\_樂</span><span class="sxs-lookup"><span data-stu-id="cd7c9-120">\_le</span></span>   | <span data-ttu-id="cd7c9-121">小於或等於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-121">Less than or equal</span></span>    |
    | <span data-ttu-id="cd7c9-122">\_情 商</span><span class="sxs-lookup"><span data-stu-id="cd7c9-122">\_eq</span></span>   | <span data-ttu-id="cd7c9-123">等於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-123">Equal to</span></span>              |
    | <span data-ttu-id="cd7c9-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="cd7c9-124">\_ne</span></span>   | <span data-ttu-id="cd7c9-125">不等於</span><span class="sxs-lookup"><span data-stu-id="cd7c9-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="cd7c9-126">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-126">src0 is a source register.</span></span> <span data-ttu-id="cd7c9-127">需要複寫 swizzle 才能選取元件。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="cd7c9-128">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-128">src1 is a source register.</span></span> <span data-ttu-id="cd7c9-129">需要複寫 swizzle 才能選取元件。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7c9-130">備註</span><span class="sxs-lookup"><span data-stu-id="cd7c9-130">Remarks</span></span>



| <span data-ttu-id="cd7c9-131">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="cd7c9-131">Vertex shader versions</span></span> | <span data-ttu-id="cd7c9-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd7c9-132">1\_1</span></span> | <span data-ttu-id="cd7c9-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd7c9-133">2\_0</span></span> | <span data-ttu-id="cd7c9-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd7c9-134">2\_x</span></span> | <span data-ttu-id="cd7c9-135">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cd7c9-135">2\_sw</span></span> | <span data-ttu-id="cd7c9-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd7c9-136">3\_0</span></span> | <span data-ttu-id="cd7c9-137">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cd7c9-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cd7c9-138">若為 \_ comp</span><span class="sxs-lookup"><span data-stu-id="cd7c9-138">if\_comp</span></span>               |      |      | <span data-ttu-id="cd7c9-139">x</span><span class="sxs-lookup"><span data-stu-id="cd7c9-139">x</span></span>    | <span data-ttu-id="cd7c9-140">x</span><span class="sxs-lookup"><span data-stu-id="cd7c9-140">x</span></span>     | <span data-ttu-id="cd7c9-141">x</span><span class="sxs-lookup"><span data-stu-id="cd7c9-141">x</span></span>    | <span data-ttu-id="cd7c9-142">x</span><span class="sxs-lookup"><span data-stu-id="cd7c9-142">x</span></span>     |



 

<span data-ttu-id="cd7c9-143">此指令是用來根據條件略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="cd7c9-144">請小心使用浮點數的 equals 和 not equals 比較模式。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="cd7c9-145">因為四捨五入是在浮點計算期間進行，所以可以針對 epsilon 值進行比較， (不) 的非零值，以避免發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="cd7c9-146">限制包含：</span><span class="sxs-lookup"><span data-stu-id="cd7c9-146">Restrictions include:</span></span>

-   <span data-ttu-id="cd7c9-147">如果 \_ 為 .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) 區塊 (以及區塊) 可以嵌套最多24層級的前提。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="cd7c9-148">src0 和 src1 暫存器需要複製 swizzle。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="cd7c9-149">如果 \_ 複合區塊必須以 [else-vs](else---vs.md) 或 [endif-vs](endif---vs.md) 指令結尾。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="cd7c9-150">如果 \_ 為 .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) 區塊無法跨迴圈區塊。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="cd7c9-151">If \_ 複合區塊必須完全在迴圈內，或在 [迴圈和迴圈](loop---vs.md) 中。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="cd7c9-152">範例</span><span class="sxs-lookup"><span data-stu-id="cd7c9-152">Example</span></span>

<span data-ttu-id="cd7c9-153">此指令提供條件式動態流量控制。</span><span class="sxs-lookup"><span data-stu-id="cd7c9-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="cd7c9-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd7c9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd7c9-155">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="cd7c9-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




