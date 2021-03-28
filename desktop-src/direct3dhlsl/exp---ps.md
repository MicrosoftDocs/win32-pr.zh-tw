---
title: exp-ps
description: 提供完整的精確度指數2x。 |exp-ps
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035252"
---
# <a name="exp---ps"></a><span data-ttu-id="231c6-104">exp-ps</span><span class="sxs-lookup"><span data-stu-id="231c6-104">exp - ps</span></span>

<span data-ttu-id="231c6-105">提供完整的精確度指數 2<sup>x</sup>。</span><span class="sxs-lookup"><span data-stu-id="231c6-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="231c6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="231c6-106">Syntax</span></span>



| <span data-ttu-id="231c6-107">exp dst、src</span><span class="sxs-lookup"><span data-stu-id="231c6-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="231c6-108">其中</span><span class="sxs-lookup"><span data-stu-id="231c6-108">where</span></span>

-   <span data-ttu-id="231c6-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="231c6-109">dst is the destination register.</span></span>
-   <span data-ttu-id="231c6-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="231c6-110">src is a source register.</span></span> <span data-ttu-id="231c6-111">來源註冊需要明確使用複寫 swizzle;也就是，您必須指定一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="231c6-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="231c6-112">請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)。</span><span class="sxs-lookup"><span data-stu-id="231c6-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="231c6-113">備註</span><span class="sxs-lookup"><span data-stu-id="231c6-113">Remarks</span></span>



| <span data-ttu-id="231c6-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="231c6-114">Pixel shader versions</span></span> | <span data-ttu-id="231c6-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="231c6-115">1\_1</span></span> | <span data-ttu-id="231c6-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="231c6-116">1\_2</span></span> | <span data-ttu-id="231c6-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="231c6-117">1\_3</span></span> | <span data-ttu-id="231c6-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="231c6-118">1\_4</span></span> | <span data-ttu-id="231c6-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="231c6-119">2\_0</span></span> | <span data-ttu-id="231c6-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="231c6-120">2\_x</span></span> | <span data-ttu-id="231c6-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="231c6-121">2\_sw</span></span> | <span data-ttu-id="231c6-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="231c6-122">3\_0</span></span> | <span data-ttu-id="231c6-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="231c6-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="231c6-124">exp</span><span class="sxs-lookup"><span data-stu-id="231c6-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="231c6-125">x</span><span class="sxs-lookup"><span data-stu-id="231c6-125">x</span></span>    | <span data-ttu-id="231c6-126">x</span><span class="sxs-lookup"><span data-stu-id="231c6-126">x</span></span>    | <span data-ttu-id="231c6-127">x</span><span class="sxs-lookup"><span data-stu-id="231c6-127">x</span></span>     | <span data-ttu-id="231c6-128">x</span><span class="sxs-lookup"><span data-stu-id="231c6-128">x</span></span>    | <span data-ttu-id="231c6-129">x</span><span class="sxs-lookup"><span data-stu-id="231c6-129">x</span></span>     |



 

<span data-ttu-id="231c6-130">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="231c6-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="231c6-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="231c6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="231c6-132">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="231c6-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




