---
title: callnz bool-ps
description: 如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。 |callnz bool-ps
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992115"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="10c9a-105">callnz bool-ps</span><span class="sxs-lookup"><span data-stu-id="10c9a-105">callnz bool - ps</span></span>

<span data-ttu-id="10c9a-106">如果不是零，則呼叫。</span><span class="sxs-lookup"><span data-stu-id="10c9a-106">Call if not zero.</span></span> <span data-ttu-id="10c9a-107">對標籤索引所標記的指令執行條件式呼叫。</span><span class="sxs-lookup"><span data-stu-id="10c9a-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c9a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="10c9a-108">Syntax</span></span>



| <span data-ttu-id="10c9a-109">callnz l \# 、 \[ ！ \]B\#</span><span class="sxs-lookup"><span data-stu-id="10c9a-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="10c9a-110">其中：</span><span class="sxs-lookup"><span data-stu-id="10c9a-110">Where:</span></span>

-   <span data-ttu-id="10c9a-111">l \# 是標示要呼叫的副程式開頭的 [標籤（ps）](label---ps.md) 。</span><span class="sxs-lookup"><span data-stu-id="10c9a-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="10c9a-112">\[!\] 這是選擇性的否定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="10c9a-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="10c9a-113">b \# 識別 [常數布林值](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="10c9a-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10c9a-114">備註</span><span class="sxs-lookup"><span data-stu-id="10c9a-114">Remarks</span></span>



| <span data-ttu-id="10c9a-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="10c9a-115">Pixel shader versions</span></span> | <span data-ttu-id="10c9a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="10c9a-116">1\_1</span></span> | <span data-ttu-id="10c9a-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="10c9a-117">1\_2</span></span> | <span data-ttu-id="10c9a-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="10c9a-118">1\_3</span></span> | <span data-ttu-id="10c9a-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="10c9a-119">1\_4</span></span> | <span data-ttu-id="10c9a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10c9a-120">2\_0</span></span> | <span data-ttu-id="10c9a-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="10c9a-121">2\_x</span></span> | <span data-ttu-id="10c9a-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="10c9a-122">2\_sw</span></span> | <span data-ttu-id="10c9a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10c9a-123">3\_0</span></span> | <span data-ttu-id="10c9a-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="10c9a-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="10c9a-125">callnz bool</span><span class="sxs-lookup"><span data-stu-id="10c9a-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="10c9a-126">x</span><span class="sxs-lookup"><span data-stu-id="10c9a-126">x</span></span>    | <span data-ttu-id="10c9a-127">x</span><span class="sxs-lookup"><span data-stu-id="10c9a-127">x</span></span>     | <span data-ttu-id="10c9a-128">x</span><span class="sxs-lookup"><span data-stu-id="10c9a-128">x</span></span>    | <span data-ttu-id="10c9a-129">x</span><span class="sxs-lookup"><span data-stu-id="10c9a-129">x</span></span>     |



 

<span data-ttu-id="10c9a-130">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="10c9a-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="10c9a-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="10c9a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10c9a-132">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="10c9a-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




