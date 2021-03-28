---
title: logp-vs
description: 部分有效位數 logp ₂ (x) 。
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022827"
---
# <a name="logp---vs"></a><span data-ttu-id="a9d4f-103">logp-vs</span><span class="sxs-lookup"><span data-stu-id="a9d4f-103">logp - vs</span></span>

<span data-ttu-id="a9d4f-104">部分有效位數 logp ₂ (x) 。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d4f-105">Syntax</span></span>



| <span data-ttu-id="a9d4f-106">logp dst、src</span><span class="sxs-lookup"><span data-stu-id="a9d4f-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="a9d4f-107">其中</span><span class="sxs-lookup"><span data-stu-id="a9d4f-107">where</span></span>

-   <span data-ttu-id="a9d4f-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-108">dst is the destination register.</span></span>
-   <span data-ttu-id="a9d4f-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-109">src is a source register.</span></span> <span data-ttu-id="a9d4f-110">來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d4f-111">備註</span><span class="sxs-lookup"><span data-stu-id="a9d4f-111">Remarks</span></span>



| <span data-ttu-id="a9d4f-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="a9d4f-112">Vertex shader versions</span></span> | <span data-ttu-id="a9d4f-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="a9d4f-113">1\_1</span></span> | <span data-ttu-id="a9d4f-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9d4f-114">2\_0</span></span> | <span data-ttu-id="a9d4f-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-115">2\_x</span></span> | <span data-ttu-id="a9d4f-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a9d4f-116">2\_sw</span></span> | <span data-ttu-id="a9d4f-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9d4f-117">3\_0</span></span> | <span data-ttu-id="a9d4f-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a9d4f-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a9d4f-119">logp</span><span class="sxs-lookup"><span data-stu-id="a9d4f-119">logp</span></span>                   | <span data-ttu-id="a9d4f-120">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-120">x</span></span>    | <span data-ttu-id="a9d4f-121">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-121">x</span></span>    | <span data-ttu-id="a9d4f-122">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-122">x</span></span>    | <span data-ttu-id="a9d4f-123">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-123">x</span></span>     | <span data-ttu-id="a9d4f-124">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-124">x</span></span>    | <span data-ttu-id="a9d4f-125">x</span><span class="sxs-lookup"><span data-stu-id="a9d4f-125">x</span></span>     |



 

<span data-ttu-id="a9d4f-126">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="a9d4f-127">此指令提供以2部分精確度為底數的對數，最多可達10個位。</span><span class="sxs-lookup"><span data-stu-id="a9d4f-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9d4f-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9d4f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d4f-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="a9d4f-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




