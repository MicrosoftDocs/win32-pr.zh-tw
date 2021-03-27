---
title: callnz pred-ps
description: 使用述詞來呼叫，如果不是零，則為。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932815"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="22396-105">callnz pred-ps</span><span class="sxs-lookup"><span data-stu-id="22396-105">callnz pred - ps</span></span>

<span data-ttu-id="22396-106">使用述詞來呼叫，如果不是零，則為。</span><span class="sxs-lookup"><span data-stu-id="22396-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="22396-107">對標籤索引所標記的指令執行條件式呼叫。</span><span class="sxs-lookup"><span data-stu-id="22396-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="22396-108">Predication 會使用布林值來判斷是否要執行指令。</span><span class="sxs-lookup"><span data-stu-id="22396-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="22396-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="22396-109">Syntax</span></span>



| <span data-ttu-id="22396-110">callnz l \# 、 \[ ！ \]P。版</span><span class="sxs-lookup"><span data-stu-id="22396-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="22396-111">x</span><span class="sxs-lookup"><span data-stu-id="22396-111">y\</span></span>|<span data-ttu-id="22396-112">#a1</span><span class="sxs-lookup"><span data-stu-id="22396-112">z\</span></span>|<span data-ttu-id="22396-113">w</span><span class="sxs-lookup"><span data-stu-id="22396-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="22396-114">其中：</span><span class="sxs-lookup"><span data-stu-id="22396-114">Where:</span></span>

-   <span data-ttu-id="22396-115">其中 l \# 是 [標籤-ps](label---ps.md) ，標示要呼叫的副程式開頭。</span><span class="sxs-lookup"><span data-stu-id="22396-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="22396-116">\[!\] 這是選擇性的否定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="22396-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="22396-117">p0 是述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="22396-117">p0 is the predicate register.</span></span> <span data-ttu-id="22396-118">請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="22396-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="22396-119">{x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="22396-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="22396-120">備註</span><span class="sxs-lookup"><span data-stu-id="22396-120">Remarks</span></span>



| <span data-ttu-id="22396-121">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="22396-121">Pixel shader versions</span></span> | <span data-ttu-id="22396-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="22396-122">1\_1</span></span> | <span data-ttu-id="22396-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="22396-123">1\_2</span></span> | <span data-ttu-id="22396-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="22396-124">1\_3</span></span> | <span data-ttu-id="22396-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="22396-125">1\_4</span></span> | <span data-ttu-id="22396-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="22396-126">2\_0</span></span> | <span data-ttu-id="22396-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="22396-127">2\_x</span></span> | <span data-ttu-id="22396-128">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="22396-128">2\_sw</span></span> | <span data-ttu-id="22396-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="22396-129">3\_0</span></span> | <span data-ttu-id="22396-130">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="22396-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="22396-131">callnz pred</span><span class="sxs-lookup"><span data-stu-id="22396-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="22396-132">x</span><span class="sxs-lookup"><span data-stu-id="22396-132">x</span></span>    | <span data-ttu-id="22396-133">x</span><span class="sxs-lookup"><span data-stu-id="22396-133">x</span></span>     | <span data-ttu-id="22396-134">x</span><span class="sxs-lookup"><span data-stu-id="22396-134">x</span></span>    | <span data-ttu-id="22396-135">x</span><span class="sxs-lookup"><span data-stu-id="22396-135">x</span></span>     |



 

<span data-ttu-id="22396-136">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="22396-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="22396-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="22396-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22396-138">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="22396-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




