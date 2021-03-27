---
title: if_comp-ps
description: 啟動 if bool-ps .。。其他-ps .。。endif-ps 區塊，具有以可在著色器中計算之值為基礎的條件。 此指令是用來根據條件略過程式碼區塊。
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679100"
---
# <a name="if_comp---ps"></a><span data-ttu-id="b3546-104">如果 \_ 是</span><span class="sxs-lookup"><span data-stu-id="b3546-104">if\_comp - ps</span></span>

<span data-ttu-id="b3546-105">啟動 [if bool-ps](if-bool---ps.md).。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md) 區塊，具有以可在著色器中計算之值為基礎的條件。</span><span class="sxs-lookup"><span data-stu-id="b3546-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="b3546-106">此指令是用來根據條件略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="b3546-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3546-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3546-107">Syntax</span></span>



| <span data-ttu-id="b3546-108">if \_ comp src0、src1</span><span class="sxs-lookup"><span data-stu-id="b3546-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b3546-109">其中：</span><span class="sxs-lookup"><span data-stu-id="b3546-109">Where:</span></span>

-   <span data-ttu-id="b3546-110">\_comp 是兩個來源暫存器之間的比較。</span><span class="sxs-lookup"><span data-stu-id="b3546-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="b3546-111">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="b3546-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="b3546-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3546-112">Syntax</span></span> | <span data-ttu-id="b3546-113">比較</span><span class="sxs-lookup"><span data-stu-id="b3546-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="b3546-114">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="b3546-114">\_gt</span></span>   | <span data-ttu-id="b3546-115">大於</span><span class="sxs-lookup"><span data-stu-id="b3546-115">Greater than</span></span>          |
    | <span data-ttu-id="b3546-116">\_淺色</span><span class="sxs-lookup"><span data-stu-id="b3546-116">\_lt</span></span>   | <span data-ttu-id="b3546-117">小於</span><span class="sxs-lookup"><span data-stu-id="b3546-117">Less than</span></span>             |
    | <span data-ttu-id="b3546-118">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="b3546-118">\_ge</span></span>   | <span data-ttu-id="b3546-119">大於或等於</span><span class="sxs-lookup"><span data-stu-id="b3546-119">Greater than or equal</span></span> |
    | <span data-ttu-id="b3546-120">\_樂</span><span class="sxs-lookup"><span data-stu-id="b3546-120">\_le</span></span>   | <span data-ttu-id="b3546-121">小於或等於</span><span class="sxs-lookup"><span data-stu-id="b3546-121">Less than or equal</span></span>    |
    | <span data-ttu-id="b3546-122">\_情 商</span><span class="sxs-lookup"><span data-stu-id="b3546-122">\_eq</span></span>   | <span data-ttu-id="b3546-123">等於</span><span class="sxs-lookup"><span data-stu-id="b3546-123">Equal to</span></span>              |
    | <span data-ttu-id="b3546-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="b3546-124">\_ne</span></span>   | <span data-ttu-id="b3546-125">不等於</span><span class="sxs-lookup"><span data-stu-id="b3546-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="b3546-126">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="b3546-126">src0 is a source register.</span></span> <span data-ttu-id="b3546-127">需要複寫 swizzle 才能選取元件。</span><span class="sxs-lookup"><span data-stu-id="b3546-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="b3546-128">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="b3546-128">src1 is a source register.</span></span> <span data-ttu-id="b3546-129">需要複寫 swizzle 才能選取元件。</span><span class="sxs-lookup"><span data-stu-id="b3546-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3546-130">備註</span><span class="sxs-lookup"><span data-stu-id="b3546-130">Remarks</span></span>



| <span data-ttu-id="b3546-131">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="b3546-131">Pixel shader versions</span></span> | <span data-ttu-id="b3546-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3546-132">1\_1</span></span> | <span data-ttu-id="b3546-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3546-133">1\_2</span></span> | <span data-ttu-id="b3546-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3546-134">1\_3</span></span> | <span data-ttu-id="b3546-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3546-135">1\_4</span></span> | <span data-ttu-id="b3546-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3546-136">2\_0</span></span> | <span data-ttu-id="b3546-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3546-137">2\_x</span></span> | <span data-ttu-id="b3546-138">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b3546-138">2\_sw</span></span> | <span data-ttu-id="b3546-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3546-139">3\_0</span></span> | <span data-ttu-id="b3546-140">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b3546-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3546-141">若為 \_ comp</span><span class="sxs-lookup"><span data-stu-id="b3546-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="b3546-142">x</span><span class="sxs-lookup"><span data-stu-id="b3546-142">x</span></span>    | <span data-ttu-id="b3546-143">x</span><span class="sxs-lookup"><span data-stu-id="b3546-143">x</span></span>     | <span data-ttu-id="b3546-144">x</span><span class="sxs-lookup"><span data-stu-id="b3546-144">x</span></span>    | <span data-ttu-id="b3546-145">x</span><span class="sxs-lookup"><span data-stu-id="b3546-145">x</span></span>     |



 

<span data-ttu-id="b3546-146">此指令是用來根據條件略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="b3546-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="b3546-147">請小心使用浮點數的 equals 和 not equals 比較模式。</span><span class="sxs-lookup"><span data-stu-id="b3546-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="b3546-148">因為四捨五入是在浮點計算期間進行，所以可以針對 epsilon 值進行比較， (不) 的非零值，以避免發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3546-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="b3546-149">限制包含：</span><span class="sxs-lookup"><span data-stu-id="b3546-149">Restrictions include:</span></span>

-   <span data-ttu-id="b3546-150">如果 \_ 為 .。。[其他-ps](else---ps.md).。。[如果](if-bool---ps.md)[區塊) ](endif---ps.md)最多可嵌套至24層，則會將 (與前提搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b3546-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="b3546-151">src0 和 src1 暫存器需要複製 swizzle。</span><span class="sxs-lookup"><span data-stu-id="b3546-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="b3546-152">如果 \_ 複合區塊必須以 [else-vs](else---vs.md) 或 [endif-vs](endif---vs.md) 指令結尾。</span><span class="sxs-lookup"><span data-stu-id="b3546-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="b3546-153">如果 \_ 為 .。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md) 區塊無法跨迴圈區塊。</span><span class="sxs-lookup"><span data-stu-id="b3546-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="b3546-154">If \_ 複合區塊必須完全在迴圈區塊內部或外部。</span><span class="sxs-lookup"><span data-stu-id="b3546-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="b3546-155">範例</span><span class="sxs-lookup"><span data-stu-id="b3546-155">Example</span></span>

<span data-ttu-id="b3546-156">此指令提供條件式動態流量控制。</span><span class="sxs-lookup"><span data-stu-id="b3546-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="b3546-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3546-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3546-158">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="b3546-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




