---
title: rsq-vs
description: 將交互平方根 (計算來源純量的) 。 |rsq-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974272"
---
# <a name="rsq---vs"></a><span data-ttu-id="1584a-104">rsq-vs</span><span class="sxs-lookup"><span data-stu-id="1584a-104">rsq - vs</span></span>

<span data-ttu-id="1584a-105">將交互平方根 (計算來源純量的) 。</span><span class="sxs-lookup"><span data-stu-id="1584a-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="1584a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1584a-106">Syntax</span></span>



| <span data-ttu-id="1584a-107">rsq dst、src</span><span class="sxs-lookup"><span data-stu-id="1584a-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="1584a-108">其中</span><span class="sxs-lookup"><span data-stu-id="1584a-108">where</span></span>

-   <span data-ttu-id="1584a-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="1584a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="1584a-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="1584a-110">src is a source register.</span></span> <span data-ttu-id="1584a-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="1584a-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="1584a-112">備註</span><span class="sxs-lookup"><span data-stu-id="1584a-112">Remarks</span></span>



| <span data-ttu-id="1584a-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="1584a-113">Vertex shader versions</span></span> | <span data-ttu-id="1584a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="1584a-114">1\_1</span></span> | <span data-ttu-id="1584a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1584a-115">2\_0</span></span> | <span data-ttu-id="1584a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1584a-116">2\_x</span></span> | <span data-ttu-id="1584a-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1584a-117">2\_sw</span></span> | <span data-ttu-id="1584a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1584a-118">3\_0</span></span> | <span data-ttu-id="1584a-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1584a-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="1584a-120">rsq</span><span class="sxs-lookup"><span data-stu-id="1584a-120">rsq</span></span>                    | <span data-ttu-id="1584a-121">x</span><span class="sxs-lookup"><span data-stu-id="1584a-121">x</span></span>    | <span data-ttu-id="1584a-122">x</span><span class="sxs-lookup"><span data-stu-id="1584a-122">x</span></span>    | <span data-ttu-id="1584a-123">x</span><span class="sxs-lookup"><span data-stu-id="1584a-123">x</span></span>    | <span data-ttu-id="1584a-124">x</span><span class="sxs-lookup"><span data-stu-id="1584a-124">x</span></span>     | <span data-ttu-id="1584a-125">x</span><span class="sxs-lookup"><span data-stu-id="1584a-125">x</span></span>    | <span data-ttu-id="1584a-126">x</span><span class="sxs-lookup"><span data-stu-id="1584a-126">x</span></span>     |



 

<span data-ttu-id="1584a-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="1584a-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="1584a-128">在處理之前，會先取得絕對值。</span><span class="sxs-lookup"><span data-stu-id="1584a-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="1584a-129">精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，4.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。</span><span class="sxs-lookup"><span data-stu-id="1584a-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="1584a-130">如果來源沒有下標，則會使用 x 元件。</span><span class="sxs-lookup"><span data-stu-id="1584a-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="1584a-131">如果輸入正好是1.0，則輸出必須正好為1.0。</span><span class="sxs-lookup"><span data-stu-id="1584a-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="1584a-132">0.0 的來源會產生無限大。</span><span class="sxs-lookup"><span data-stu-id="1584a-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1584a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="1584a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1584a-134">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="1584a-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




