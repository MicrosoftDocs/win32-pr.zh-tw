---
title: m3x4-vs
description: 將3個元件向量乘以3x4 圓矩陣。 |m3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974025"
---
# <a name="m3x4---vs"></a><span data-ttu-id="82620-104">m3x4-vs</span><span class="sxs-lookup"><span data-stu-id="82620-104">m3x4 - vs</span></span>

<span data-ttu-id="82620-105">將3個元件向量乘以3x4 圓矩陣。</span><span class="sxs-lookup"><span data-stu-id="82620-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="82620-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="82620-106">Syntax</span></span>



| <span data-ttu-id="82620-107">m3x4 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="82620-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="82620-108">其中</span><span class="sxs-lookup"><span data-stu-id="82620-108">where</span></span>

-   <span data-ttu-id="82620-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="82620-109">dst is the destination register.</span></span> <span data-ttu-id="82620-110">結果是4個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="82620-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="82620-111">src0 是代表3個元件向量的來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="82620-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="82620-112">src1 是代表3x4 圓矩陣的來源暫存器，它會對應至4個連續暫存器中的第一個。</span><span class="sxs-lookup"><span data-stu-id="82620-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="82620-113">備註</span><span class="sxs-lookup"><span data-stu-id="82620-113">Remarks</span></span>



| <span data-ttu-id="82620-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="82620-114">Vertex shader versions</span></span> | <span data-ttu-id="82620-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="82620-115">1\_1</span></span> | <span data-ttu-id="82620-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82620-116">2\_0</span></span> | <span data-ttu-id="82620-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="82620-117">2\_x</span></span> | <span data-ttu-id="82620-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="82620-118">2\_sw</span></span> | <span data-ttu-id="82620-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82620-119">3\_0</span></span> | <span data-ttu-id="82620-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="82620-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="82620-121">m3x4</span><span class="sxs-lookup"><span data-stu-id="82620-121">m3x4</span></span>                   | <span data-ttu-id="82620-122">x</span><span class="sxs-lookup"><span data-stu-id="82620-122">x</span></span>    | <span data-ttu-id="82620-123">x</span><span class="sxs-lookup"><span data-stu-id="82620-123">x</span></span>    | <span data-ttu-id="82620-124">x</span><span class="sxs-lookup"><span data-stu-id="82620-124">x</span></span>    | <span data-ttu-id="82620-125">x</span><span class="sxs-lookup"><span data-stu-id="82620-125">x</span></span>     | <span data-ttu-id="82620-126">x</span><span class="sxs-lookup"><span data-stu-id="82620-126">x</span></span>    | <span data-ttu-id="82620-127">x</span><span class="sxs-lookup"><span data-stu-id="82620-127">x</span></span>     |



 

<span data-ttu-id="82620-128">目的地註冊需要 xyzw (預設) 遮罩。</span><span class="sxs-lookup"><span data-stu-id="82620-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="82620-129">Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。</span><span class="sxs-lookup"><span data-stu-id="82620-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="82620-130">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="82620-130">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



<span data-ttu-id="82620-131">輸入向量位於 register src0 中。</span><span class="sxs-lookup"><span data-stu-id="82620-131">The input vector is in register src0.</span></span> <span data-ttu-id="82620-132">輸入3x4 圓矩陣位於 register src1 和後續三個較高的暫存器中，如下列擴充所示。</span><span class="sxs-lookup"><span data-stu-id="82620-132">The input 3x4 matrix is in register src1 and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="82620-133">這項作業通常用來透過具有 projective 效果但未套用轉譯的矩陣來轉換位置向量。</span><span class="sxs-lookup"><span data-stu-id="82620-133">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="82620-134">此指示會實作為一對點產品，如下所示。</span><span class="sxs-lookup"><span data-stu-id="82620-134">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="82620-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="82620-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82620-136">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="82620-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




