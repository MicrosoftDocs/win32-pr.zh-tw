---
title: rsq-ps
description: 將交互平方根 (計算來源純量的) 。 |rsq-ps
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974148"
---
# <a name="rsq---ps"></a><span data-ttu-id="e4487-104">rsq-ps</span><span class="sxs-lookup"><span data-stu-id="e4487-104">rsq - ps</span></span>

<span data-ttu-id="e4487-105">將交互平方根 (計算來源純量的) 。</span><span class="sxs-lookup"><span data-stu-id="e4487-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4487-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4487-106">Syntax</span></span>



| <span data-ttu-id="e4487-107">rsq dst、src</span><span class="sxs-lookup"><span data-stu-id="e4487-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e4487-108">其中</span><span class="sxs-lookup"><span data-stu-id="e4487-108">where</span></span>

-   <span data-ttu-id="e4487-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e4487-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e4487-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e4487-110">src is a source register.</span></span> <span data-ttu-id="e4487-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="e4487-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4487-112">備註</span><span class="sxs-lookup"><span data-stu-id="e4487-112">Remarks</span></span>



| <span data-ttu-id="e4487-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e4487-113">Pixel shader versions</span></span> | <span data-ttu-id="e4487-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e4487-114">1\_1</span></span> | <span data-ttu-id="e4487-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e4487-115">1\_2</span></span> | <span data-ttu-id="e4487-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e4487-116">1\_3</span></span> | <span data-ttu-id="e4487-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e4487-117">1\_4</span></span> | <span data-ttu-id="e4487-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4487-118">2\_0</span></span> | <span data-ttu-id="e4487-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e4487-119">2\_x</span></span> | <span data-ttu-id="e4487-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e4487-120">2\_sw</span></span> | <span data-ttu-id="e4487-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4487-121">3\_0</span></span> | <span data-ttu-id="e4487-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e4487-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e4487-123">rsq</span><span class="sxs-lookup"><span data-stu-id="e4487-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="e4487-124">x</span><span class="sxs-lookup"><span data-stu-id="e4487-124">x</span></span>    | <span data-ttu-id="e4487-125">x</span><span class="sxs-lookup"><span data-stu-id="e4487-125">x</span></span>    | <span data-ttu-id="e4487-126">x</span><span class="sxs-lookup"><span data-stu-id="e4487-126">x</span></span>     | <span data-ttu-id="e4487-127">x</span><span class="sxs-lookup"><span data-stu-id="e4487-127">x</span></span>    | <span data-ttu-id="e4487-128">x</span><span class="sxs-lookup"><span data-stu-id="e4487-128">x</span></span>     |



 

<span data-ttu-id="e4487-129">在處理之前，會先取得絕對值。</span><span class="sxs-lookup"><span data-stu-id="e4487-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="e4487-130">精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，4.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。</span><span class="sxs-lookup"><span data-stu-id="e4487-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="e4487-131">如果輸入正好是1.0，則輸出必須正好為1.0。</span><span class="sxs-lookup"><span data-stu-id="e4487-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="e4487-132">0.0 的來源會產生無限大。</span><span class="sxs-lookup"><span data-stu-id="e4487-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4487-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4487-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4487-134">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e4487-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




