---
title: exp-vs
description: 提供完整的精確度指數2x。 |exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992078"
---
# <a name="exp---vs"></a><span data-ttu-id="52ca4-104">exp-vs</span><span class="sxs-lookup"><span data-stu-id="52ca4-104">exp - vs</span></span>

<span data-ttu-id="52ca4-105">提供完整的精確度指數 2<sup>x</sup>。</span><span class="sxs-lookup"><span data-stu-id="52ca4-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ca4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="52ca4-106">Syntax</span></span>



| <span data-ttu-id="52ca4-107">exp dst、src</span><span class="sxs-lookup"><span data-stu-id="52ca4-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="52ca4-108">其中</span><span class="sxs-lookup"><span data-stu-id="52ca4-108">where</span></span>

-   <span data-ttu-id="52ca4-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="52ca4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="52ca4-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="52ca4-110">src is a source register.</span></span> <span data-ttu-id="52ca4-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="52ca4-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="52ca4-112">請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md)。</span><span class="sxs-lookup"><span data-stu-id="52ca4-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52ca4-113">備註</span><span class="sxs-lookup"><span data-stu-id="52ca4-113">Remarks</span></span>



| <span data-ttu-id="52ca4-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="52ca4-114">Vertex shader versions</span></span> | <span data-ttu-id="52ca4-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="52ca4-115">1\_1</span></span> | <span data-ttu-id="52ca4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52ca4-116">2\_0</span></span> | <span data-ttu-id="52ca4-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="52ca4-117">2\_x</span></span> | <span data-ttu-id="52ca4-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="52ca4-118">2\_sw</span></span> | <span data-ttu-id="52ca4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52ca4-119">3\_0</span></span> | <span data-ttu-id="52ca4-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="52ca4-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="52ca4-121">exp</span><span class="sxs-lookup"><span data-stu-id="52ca4-121">exp</span></span>                    | <span data-ttu-id="52ca4-122">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-122">x</span></span>    | <span data-ttu-id="52ca4-123">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-123">x</span></span>    | <span data-ttu-id="52ca4-124">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-124">x</span></span>    | <span data-ttu-id="52ca4-125">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-125">x</span></span>     | <span data-ttu-id="52ca4-126">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-126">x</span></span>    | <span data-ttu-id="52ca4-127">x</span><span class="sxs-lookup"><span data-stu-id="52ca4-127">x</span></span>     |



 

<span data-ttu-id="52ca4-128">此指令提供至少21個位的精確度。</span><span class="sxs-lookup"><span data-stu-id="52ca4-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="52ca4-129">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="52ca4-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="52ca4-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="52ca4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52ca4-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="52ca4-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




