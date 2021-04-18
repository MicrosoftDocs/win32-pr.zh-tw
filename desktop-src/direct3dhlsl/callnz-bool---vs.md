---
title: callnz bool-vs
description: 如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。 |callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992114"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="71c8d-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="71c8d-105">callnz bool - vs</span></span>

<span data-ttu-id="71c8d-106">如果不是零，則呼叫。</span><span class="sxs-lookup"><span data-stu-id="71c8d-106">Call if not zero.</span></span> <span data-ttu-id="71c8d-107">對標籤索引所標記的指令執行條件式呼叫。</span><span class="sxs-lookup"><span data-stu-id="71c8d-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c8d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71c8d-108">Syntax</span></span>



| <span data-ttu-id="71c8d-109">callnz l \# 、 \[ ！ \]B\#</span><span class="sxs-lookup"><span data-stu-id="71c8d-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="71c8d-110">其中：</span><span class="sxs-lookup"><span data-stu-id="71c8d-110">where:</span></span>

-   <span data-ttu-id="71c8d-111">其中 l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。</span><span class="sxs-lookup"><span data-stu-id="71c8d-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="71c8d-112">\[!\] 這是選擇性的布林值 NOT 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="71c8d-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="71c8d-113">b \# 識別 [常數布林值](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="71c8d-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71c8d-114">備註</span><span class="sxs-lookup"><span data-stu-id="71c8d-114">Remarks</span></span>



| <span data-ttu-id="71c8d-115">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="71c8d-115">Vertex shader versions</span></span> | <span data-ttu-id="71c8d-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="71c8d-116">1\_1</span></span> | <span data-ttu-id="71c8d-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="71c8d-117">2\_0</span></span> | <span data-ttu-id="71c8d-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="71c8d-118">2\_x</span></span> | <span data-ttu-id="71c8d-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="71c8d-119">2\_sw</span></span> | <span data-ttu-id="71c8d-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="71c8d-120">3\_0</span></span> | <span data-ttu-id="71c8d-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="71c8d-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="71c8d-122">callnz bool</span><span class="sxs-lookup"><span data-stu-id="71c8d-122">callnz bool</span></span>            |      | <span data-ttu-id="71c8d-123">x</span><span class="sxs-lookup"><span data-stu-id="71c8d-123">x</span></span>    | <span data-ttu-id="71c8d-124">x</span><span class="sxs-lookup"><span data-stu-id="71c8d-124">x</span></span>    | <span data-ttu-id="71c8d-125">x</span><span class="sxs-lookup"><span data-stu-id="71c8d-125">x</span></span>     | <span data-ttu-id="71c8d-126">x</span><span class="sxs-lookup"><span data-stu-id="71c8d-126">x</span></span>    | <span data-ttu-id="71c8d-127">x</span><span class="sxs-lookup"><span data-stu-id="71c8d-127">x</span></span>     |



 

<span data-ttu-id="71c8d-128">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="71c8d-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="71c8d-129">此指令會使用一個頂點著色器指令位置。</span><span class="sxs-lookup"><span data-stu-id="71c8d-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71c8d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="71c8d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71c8d-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="71c8d-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




