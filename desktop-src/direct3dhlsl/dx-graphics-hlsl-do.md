---
title: 'do 語句 (Ocidl) '
description: 持續執行一連串的語句，直到條件運算式失敗為止。
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do 語句 HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118783"
---
# <a name="do-statement"></a><span data-ttu-id="3ba8a-104">do 語句</span><span class="sxs-lookup"><span data-stu-id="3ba8a-104">do Statement</span></span>

<span data-ttu-id="3ba8a-105">持續執行一連串的語句，直到條件運算式失敗為止。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="3ba8a-106">\[*屬性* \] (*條件* 式 ) 時，請進行 {*語句區塊*;}</span><span class="sxs-lookup"><span data-stu-id="3ba8a-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="3ba8a-107">參數</span><span class="sxs-lookup"><span data-stu-id="3ba8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba8a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*</span><span class="sxs-lookup"><span data-stu-id="3ba8a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="3ba8a-109">可控制如何編譯語句的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="3ba8a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3ba8a-110">Attribute</span></span> | <span data-ttu-id="3ba8a-111">描述</span><span class="sxs-lookup"><span data-stu-id="3ba8a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba8a-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="3ba8a-112">fastopt</span></span>   | <span data-ttu-id="3ba8a-113">減少編譯時間，但不會產生較不積極的優化。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="3ba8a-114">如果您使用這個屬性，編譯器將不會展開迴圈。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="3ba8a-115">這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="3ba8a-116">此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="3ba8a-117">當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="3ba8a-118">編譯器預設會模擬迴圈，以評估它是否可以展開它們。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="3ba8a-119">如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3ba8a-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*</span><span class="sxs-lookup"><span data-stu-id="3ba8a-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="3ba8a-121">一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ba8a-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*</span><span class="sxs-lookup"><span data-stu-id="3ba8a-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="3ba8a-123">條件 [運算式](dx-graphics-hlsl-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="3ba8a-124">語句區塊會在評估運算式之前執行。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="3ba8a-125">當運算式評估為 false 時，就會結束迴圈。</span><span class="sxs-lookup"><span data-stu-id="3ba8a-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ba8a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ba8a-126">Requirements</span></span>



| <span data-ttu-id="3ba8a-127">需求</span><span class="sxs-lookup"><span data-stu-id="3ba8a-127">Requirement</span></span> | <span data-ttu-id="3ba8a-128">值</span><span class="sxs-lookup"><span data-stu-id="3ba8a-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba8a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3ba8a-129">Header</span></span><br/> | <dl> <span data-ttu-id="3ba8a-130"><dt>Ocidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba8a-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba8a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ba8a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba8a-132">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="3ba8a-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





