---
title: break_comp-ps
description: 根據每個元件的比較，中斷最近 endloop ps 或 endrep ps 的目前迴圈。
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092455"
---
# <a name="break_comp---ps"></a><span data-ttu-id="c3151-103">中斷 \_ 複合-ps</span><span class="sxs-lookup"><span data-stu-id="c3151-103">break\_comp - ps</span></span>

<span data-ttu-id="c3151-104">根據每個元件的比較，中斷最近 [endloop ps](endloop---ps.md) 或 [endrep ps](endrep---ps.md)的目前迴圈。</span><span class="sxs-lookup"><span data-stu-id="c3151-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3151-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3151-105">Syntax</span></span>



| <span data-ttu-id="c3151-106">break \_ comp src0，src1</span><span class="sxs-lookup"><span data-stu-id="c3151-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="c3151-107">其中：</span><span class="sxs-lookup"><span data-stu-id="c3151-107">Where:</span></span>

-   <span data-ttu-id="c3151-108">\_comp 是兩個來源暫存器之間的純量 (或單一) 比較。</span><span class="sxs-lookup"><span data-stu-id="c3151-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="c3151-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="c3151-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="c3151-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3151-110">Syntax</span></span> | <span data-ttu-id="c3151-111">比較</span><span class="sxs-lookup"><span data-stu-id="c3151-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="c3151-112">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="c3151-112">\_gt</span></span>   | <span data-ttu-id="c3151-113">大於</span><span class="sxs-lookup"><span data-stu-id="c3151-113">Greater than</span></span>          |
    | <span data-ttu-id="c3151-114">\_淺色</span><span class="sxs-lookup"><span data-stu-id="c3151-114">\_lt</span></span>   | <span data-ttu-id="c3151-115">小於</span><span class="sxs-lookup"><span data-stu-id="c3151-115">Less than</span></span>             |
    | <span data-ttu-id="c3151-116">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="c3151-116">\_ge</span></span>   | <span data-ttu-id="c3151-117">大於或等於</span><span class="sxs-lookup"><span data-stu-id="c3151-117">Greater than or equal</span></span> |
    | <span data-ttu-id="c3151-118">\_樂</span><span class="sxs-lookup"><span data-stu-id="c3151-118">\_le</span></span>   | <span data-ttu-id="c3151-119">小於或等於</span><span class="sxs-lookup"><span data-stu-id="c3151-119">Less than or equal</span></span>    |
    | <span data-ttu-id="c3151-120">\_情 商</span><span class="sxs-lookup"><span data-stu-id="c3151-120">\_eq</span></span>   | <span data-ttu-id="c3151-121">等於</span><span class="sxs-lookup"><span data-stu-id="c3151-121">Equal to</span></span>              |
    | <span data-ttu-id="c3151-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="c3151-122">\_ne</span></span>   | <span data-ttu-id="c3151-123">不等於</span><span class="sxs-lookup"><span data-stu-id="c3151-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="c3151-124">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="c3151-124">src0 is a source register.</span></span> <span data-ttu-id="c3151-125">如果選取單一元件，則需要複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="c3151-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="c3151-126">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="c3151-126">src1 is a source register.</span></span> <span data-ttu-id="c3151-127">如果選取單一元件，則需要複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="c3151-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3151-128">備註</span><span class="sxs-lookup"><span data-stu-id="c3151-128">Remarks</span></span>

<span data-ttu-id="c3151-129">下列版本支援此指令。</span><span class="sxs-lookup"><span data-stu-id="c3151-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="c3151-130">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c3151-130">Pixel shader versions</span></span> | <span data-ttu-id="c3151-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="c3151-131">1\_1</span></span> | <span data-ttu-id="c3151-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="c3151-132">1\_2</span></span> | <span data-ttu-id="c3151-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c3151-133">1\_3</span></span> | <span data-ttu-id="c3151-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="c3151-134">1\_4</span></span> | <span data-ttu-id="c3151-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c3151-135">2\_0</span></span> | <span data-ttu-id="c3151-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c3151-136">2\_x</span></span> | <span data-ttu-id="c3151-137">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c3151-137">2\_sw</span></span> | <span data-ttu-id="c3151-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c3151-138">3\_0</span></span> | <span data-ttu-id="c3151-139">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c3151-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c3151-140">中斷 \_ 複合</span><span class="sxs-lookup"><span data-stu-id="c3151-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="c3151-141">x</span><span class="sxs-lookup"><span data-stu-id="c3151-141">x</span></span>    | <span data-ttu-id="c3151-142">x</span><span class="sxs-lookup"><span data-stu-id="c3151-142">x</span></span>     | <span data-ttu-id="c3151-143">x</span><span class="sxs-lookup"><span data-stu-id="c3151-143">x</span></span>    | <span data-ttu-id="c3151-144">x</span><span class="sxs-lookup"><span data-stu-id="c3151-144">x</span></span>     |



 

<span data-ttu-id="c3151-145">當比較結果為 true 時，它會中斷目前的迴圈，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c3151-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="c3151-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3151-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3151-147">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c3151-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




