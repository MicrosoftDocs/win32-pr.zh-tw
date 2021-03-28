---
title: pow-ps
description: 完整有效位數 abs (src0) src1。 |pow-ps
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974008"
---
# <a name="pow---ps"></a><span data-ttu-id="64665-104">pow-ps</span><span class="sxs-lookup"><span data-stu-id="64665-104">pow - ps</span></span>

<span data-ttu-id="64665-105">完整有效位數 abs (src0) <sup>src1</sup>。</span><span class="sxs-lookup"><span data-stu-id="64665-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="64665-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64665-106">Syntax</span></span>



| <span data-ttu-id="64665-107">pow dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="64665-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="64665-108">其中</span><span class="sxs-lookup"><span data-stu-id="64665-108">where</span></span>

-   <span data-ttu-id="64665-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="64665-109">dst is the destination register.</span></span>
-   <span data-ttu-id="64665-110">src0 是輸入來源註冊。</span><span class="sxs-lookup"><span data-stu-id="64665-110">src0 is an input source register.</span></span> <span data-ttu-id="64665-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="64665-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="64665-112">src1 是輸入來源註冊。</span><span class="sxs-lookup"><span data-stu-id="64665-112">src1 is an input source register.</span></span> <span data-ttu-id="64665-113">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="64665-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="64665-114">備註</span><span class="sxs-lookup"><span data-stu-id="64665-114">Remarks</span></span>



| <span data-ttu-id="64665-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="64665-115">Pixel shader versions</span></span> | <span data-ttu-id="64665-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="64665-116">1\_1</span></span> | <span data-ttu-id="64665-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="64665-117">1\_2</span></span> | <span data-ttu-id="64665-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="64665-118">1\_3</span></span> | <span data-ttu-id="64665-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="64665-119">1\_4</span></span> | <span data-ttu-id="64665-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64665-120">2\_0</span></span> | <span data-ttu-id="64665-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64665-121">2\_x</span></span> | <span data-ttu-id="64665-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="64665-122">2\_sw</span></span> | <span data-ttu-id="64665-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64665-123">3\_0</span></span> | <span data-ttu-id="64665-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="64665-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="64665-125">pow</span><span class="sxs-lookup"><span data-stu-id="64665-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="64665-126">x</span><span class="sxs-lookup"><span data-stu-id="64665-126">x</span></span>    | <span data-ttu-id="64665-127">x</span><span class="sxs-lookup"><span data-stu-id="64665-127">x</span></span>    | <span data-ttu-id="64665-128">x</span><span class="sxs-lookup"><span data-stu-id="64665-128">x</span></span>     | <span data-ttu-id="64665-129">x</span><span class="sxs-lookup"><span data-stu-id="64665-129">x</span></span>    | <span data-ttu-id="64665-130">x</span><span class="sxs-lookup"><span data-stu-id="64665-130">x</span></span>     |



 

<span data-ttu-id="64665-131">此指示的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="64665-131">This instruction works as follows:</span></span>

<span data-ttu-id="64665-132">dest. x = dest. y = dest. z = dest. w = \[ abs (src0) \] <sup>src1</sup>;</span><span class="sxs-lookup"><span data-stu-id="64665-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="64665-133">這是純量指令，因此來源暫存器應該具有複寫 swizzles，以指出要使用的通道。</span><span class="sxs-lookup"><span data-stu-id="64665-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="64665-134">輸入 power (src1) 必須是純量。</span><span class="sxs-lookup"><span data-stu-id="64665-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="64665-135">純量結果會複寫到所有的四個輸出通道。</span><span class="sxs-lookup"><span data-stu-id="64665-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="64665-136">此指令可以擴充為 exp (src1 \* 記錄 (src0) ) 。</span><span class="sxs-lookup"><span data-stu-id="64665-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="64665-137">Dst 暫存器應該是暫時的註冊，而且不應該與 src1 相同。</span><span class="sxs-lookup"><span data-stu-id="64665-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64665-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="64665-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64665-139">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="64665-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




