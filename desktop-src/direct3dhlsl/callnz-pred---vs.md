---
title: callnz pred-vs
description: 如果不是零，則使用述詞來呼叫。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022818"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="c4357-105">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="c4357-105">callnz pred - vs</span></span>

<span data-ttu-id="c4357-106">如果不是零，則使用述詞來呼叫。</span><span class="sxs-lookup"><span data-stu-id="c4357-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="c4357-107">對標籤索引所標記的指令執行條件式呼叫。</span><span class="sxs-lookup"><span data-stu-id="c4357-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="c4357-108">Predication 會使用布林值來判斷是否要執行指令。</span><span class="sxs-lookup"><span data-stu-id="c4357-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4357-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4357-109">Syntax</span></span>



| <span data-ttu-id="c4357-110">callnz l \# 、 \[ ！ \]P。版</span><span class="sxs-lookup"><span data-stu-id="c4357-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="c4357-111">x</span><span class="sxs-lookup"><span data-stu-id="c4357-111">y\</span></span>|<span data-ttu-id="c4357-112">#a1</span><span class="sxs-lookup"><span data-stu-id="c4357-112">z\</span></span>|<span data-ttu-id="c4357-113">w</span><span class="sxs-lookup"><span data-stu-id="c4357-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="c4357-114">其中：</span><span class="sxs-lookup"><span data-stu-id="c4357-114">where:</span></span>

-   <span data-ttu-id="c4357-115">l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。</span><span class="sxs-lookup"><span data-stu-id="c4357-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="c4357-116">\[!\] 這是選擇性的否定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c4357-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="c4357-117">p0 是述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="c4357-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="c4357-118">{x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="c4357-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4357-119">備註</span><span class="sxs-lookup"><span data-stu-id="c4357-119">Remarks</span></span>



| <span data-ttu-id="c4357-120">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="c4357-120">Vertex shader versions</span></span> | <span data-ttu-id="c4357-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="c4357-121">1\_1</span></span> | <span data-ttu-id="c4357-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4357-122">2\_0</span></span> | <span data-ttu-id="c4357-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4357-123">2\_x</span></span> | <span data-ttu-id="c4357-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c4357-124">2\_sw</span></span> | <span data-ttu-id="c4357-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4357-125">3\_0</span></span> | <span data-ttu-id="c4357-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c4357-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c4357-127">callnz pred</span><span class="sxs-lookup"><span data-stu-id="c4357-127">callnz pred</span></span>            |      |      | <span data-ttu-id="c4357-128">x</span><span class="sxs-lookup"><span data-stu-id="c4357-128">x</span></span>    | <span data-ttu-id="c4357-129">x</span><span class="sxs-lookup"><span data-stu-id="c4357-129">x</span></span>     | <span data-ttu-id="c4357-130">x</span><span class="sxs-lookup"><span data-stu-id="c4357-130">x</span></span>    | <span data-ttu-id="c4357-131">x</span><span class="sxs-lookup"><span data-stu-id="c4357-131">x</span></span>     |



 

<span data-ttu-id="c4357-132">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="c4357-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="c4357-133">此指令會使用一個頂點著色器指令位置。</span><span class="sxs-lookup"><span data-stu-id="c4357-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4357-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4357-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4357-135">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="c4357-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




