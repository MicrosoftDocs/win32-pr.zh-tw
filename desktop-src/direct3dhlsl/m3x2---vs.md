---
title: m3x2-vs
description: 將3個元件向量乘以3x2 矩陣。 |m3x2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195937"
---
# <a name="m3x2---vs"></a><span data-ttu-id="9609a-104">m3x2-vs</span><span class="sxs-lookup"><span data-stu-id="9609a-104">m3x2 - vs</span></span>

<span data-ttu-id="9609a-105">將3個元件向量乘以3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="9609a-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9609a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9609a-106">Syntax</span></span>



| <span data-ttu-id="9609a-107">m3x2 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="9609a-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="9609a-108">其中</span><span class="sxs-lookup"><span data-stu-id="9609a-108">where</span></span>

-   <span data-ttu-id="9609a-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="9609a-109">dst is the destination register.</span></span> <span data-ttu-id="9609a-110">結果是2個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="9609a-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="9609a-111">src0 是代表3個元件向量的來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="9609a-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="9609a-112">src1 是代表3x2 矩陣的來源暫存器，它會對應到2個連續暫存器中的第一個。</span><span class="sxs-lookup"><span data-stu-id="9609a-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="9609a-113">備註</span><span class="sxs-lookup"><span data-stu-id="9609a-113">Remarks</span></span>



| <span data-ttu-id="9609a-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="9609a-114">Vertex shader versions</span></span> | <span data-ttu-id="9609a-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9609a-115">1\_1</span></span> | <span data-ttu-id="9609a-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9609a-116">2\_0</span></span> | <span data-ttu-id="9609a-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9609a-117">2\_x</span></span> | <span data-ttu-id="9609a-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9609a-118">2\_sw</span></span> | <span data-ttu-id="9609a-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9609a-119">3\_0</span></span> | <span data-ttu-id="9609a-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9609a-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9609a-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="9609a-121">m3x2</span></span>                   | <span data-ttu-id="9609a-122">x</span><span class="sxs-lookup"><span data-stu-id="9609a-122">x</span></span>    | <span data-ttu-id="9609a-123">x</span><span class="sxs-lookup"><span data-stu-id="9609a-123">x</span></span>    | <span data-ttu-id="9609a-124">x</span><span class="sxs-lookup"><span data-stu-id="9609a-124">x</span></span>    | <span data-ttu-id="9609a-125">x</span><span class="sxs-lookup"><span data-stu-id="9609a-125">x</span></span>     | <span data-ttu-id="9609a-126">x</span><span class="sxs-lookup"><span data-stu-id="9609a-126">x</span></span>    | <span data-ttu-id="9609a-127">x</span><span class="sxs-lookup"><span data-stu-id="9609a-127">x</span></span>     |



 

<span data-ttu-id="9609a-128">目的地註冊需要 xy 遮罩。</span><span class="sxs-lookup"><span data-stu-id="9609a-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="9609a-129">Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。</span><span class="sxs-lookup"><span data-stu-id="9609a-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="9609a-130">下列方會顯示指令的運作方式：</span><span class="sxs-lookup"><span data-stu-id="9609a-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="9609a-131">輸入向量位於 register src0 中。</span><span class="sxs-lookup"><span data-stu-id="9609a-131">The input vector is in register src0.</span></span> <span data-ttu-id="9609a-132">輸入3x2 矩陣位於登錄 src1 和下一個較高的註冊檔中，如下列擴充所示。</span><span class="sxs-lookup"><span data-stu-id="9609a-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="9609a-133">會產生2D 結果，而將目的地暫存器的其他元素 (的 destination 和 dest) 不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="9609a-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="9609a-134">這項作業通常用於2D 轉換。</span><span class="sxs-lookup"><span data-stu-id="9609a-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="9609a-135">此指示會實作為一對點產品，如下所示。</span><span class="sxs-lookup"><span data-stu-id="9609a-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="9609a-136">Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="9609a-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="9609a-137">目的地和 src0 暫存器，或任何 src1 + i 暫存器都不能相同。</span><span class="sxs-lookup"><span data-stu-id="9609a-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9609a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="9609a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9609a-139">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="9609a-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




