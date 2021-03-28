---
title: 記錄-ps
description: Full precision log ₂ (x) 。 |記錄-ps
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974388"
---
# <a name="log---ps"></a><span data-ttu-id="e61f5-104">記錄-ps</span><span class="sxs-lookup"><span data-stu-id="e61f5-104">log - ps</span></span>

<span data-ttu-id="e61f5-105">Full precision log ₂ (x) 。</span><span class="sxs-lookup"><span data-stu-id="e61f5-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="e61f5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e61f5-106">Syntax</span></span>



| <span data-ttu-id="e61f5-107">記錄 dst、src</span><span class="sxs-lookup"><span data-stu-id="e61f5-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e61f5-108">其中</span><span class="sxs-lookup"><span data-stu-id="e61f5-108">where</span></span>

-   <span data-ttu-id="e61f5-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e61f5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e61f5-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e61f5-110">src is a source register.</span></span> <span data-ttu-id="e61f5-111">來源註冊需要明確使用複寫 swizzle;也就是，您必須指定一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="e61f5-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e61f5-112">備註</span><span class="sxs-lookup"><span data-stu-id="e61f5-112">Remarks</span></span>



| <span data-ttu-id="e61f5-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e61f5-113">Pixel shader versions</span></span> | <span data-ttu-id="e61f5-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e61f5-114">1\_1</span></span> | <span data-ttu-id="e61f5-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e61f5-115">1\_2</span></span> | <span data-ttu-id="e61f5-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e61f5-116">1\_3</span></span> | <span data-ttu-id="e61f5-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e61f5-117">1\_4</span></span> | <span data-ttu-id="e61f5-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e61f5-118">2\_0</span></span> | <span data-ttu-id="e61f5-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e61f5-119">2\_x</span></span> | <span data-ttu-id="e61f5-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e61f5-120">2\_sw</span></span> | <span data-ttu-id="e61f5-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e61f5-121">3\_0</span></span> | <span data-ttu-id="e61f5-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e61f5-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e61f5-123">log</span><span class="sxs-lookup"><span data-stu-id="e61f5-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="e61f5-124">x</span><span class="sxs-lookup"><span data-stu-id="e61f5-124">x</span></span>    | <span data-ttu-id="e61f5-125">x</span><span class="sxs-lookup"><span data-stu-id="e61f5-125">x</span></span>    | <span data-ttu-id="e61f5-126">x</span><span class="sxs-lookup"><span data-stu-id="e61f5-126">x</span></span>     | <span data-ttu-id="e61f5-127">x</span><span class="sxs-lookup"><span data-stu-id="e61f5-127">x</span></span>    | <span data-ttu-id="e61f5-128">x</span><span class="sxs-lookup"><span data-stu-id="e61f5-128">x</span></span>     |



 

<span data-ttu-id="e61f5-129">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="e61f5-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="e61f5-130">此指示會接受已忽略其正負號位的純量來源。</span><span class="sxs-lookup"><span data-stu-id="e61f5-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="e61f5-131">結果會複寫到所有的四個通道。</span><span class="sxs-lookup"><span data-stu-id="e61f5-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e61f5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e61f5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e61f5-133">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e61f5-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




