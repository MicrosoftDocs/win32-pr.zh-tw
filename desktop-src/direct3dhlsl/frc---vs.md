---
title: frc-vs
description: 傳回每個輸入元件的小數部分。 |frc-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322340"
---
# <a name="frc---vs"></a><span data-ttu-id="c6518-104">frc-vs</span><span class="sxs-lookup"><span data-stu-id="c6518-104">frc - vs</span></span>

<span data-ttu-id="c6518-105">傳回每個輸入元件的小數部分。</span><span class="sxs-lookup"><span data-stu-id="c6518-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6518-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6518-106">Syntax</span></span>



| <span data-ttu-id="c6518-107">frc dst、src</span><span class="sxs-lookup"><span data-stu-id="c6518-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="c6518-108">其中</span><span class="sxs-lookup"><span data-stu-id="c6518-108">where</span></span>

-   <span data-ttu-id="c6518-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="c6518-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c6518-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="c6518-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6518-111">備註</span><span class="sxs-lookup"><span data-stu-id="c6518-111">Remarks</span></span>



| <span data-ttu-id="c6518-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="c6518-112">Vertex shader versions</span></span> | <span data-ttu-id="c6518-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="c6518-113">1\_1</span></span> | <span data-ttu-id="c6518-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c6518-114">2\_0</span></span> | <span data-ttu-id="c6518-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c6518-115">2\_x</span></span> | <span data-ttu-id="c6518-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c6518-116">2\_sw</span></span> | <span data-ttu-id="c6518-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c6518-117">3\_0</span></span> | <span data-ttu-id="c6518-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c6518-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c6518-119">Frc</span><span class="sxs-lookup"><span data-stu-id="c6518-119">frc</span></span>                    | <span data-ttu-id="c6518-120">x</span><span class="sxs-lookup"><span data-stu-id="c6518-120">x</span></span>    | <span data-ttu-id="c6518-121">x</span><span class="sxs-lookup"><span data-stu-id="c6518-121">x</span></span>    | <span data-ttu-id="c6518-122">x</span><span class="sxs-lookup"><span data-stu-id="c6518-122">x</span></span>    | <span data-ttu-id="c6518-123">x</span><span class="sxs-lookup"><span data-stu-id="c6518-123">x</span></span>     | <span data-ttu-id="c6518-124">x</span><span class="sxs-lookup"><span data-stu-id="c6518-124">x</span></span>    | <span data-ttu-id="c6518-125">x</span><span class="sxs-lookup"><span data-stu-id="c6518-125">x</span></span>     |



 

<span data-ttu-id="c6518-126">下列程式碼片段會以概念方式顯示指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="c6518-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="c6518-127">Floor 函數會將傳入的引數轉換成小於 (或等於) 引數的最大整數。</span><span class="sxs-lookup"><span data-stu-id="c6518-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="c6518-128">這會轉換成浮點數，然後將原始值減去從。</span><span class="sxs-lookup"><span data-stu-id="c6518-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="c6518-129">產生的小數值範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="c6518-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="c6518-130">在第1版 \_ 中，允許的寫入遮罩是. y 和 xy (. x 不允許) 。</span><span class="sxs-lookup"><span data-stu-id="c6518-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6518-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6518-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6518-132">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="c6518-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




