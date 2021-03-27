---
title: dst-vs
description: 計算距離向量。 |dst-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853611"
---
# <a name="dst---vs"></a><span data-ttu-id="261b3-104">dst-vs</span><span class="sxs-lookup"><span data-stu-id="261b3-104">dst - vs</span></span>

<span data-ttu-id="261b3-105">計算距離向量。</span><span class="sxs-lookup"><span data-stu-id="261b3-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="261b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="261b3-106">Syntax</span></span>



| <span data-ttu-id="261b3-107">dst dest、src0、src1</span><span class="sxs-lookup"><span data-stu-id="261b3-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="261b3-108">其中</span><span class="sxs-lookup"><span data-stu-id="261b3-108">where</span></span>

-   <span data-ttu-id="261b3-109">dest 是目的地暫存器。</span><span class="sxs-lookup"><span data-stu-id="261b3-109">dest is the destination register.</span></span>
-   <span data-ttu-id="261b3-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="261b3-110">src0 is a source register.</span></span>
-   <span data-ttu-id="261b3-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="261b3-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="261b3-112">備註</span><span class="sxs-lookup"><span data-stu-id="261b3-112">Remarks</span></span>



| <span data-ttu-id="261b3-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="261b3-113">Vertex shader versions</span></span> | <span data-ttu-id="261b3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="261b3-114">1\_1</span></span> | <span data-ttu-id="261b3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="261b3-115">2\_0</span></span> | <span data-ttu-id="261b3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="261b3-116">2\_x</span></span> | <span data-ttu-id="261b3-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="261b3-117">2\_sw</span></span> | <span data-ttu-id="261b3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="261b3-118">3\_0</span></span> | <span data-ttu-id="261b3-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="261b3-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="261b3-120">Dst</span><span class="sxs-lookup"><span data-stu-id="261b3-120">dst</span></span>                    | <span data-ttu-id="261b3-121">x</span><span class="sxs-lookup"><span data-stu-id="261b3-121">x</span></span>    | <span data-ttu-id="261b3-122">x</span><span class="sxs-lookup"><span data-stu-id="261b3-122">x</span></span>    | <span data-ttu-id="261b3-123">x</span><span class="sxs-lookup"><span data-stu-id="261b3-123">x</span></span>    | <span data-ttu-id="261b3-124">x</span><span class="sxs-lookup"><span data-stu-id="261b3-124">x</span></span>     | <span data-ttu-id="261b3-125">x</span><span class="sxs-lookup"><span data-stu-id="261b3-125">x</span></span>    | <span data-ttu-id="261b3-126">x</span><span class="sxs-lookup"><span data-stu-id="261b3-126">x</span></span>     |



 

<span data-ttu-id="261b3-127">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="261b3-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="261b3-128">第一個來源運算元 (src0) 會假設為向量 (忽略、d \* d、d \* d、忽略) ，而第二個來源運算元 (src1) 會假設為向量 (忽略、1/d、忽略、1/d) 。</span><span class="sxs-lookup"><span data-stu-id="261b3-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="261b3-129">目的地 (dest) 是結果向量 (1、d、d \* d、1/d) 。</span><span class="sxs-lookup"><span data-stu-id="261b3-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="261b3-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="261b3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="261b3-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="261b3-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




