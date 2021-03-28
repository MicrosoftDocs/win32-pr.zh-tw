---
title: m4x3-ps
description: 將4個元件向量乘以4x3 矩陣。 |m4x3-ps
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974340"
---
# <a name="m4x3---ps"></a><span data-ttu-id="938a9-104">m4x3-ps</span><span class="sxs-lookup"><span data-stu-id="938a9-104">m4x3 - ps</span></span>

<span data-ttu-id="938a9-105">將4個元件向量乘以4x3 矩陣。</span><span class="sxs-lookup"><span data-stu-id="938a9-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="938a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="938a9-106">Syntax</span></span>



| <span data-ttu-id="938a9-107">m4x3 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="938a9-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="938a9-108">其中</span><span class="sxs-lookup"><span data-stu-id="938a9-108">where</span></span>

-   <span data-ttu-id="938a9-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="938a9-109">dst is the destination register.</span></span> <span data-ttu-id="938a9-110">結果是3個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="938a9-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="938a9-111">src0 是代表4元件向量的來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="938a9-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="938a9-112">src1 是代表4x3 矩陣的來源暫存器，它會對應至3個連續暫存器中的第一個。</span><span class="sxs-lookup"><span data-stu-id="938a9-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="938a9-113">備註</span><span class="sxs-lookup"><span data-stu-id="938a9-113">Remarks</span></span>



| <span data-ttu-id="938a9-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="938a9-114">Pixel shader versions</span></span> | <span data-ttu-id="938a9-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="938a9-115">1\_1</span></span> | <span data-ttu-id="938a9-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="938a9-116">1\_2</span></span> | <span data-ttu-id="938a9-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="938a9-117">1\_3</span></span> | <span data-ttu-id="938a9-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="938a9-118">1\_4</span></span> | <span data-ttu-id="938a9-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="938a9-119">2\_0</span></span> | <span data-ttu-id="938a9-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="938a9-120">2\_x</span></span> | <span data-ttu-id="938a9-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="938a9-121">2\_sw</span></span> | <span data-ttu-id="938a9-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="938a9-122">3\_0</span></span> | <span data-ttu-id="938a9-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="938a9-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="938a9-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="938a9-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="938a9-125">x</span><span class="sxs-lookup"><span data-stu-id="938a9-125">x</span></span>    | <span data-ttu-id="938a9-126">x</span><span class="sxs-lookup"><span data-stu-id="938a9-126">x</span></span>    | <span data-ttu-id="938a9-127">x</span><span class="sxs-lookup"><span data-stu-id="938a9-127">x</span></span>     | <span data-ttu-id="938a9-128">x</span><span class="sxs-lookup"><span data-stu-id="938a9-128">x</span></span>    | <span data-ttu-id="938a9-129">x</span><span class="sxs-lookup"><span data-stu-id="938a9-129">x</span></span>     |



 

<span data-ttu-id="938a9-130">目的地註冊需要 xyz mask。</span><span class="sxs-lookup"><span data-stu-id="938a9-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="938a9-131">Src0 允許否定和 swizzle 修飾詞，但不允許 src1。</span><span class="sxs-lookup"><span data-stu-id="938a9-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="938a9-132">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="938a9-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="938a9-133">輸入向量位於 register src0 中。</span><span class="sxs-lookup"><span data-stu-id="938a9-133">The input vector is in register src0.</span></span> <span data-ttu-id="938a9-134">輸入4x3 矩陣位於 register src1 和接下來的兩個較高的暫存器中，如下列擴充所示。</span><span class="sxs-lookup"><span data-stu-id="938a9-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="938a9-135">產生3D 結果，讓目的地登錄的另一個元素 (的) 不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="938a9-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="938a9-136">這項作業通常用來將位置向量轉換為沒有 projective 效果的矩陣，例如模型空間轉換時。</span><span class="sxs-lookup"><span data-stu-id="938a9-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="938a9-137">此指令會實作為一組點乘積，如下所示。</span><span class="sxs-lookup"><span data-stu-id="938a9-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="938a9-138">Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="938a9-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="938a9-139">Dst 和 src0 暫存器不能相同。</span><span class="sxs-lookup"><span data-stu-id="938a9-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="938a9-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="938a9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="938a9-141">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="938a9-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




