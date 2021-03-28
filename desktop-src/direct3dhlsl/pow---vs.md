---
title: pow-vs
description: 完整有效位數 abs (src0) src1。 |pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195918"
---
# <a name="pow---vs"></a><span data-ttu-id="92974-104">pow-vs</span><span class="sxs-lookup"><span data-stu-id="92974-104">pow - vs</span></span>

<span data-ttu-id="92974-105">完整有效位數 abs (src0) <sup>src1</sup>。</span><span class="sxs-lookup"><span data-stu-id="92974-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="92974-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="92974-106">Syntax</span></span>



| <span data-ttu-id="92974-107">pow dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="92974-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="92974-108">其中</span><span class="sxs-lookup"><span data-stu-id="92974-108">where</span></span>

-   <span data-ttu-id="92974-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-109">dst is the destination register.</span></span>
-   <span data-ttu-id="92974-110">src0 是輸入來源註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-110">src0 is an input source register.</span></span> <span data-ttu-id="92974-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="92974-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="92974-112">src1 是輸入來源註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-112">src1 is an input source register.</span></span> <span data-ttu-id="92974-113">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="92974-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="92974-114">備註</span><span class="sxs-lookup"><span data-stu-id="92974-114">Remarks</span></span>



| <span data-ttu-id="92974-115">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="92974-115">Vertex shader versions</span></span> | <span data-ttu-id="92974-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="92974-116">1\_1</span></span> | <span data-ttu-id="92974-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92974-117">2\_0</span></span> | <span data-ttu-id="92974-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="92974-118">2\_x</span></span> | <span data-ttu-id="92974-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92974-119">2\_sw</span></span> | <span data-ttu-id="92974-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92974-120">3\_0</span></span> | <span data-ttu-id="92974-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92974-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="92974-122">pow</span><span class="sxs-lookup"><span data-stu-id="92974-122">pow</span></span>                    |      | <span data-ttu-id="92974-123">x</span><span class="sxs-lookup"><span data-stu-id="92974-123">x</span></span>    | <span data-ttu-id="92974-124">x</span><span class="sxs-lookup"><span data-stu-id="92974-124">x</span></span>    | <span data-ttu-id="92974-125">x</span><span class="sxs-lookup"><span data-stu-id="92974-125">x</span></span>     | <span data-ttu-id="92974-126">x</span><span class="sxs-lookup"><span data-stu-id="92974-126">x</span></span>    | <span data-ttu-id="92974-127">x</span><span class="sxs-lookup"><span data-stu-id="92974-127">x</span></span>     |



 

<span data-ttu-id="92974-128">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="92974-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="92974-129">這是純量指令，因此來源暫存器應該具有複寫 swizzles，以指出要使用的通道。</span><span class="sxs-lookup"><span data-stu-id="92974-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="92974-130">純量結果會複寫到所有的四個輸出通道。</span><span class="sxs-lookup"><span data-stu-id="92974-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="92974-131">此指令可以擴充為 exp (src1 \* 記錄 (src0) ) 。</span><span class="sxs-lookup"><span data-stu-id="92974-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="92974-132">有效位數不是低於15個位。</span><span class="sxs-lookup"><span data-stu-id="92974-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="92974-133">目的地暫存器應該是臨時暫存器，而且不應該與 src1 是相同的註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92974-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="92974-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92974-135">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="92974-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




