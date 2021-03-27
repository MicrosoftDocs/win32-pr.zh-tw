---
title: expp-vs
description: 提供部分有效位數指數2x。
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679136"
---
# <a name="expp---vs"></a><span data-ttu-id="fcb36-103">expp-vs</span><span class="sxs-lookup"><span data-stu-id="fcb36-103">expp - vs</span></span>

<span data-ttu-id="fcb36-104">提供部分有效位數指數 2<sup>x</sup>。</span><span class="sxs-lookup"><span data-stu-id="fcb36-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb36-105">Syntax</span></span>



| <span data-ttu-id="fcb36-106">expp dst、src。版</span><span class="sxs-lookup"><span data-stu-id="fcb36-106">expp dst, src.{x\</span></span>|<span data-ttu-id="fcb36-107">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-107">y\</span></span>|<span data-ttu-id="fcb36-108">#a1</span><span class="sxs-lookup"><span data-stu-id="fcb36-108">z\</span></span>|<span data-ttu-id="fcb36-109">w</span><span class="sxs-lookup"><span data-stu-id="fcb36-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="fcb36-110">其中：</span><span class="sxs-lookup"><span data-stu-id="fcb36-110">Where:</span></span>

-   <span data-ttu-id="fcb36-111">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="fcb36-111">dst is the destination register.</span></span>
-   <span data-ttu-id="fcb36-112">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="fcb36-112">src is a source register.</span></span> <span data-ttu-id="fcb36-113">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="fcb36-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="fcb36-114">{x \| y \| z \| w} 是在來源註冊上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="fcb36-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb36-115">備註</span><span class="sxs-lookup"><span data-stu-id="fcb36-115">Remarks</span></span>



| <span data-ttu-id="fcb36-116">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="fcb36-116">Vertex shader versions</span></span> | <span data-ttu-id="fcb36-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="fcb36-117">1\_1</span></span> | <span data-ttu-id="fcb36-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fcb36-118">2\_0</span></span> | <span data-ttu-id="fcb36-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fcb36-119">2\_x</span></span> | <span data-ttu-id="fcb36-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fcb36-120">2\_sw</span></span> | <span data-ttu-id="fcb36-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fcb36-121">3\_0</span></span> | <span data-ttu-id="fcb36-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fcb36-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fcb36-123">expp</span><span class="sxs-lookup"><span data-stu-id="fcb36-123">expp</span></span>                   | <span data-ttu-id="fcb36-124">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-124">x</span></span>    | <span data-ttu-id="fcb36-125">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-125">x</span></span>    | <span data-ttu-id="fcb36-126">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-126">x</span></span>    | <span data-ttu-id="fcb36-127">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-127">x</span></span>     | <span data-ttu-id="fcb36-128">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-128">x</span></span>    | <span data-ttu-id="fcb36-129">x</span><span class="sxs-lookup"><span data-stu-id="fcb36-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="fcb36-130">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fcb36-130">vs\_1\_1</span></span>

<span data-ttu-id="fcb36-131">依據頂點著色器版本而 [定，exp vs](exp---vs.md) 指令的運作方式會有所不同。</span><span class="sxs-lookup"><span data-stu-id="fcb36-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="fcb36-132">在 vs \_ 1 \_ 1 中，expp 指令會提供下列結果：</span><span class="sxs-lookup"><span data-stu-id="fcb36-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="fcb36-133">在 vs \_ 2 \_ 0 和更新的中，expp 指令會提供下列結果：</span><span class="sxs-lookup"><span data-stu-id="fcb36-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="fcb36-134">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fcb36-134">vs\_2\_0</span></span>

<span data-ttu-id="fcb36-135">在 vs \_ 2 \_ 0 和更新的中，指令的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="fcb36-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="fcb36-136">指令至少提供10個位的精確度。</span><span class="sxs-lookup"><span data-stu-id="fcb36-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcb36-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcb36-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb36-138">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="fcb36-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




