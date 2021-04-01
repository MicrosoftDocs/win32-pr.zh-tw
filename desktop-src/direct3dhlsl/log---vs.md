---
title: 記錄檔-vs
description: Full precision log ₂ (x) 。 |記錄檔-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196020"
---
# <a name="log---vs"></a><span data-ttu-id="37015-104">記錄檔-vs</span><span class="sxs-lookup"><span data-stu-id="37015-104">log - vs</span></span>

<span data-ttu-id="37015-105">Full precision log ₂ (x) 。</span><span class="sxs-lookup"><span data-stu-id="37015-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="37015-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37015-106">Syntax</span></span>



| <span data-ttu-id="37015-107">記錄 dst、src</span><span class="sxs-lookup"><span data-stu-id="37015-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="37015-108">其中</span><span class="sxs-lookup"><span data-stu-id="37015-108">where</span></span>

-   <span data-ttu-id="37015-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="37015-109">dst is the destination register.</span></span>
-   <span data-ttu-id="37015-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="37015-110">src is a source register.</span></span> <span data-ttu-id="37015-111">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="37015-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="37015-112">備註</span><span class="sxs-lookup"><span data-stu-id="37015-112">Remarks</span></span>



| <span data-ttu-id="37015-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="37015-113">Vertex shader versions</span></span> | <span data-ttu-id="37015-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="37015-114">1\_1</span></span> | <span data-ttu-id="37015-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37015-115">2\_0</span></span> | <span data-ttu-id="37015-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37015-116">2\_x</span></span> | <span data-ttu-id="37015-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="37015-117">2\_sw</span></span> | <span data-ttu-id="37015-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37015-118">3\_0</span></span> | <span data-ttu-id="37015-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="37015-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="37015-120">log</span><span class="sxs-lookup"><span data-stu-id="37015-120">log</span></span>                    | <span data-ttu-id="37015-121">x</span><span class="sxs-lookup"><span data-stu-id="37015-121">x</span></span>    | <span data-ttu-id="37015-122">x</span><span class="sxs-lookup"><span data-stu-id="37015-122">x</span></span>    | <span data-ttu-id="37015-123">x</span><span class="sxs-lookup"><span data-stu-id="37015-123">x</span></span>    | <span data-ttu-id="37015-124">x</span><span class="sxs-lookup"><span data-stu-id="37015-124">x</span></span>     | <span data-ttu-id="37015-125">x</span><span class="sxs-lookup"><span data-stu-id="37015-125">x</span></span>    | <span data-ttu-id="37015-126">x</span><span class="sxs-lookup"><span data-stu-id="37015-126">x</span></span>     |



 

<span data-ttu-id="37015-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="37015-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="37015-128">此指示會接受已忽略其正負號位的純量來源。</span><span class="sxs-lookup"><span data-stu-id="37015-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="37015-129">結果會複寫到所有的四個通道。</span><span class="sxs-lookup"><span data-stu-id="37015-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="37015-130">此指令提供21位精確度。</span><span class="sxs-lookup"><span data-stu-id="37015-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37015-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="37015-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37015-132">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="37015-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




