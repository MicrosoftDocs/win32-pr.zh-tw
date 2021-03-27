---
title: break_comp-vs
description: 有條件地中斷最接近 endloop-vs 或 endrep-vs 的目前迴圈。
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841664"
---
# <a name="break_comp---vs"></a><span data-ttu-id="13ddf-103">中斷 \_ 複合-vs</span><span class="sxs-lookup"><span data-stu-id="13ddf-103">break\_comp - vs</span></span>

<span data-ttu-id="13ddf-104">有條件地中斷最接近 [endloop-vs](endloop---vs.md) 或 [endrep-vs](endrep---vs.md)的目前迴圈。</span><span class="sxs-lookup"><span data-stu-id="13ddf-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13ddf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ddf-105">Syntax</span></span>



| <span data-ttu-id="13ddf-106">break \_ comp src0，src1</span><span class="sxs-lookup"><span data-stu-id="13ddf-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="13ddf-107">其中：</span><span class="sxs-lookup"><span data-stu-id="13ddf-107">Where:</span></span>

-   <span data-ttu-id="13ddf-108">\_comp 是兩個來源暫存器之間的比較。</span><span class="sxs-lookup"><span data-stu-id="13ddf-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="13ddf-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="13ddf-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="13ddf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ddf-110">Syntax</span></span> | <span data-ttu-id="13ddf-111">比較</span><span class="sxs-lookup"><span data-stu-id="13ddf-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="13ddf-112">\_燃氣輪機</span><span class="sxs-lookup"><span data-stu-id="13ddf-112">\_gt</span></span>   | <span data-ttu-id="13ddf-113">大於</span><span class="sxs-lookup"><span data-stu-id="13ddf-113">Greater than</span></span>          |
    | <span data-ttu-id="13ddf-114">\_淺色</span><span class="sxs-lookup"><span data-stu-id="13ddf-114">\_lt</span></span>   | <span data-ttu-id="13ddf-115">小於</span><span class="sxs-lookup"><span data-stu-id="13ddf-115">Less than</span></span>             |
    | <span data-ttu-id="13ddf-116">\_通用 電氣</span><span class="sxs-lookup"><span data-stu-id="13ddf-116">\_ge</span></span>   | <span data-ttu-id="13ddf-117">大於或等於</span><span class="sxs-lookup"><span data-stu-id="13ddf-117">Greater than or equal</span></span> |
    | <span data-ttu-id="13ddf-118">\_樂</span><span class="sxs-lookup"><span data-stu-id="13ddf-118">\_le</span></span>   | <span data-ttu-id="13ddf-119">小於或等於</span><span class="sxs-lookup"><span data-stu-id="13ddf-119">Less than or equal</span></span>    |
    | <span data-ttu-id="13ddf-120">\_情 商</span><span class="sxs-lookup"><span data-stu-id="13ddf-120">\_eq</span></span>   | <span data-ttu-id="13ddf-121">等於</span><span class="sxs-lookup"><span data-stu-id="13ddf-121">Equal to</span></span>              |
    | <span data-ttu-id="13ddf-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="13ddf-122">\_ne</span></span>   | <span data-ttu-id="13ddf-123">不等於</span><span class="sxs-lookup"><span data-stu-id="13ddf-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="13ddf-124">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="13ddf-124">src0 is a source register.</span></span> <span data-ttu-id="13ddf-125">需要複寫 swizzle 才能選取單一元件。</span><span class="sxs-lookup"><span data-stu-id="13ddf-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="13ddf-126">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="13ddf-126">src1 is a source register.</span></span> <span data-ttu-id="13ddf-127">需要複寫 swizzle 才能選取單一元件。</span><span class="sxs-lookup"><span data-stu-id="13ddf-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ddf-128">備註</span><span class="sxs-lookup"><span data-stu-id="13ddf-128">Remarks</span></span>

<span data-ttu-id="13ddf-129">下列版本支援此指令。</span><span class="sxs-lookup"><span data-stu-id="13ddf-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="13ddf-130">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="13ddf-130">Vertex shader versions</span></span> | <span data-ttu-id="13ddf-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="13ddf-131">1\_1</span></span> | <span data-ttu-id="13ddf-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13ddf-132">2\_0</span></span> | <span data-ttu-id="13ddf-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="13ddf-133">2\_x</span></span> | <span data-ttu-id="13ddf-134">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="13ddf-134">2\_sw</span></span> | <span data-ttu-id="13ddf-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13ddf-135">3\_0</span></span> | <span data-ttu-id="13ddf-136">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="13ddf-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="13ddf-137">中斷 \_ 複合</span><span class="sxs-lookup"><span data-stu-id="13ddf-137">break\_comp</span></span>            |      |      | <span data-ttu-id="13ddf-138">x</span><span class="sxs-lookup"><span data-stu-id="13ddf-138">x</span></span>    | <span data-ttu-id="13ddf-139">x</span><span class="sxs-lookup"><span data-stu-id="13ddf-139">x</span></span>     | <span data-ttu-id="13ddf-140">x</span><span class="sxs-lookup"><span data-stu-id="13ddf-140">x</span></span>    | <span data-ttu-id="13ddf-141">x</span><span class="sxs-lookup"><span data-stu-id="13ddf-141">x</span></span>     |



 

<span data-ttu-id="13ddf-142">當比較結果為 true 時，它會中斷目前的迴圈，如下所示。</span><span class="sxs-lookup"><span data-stu-id="13ddf-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="13ddf-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="13ddf-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ddf-144">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="13ddf-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




