---
title: m4x4-vs
description: 將4個元件向量乘以4x4 矩陣。 |m4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195934"
---
# <a name="m4x4---vs"></a><span data-ttu-id="fb36d-104">m4x4-vs</span><span class="sxs-lookup"><span data-stu-id="fb36d-104">m4x4 - vs</span></span>

<span data-ttu-id="fb36d-105">將4個元件向量乘以4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="fb36d-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb36d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb36d-106">Syntax</span></span>



| <span data-ttu-id="fb36d-107">m4x4 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="fb36d-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="fb36d-108">其中</span><span class="sxs-lookup"><span data-stu-id="fb36d-108">where</span></span>

-   <span data-ttu-id="fb36d-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="fb36d-109">dst is the destination register.</span></span> <span data-ttu-id="fb36d-110">結果是4個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="fb36d-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="fb36d-111">src0 是代表4元件向量的來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="fb36d-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="fb36d-112">src1 是代表4x4 矩陣的來源暫存器，它會對應至4個連續暫存器中的第一個。</span><span class="sxs-lookup"><span data-stu-id="fb36d-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb36d-113">備註</span><span class="sxs-lookup"><span data-stu-id="fb36d-113">Remarks</span></span>



| <span data-ttu-id="fb36d-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="fb36d-114">Vertex shader versions</span></span> | <span data-ttu-id="fb36d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="fb36d-115">1\_1</span></span> | <span data-ttu-id="fb36d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fb36d-116">2\_0</span></span> | <span data-ttu-id="fb36d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fb36d-117">2\_x</span></span> | <span data-ttu-id="fb36d-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fb36d-118">2\_sw</span></span> | <span data-ttu-id="fb36d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fb36d-119">3\_0</span></span> | <span data-ttu-id="fb36d-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fb36d-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fb36d-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="fb36d-121">m4x4</span></span>                   | <span data-ttu-id="fb36d-122">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-122">x</span></span>    | <span data-ttu-id="fb36d-123">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-123">x</span></span>    | <span data-ttu-id="fb36d-124">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-124">x</span></span>    | <span data-ttu-id="fb36d-125">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-125">x</span></span>     | <span data-ttu-id="fb36d-126">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-126">x</span></span>    | <span data-ttu-id="fb36d-127">x</span><span class="sxs-lookup"><span data-stu-id="fb36d-127">x</span></span>     |



 

<span data-ttu-id="fb36d-128">目的地註冊需要 xyzw (預設) 遮罩。</span><span class="sxs-lookup"><span data-stu-id="fb36d-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="fb36d-129">Src0 允許否定和 swizzle 修飾詞，但不允許 src1。</span><span class="sxs-lookup"><span data-stu-id="fb36d-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="fb36d-130">Swizzle 和否定修飾詞對 src0 暫存器而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="fb36d-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="fb36d-131">目的地和 src0 暫存器不可以相同。</span><span class="sxs-lookup"><span data-stu-id="fb36d-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="fb36d-132">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="fb36d-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="fb36d-133">輸入向量位於 register src0 中。</span><span class="sxs-lookup"><span data-stu-id="fb36d-133">The input vector is in register src0.</span></span> <span data-ttu-id="fb36d-134">輸入4x4 矩陣位於 register src1 和後續三個較高的暫存器中，如下列擴充所示。</span><span class="sxs-lookup"><span data-stu-id="fb36d-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="fb36d-135">這項作業通常用來將位置轉換成投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="fb36d-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="fb36d-136">此指示會實作為一系列的點乘積，如下所示。</span><span class="sxs-lookup"><span data-stu-id="fb36d-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="fb36d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb36d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb36d-138">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="fb36d-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




