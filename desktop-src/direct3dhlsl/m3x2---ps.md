---
title: m3x2-ps
description: 將3個元件向量乘以3x2 矩陣。 |m3x2-ps
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974385"
---
# <a name="m3x2---ps"></a><span data-ttu-id="107a5-104">m3x2-ps</span><span class="sxs-lookup"><span data-stu-id="107a5-104">m3x2 - ps</span></span>

<span data-ttu-id="107a5-105">將3個元件向量乘以3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="107a5-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="107a5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="107a5-106">Syntax</span></span>



| <span data-ttu-id="107a5-107">m3x2 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="107a5-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="107a5-108">其中</span><span class="sxs-lookup"><span data-stu-id="107a5-108">where</span></span>

-   <span data-ttu-id="107a5-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="107a5-109">dst is the destination register.</span></span> <span data-ttu-id="107a5-110">結果是2個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="107a5-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="107a5-111">src0 是代表3個元件向量的來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="107a5-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="107a5-112">src1 是代表3x2 矩陣的來源暫存器，它會對應到2個連續暫存器中的第一個。</span><span class="sxs-lookup"><span data-stu-id="107a5-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="107a5-113">備註</span><span class="sxs-lookup"><span data-stu-id="107a5-113">Remarks</span></span>



| <span data-ttu-id="107a5-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="107a5-114">Pixel shader versions</span></span> | <span data-ttu-id="107a5-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="107a5-115">1\_1</span></span> | <span data-ttu-id="107a5-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="107a5-116">1\_2</span></span> | <span data-ttu-id="107a5-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="107a5-117">1\_3</span></span> | <span data-ttu-id="107a5-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="107a5-118">1\_4</span></span> | <span data-ttu-id="107a5-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="107a5-119">2\_0</span></span> | <span data-ttu-id="107a5-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="107a5-120">2\_x</span></span> | <span data-ttu-id="107a5-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="107a5-121">2\_sw</span></span> | <span data-ttu-id="107a5-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="107a5-122">3\_0</span></span> | <span data-ttu-id="107a5-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="107a5-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="107a5-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="107a5-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="107a5-125">x</span><span class="sxs-lookup"><span data-stu-id="107a5-125">x</span></span>    | <span data-ttu-id="107a5-126">x</span><span class="sxs-lookup"><span data-stu-id="107a5-126">x</span></span>    | <span data-ttu-id="107a5-127">x</span><span class="sxs-lookup"><span data-stu-id="107a5-127">x</span></span>     | <span data-ttu-id="107a5-128">x</span><span class="sxs-lookup"><span data-stu-id="107a5-128">x</span></span>    | <span data-ttu-id="107a5-129">x</span><span class="sxs-lookup"><span data-stu-id="107a5-129">x</span></span>     |



 

<span data-ttu-id="107a5-130">目的地註冊需要 xy 遮罩。</span><span class="sxs-lookup"><span data-stu-id="107a5-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="107a5-131">Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。</span><span class="sxs-lookup"><span data-stu-id="107a5-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="107a5-132">下列方會顯示指令的運作方式：</span><span class="sxs-lookup"><span data-stu-id="107a5-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="107a5-133">輸入向量位於 register src0 中。</span><span class="sxs-lookup"><span data-stu-id="107a5-133">The input vector is in register src0.</span></span> <span data-ttu-id="107a5-134">輸入3x2 矩陣位於登錄 src1 和下一個較高的註冊檔中，如下列擴充所示。</span><span class="sxs-lookup"><span data-stu-id="107a5-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="107a5-135">會產生2D 結果，而將目的地暫存器的其他元素 (的 destination 和 dest) 不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="107a5-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="107a5-136">這項作業通常用於2D 轉換。</span><span class="sxs-lookup"><span data-stu-id="107a5-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="107a5-137">此指示會實作為一對點產品，如下所示。</span><span class="sxs-lookup"><span data-stu-id="107a5-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="107a5-138">Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="107a5-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="107a5-139">Dst 和 src0 暫存器或 src1 + i 註冊的任何一個都不能相同。</span><span class="sxs-lookup"><span data-stu-id="107a5-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="107a5-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="107a5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="107a5-141">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="107a5-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




