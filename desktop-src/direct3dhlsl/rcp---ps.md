---
title: rcp-ps
description: 計算來源純量的倒數。 |rcp-ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974237"
---
# <a name="rcp---ps"></a><span data-ttu-id="d0420-104">rcp-ps</span><span class="sxs-lookup"><span data-stu-id="d0420-104">rcp - ps</span></span>

<span data-ttu-id="d0420-105">計算來源純量的倒數。</span><span class="sxs-lookup"><span data-stu-id="d0420-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0420-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0420-106">Syntax</span></span>



| <span data-ttu-id="d0420-107">rcp dst、src</span><span class="sxs-lookup"><span data-stu-id="d0420-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="d0420-108">其中</span><span class="sxs-lookup"><span data-stu-id="d0420-108">where</span></span>

-   <span data-ttu-id="d0420-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="d0420-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d0420-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="d0420-110">src is a source register.</span></span> <span data-ttu-id="d0420-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="d0420-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0420-112">備註</span><span class="sxs-lookup"><span data-stu-id="d0420-112">Remarks</span></span>



| <span data-ttu-id="d0420-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="d0420-113">Pixel shader versions</span></span> | <span data-ttu-id="d0420-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d0420-114">1\_1</span></span> | <span data-ttu-id="d0420-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="d0420-115">1\_2</span></span> | <span data-ttu-id="d0420-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d0420-116">1\_3</span></span> | <span data-ttu-id="d0420-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="d0420-117">1\_4</span></span> | <span data-ttu-id="d0420-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0420-118">2\_0</span></span> | <span data-ttu-id="d0420-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d0420-119">2\_x</span></span> | <span data-ttu-id="d0420-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d0420-120">2\_sw</span></span> | <span data-ttu-id="d0420-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0420-121">3\_0</span></span> | <span data-ttu-id="d0420-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d0420-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d0420-123">rcp</span><span class="sxs-lookup"><span data-stu-id="d0420-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="d0420-124">x</span><span class="sxs-lookup"><span data-stu-id="d0420-124">x</span></span>    | <span data-ttu-id="d0420-125">x</span><span class="sxs-lookup"><span data-stu-id="d0420-125">x</span></span>    | <span data-ttu-id="d0420-126">x</span><span class="sxs-lookup"><span data-stu-id="d0420-126">x</span></span>     | <span data-ttu-id="d0420-127">x</span><span class="sxs-lookup"><span data-stu-id="d0420-127">x</span></span>    | <span data-ttu-id="d0420-128">x</span><span class="sxs-lookup"><span data-stu-id="d0420-128">x</span></span>     |



 

<span data-ttu-id="d0420-129">如果輸入正好是1.0，則輸出必須正好為1.0。</span><span class="sxs-lookup"><span data-stu-id="d0420-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="d0420-130">0.0 的來源會產生無限大。</span><span class="sxs-lookup"><span data-stu-id="d0420-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="d0420-131">純量結果會複寫至目的地寫入遮罩中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="d0420-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="d0420-132">精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，2.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。</span><span class="sxs-lookup"><span data-stu-id="d0420-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0420-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0420-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0420-134">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="d0420-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




