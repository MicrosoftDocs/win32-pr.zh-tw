---
title: dp2add-ps
description: 執行2D 點乘積和純量加法。
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092447"
---
# <a name="dp2add---ps"></a><span data-ttu-id="e1780-103">dp2add-ps</span><span class="sxs-lookup"><span data-stu-id="e1780-103">dp2add - ps</span></span>

<span data-ttu-id="e1780-104">執行2D 點乘積和純量加法。</span><span class="sxs-lookup"><span data-stu-id="e1780-104">Performs a 2D dot product and a scalar addition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1780-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1780-105">Syntax</span></span>


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



<span data-ttu-id="e1780-106">其中：</span><span class="sxs-lookup"><span data-stu-id="e1780-106">Where:</span></span>

-   <span data-ttu-id="e1780-107">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e1780-107">dst is a destination register.</span></span>
-   <span data-ttu-id="e1780-108">src0、src1 和 src2 收取都是三個來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e1780-108">src0, src1, and src2 are three source registers.</span></span>
-   <span data-ttu-id="e1780-109">{x \| y \| z \| w} 是 src2 收取上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="e1780-109">{x\|y\|z\|w} is the required replicate swizzle on src2.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1780-110">備註</span><span class="sxs-lookup"><span data-stu-id="e1780-110">Remarks</span></span>



| <span data-ttu-id="e1780-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e1780-111">Pixel shader versions</span></span> | <span data-ttu-id="e1780-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e1780-112">1\_1</span></span> | <span data-ttu-id="e1780-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e1780-113">1\_2</span></span> | <span data-ttu-id="e1780-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e1780-114">1\_3</span></span> | <span data-ttu-id="e1780-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e1780-115">1\_4</span></span> | <span data-ttu-id="e1780-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1780-116">2\_0</span></span> | <span data-ttu-id="e1780-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e1780-117">2\_x</span></span> | <span data-ttu-id="e1780-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e1780-118">2\_sw</span></span> | <span data-ttu-id="e1780-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1780-119">3\_0</span></span> | <span data-ttu-id="e1780-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e1780-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e1780-121">dp2add</span><span class="sxs-lookup"><span data-stu-id="e1780-121">dp2add</span></span>                |      |      |      |      | <span data-ttu-id="e1780-122">x</span><span class="sxs-lookup"><span data-stu-id="e1780-122">x</span></span>    | <span data-ttu-id="e1780-123">x</span><span class="sxs-lookup"><span data-stu-id="e1780-123">x</span></span>    | <span data-ttu-id="e1780-124">x</span><span class="sxs-lookup"><span data-stu-id="e1780-124">x</span></span>     | <span data-ttu-id="e1780-125">x</span><span class="sxs-lookup"><span data-stu-id="e1780-125">x</span></span>    | <span data-ttu-id="e1780-126">x</span><span class="sxs-lookup"><span data-stu-id="e1780-126">x</span></span>     |



 

<span data-ttu-id="e1780-127">Add 的純量值是由 src2 收取上的複寫 swizzle 所選擇。</span><span class="sxs-lookup"><span data-stu-id="e1780-127">The scalar value for add is chosen by the replicate swizzle on src2.</span></span>

<span data-ttu-id="e1780-128">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="e1780-128">The following code snippet shows the operations performed.</span></span>


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a><span data-ttu-id="e1780-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1780-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1780-130">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e1780-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




