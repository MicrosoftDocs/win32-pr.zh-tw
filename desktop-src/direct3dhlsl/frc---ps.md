---
title: frc-ps
description: 傳回每個輸入元件的小數部分。 |frc-ps
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322343"
---
# <a name="frc---ps"></a><span data-ttu-id="ef1ac-104">frc-ps</span><span class="sxs-lookup"><span data-stu-id="ef1ac-104">frc - ps</span></span>

<span data-ttu-id="ef1ac-105">傳回每個輸入元件的小數部分。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1ac-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef1ac-106">Syntax</span></span>



| <span data-ttu-id="ef1ac-107">frc dst、src</span><span class="sxs-lookup"><span data-stu-id="ef1ac-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ef1ac-108">其中</span><span class="sxs-lookup"><span data-stu-id="ef1ac-108">where</span></span>

-   <span data-ttu-id="ef1ac-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ef1ac-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1ac-111">備註</span><span class="sxs-lookup"><span data-stu-id="ef1ac-111">Remarks</span></span>



| <span data-ttu-id="ef1ac-112">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="ef1ac-112">Pixel shader versions</span></span> | <span data-ttu-id="ef1ac-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ef1ac-113">1\_1</span></span> | <span data-ttu-id="ef1ac-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="ef1ac-114">1\_2</span></span> | <span data-ttu-id="ef1ac-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ef1ac-115">1\_3</span></span> | <span data-ttu-id="ef1ac-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="ef1ac-116">1\_4</span></span> | <span data-ttu-id="ef1ac-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef1ac-117">2\_0</span></span> | <span data-ttu-id="ef1ac-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-118">2\_x</span></span> | <span data-ttu-id="ef1ac-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ef1ac-119">2\_sw</span></span> | <span data-ttu-id="ef1ac-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef1ac-120">3\_0</span></span> | <span data-ttu-id="ef1ac-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ef1ac-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ef1ac-122">Frc</span><span class="sxs-lookup"><span data-stu-id="ef1ac-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="ef1ac-123">x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-123">x</span></span>    | <span data-ttu-id="ef1ac-124">x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-124">x</span></span>    | <span data-ttu-id="ef1ac-125">x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-125">x</span></span>     | <span data-ttu-id="ef1ac-126">x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-126">x</span></span>    | <span data-ttu-id="ef1ac-127">x</span><span class="sxs-lookup"><span data-stu-id="ef1ac-127">x</span></span>     |



 

<span data-ttu-id="ef1ac-128">下列程式碼片段會以概念方式顯示指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="ef1ac-129">Floor 函數會將傳入的引數轉換成小於 (或等於) 引數的最大整數。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="ef1ac-130">這會轉換成浮點數，然後將原始值減去從。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="ef1ac-131">產生的小數值範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="ef1ac-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef1ac-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef1ac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef1ac-133">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="ef1ac-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




