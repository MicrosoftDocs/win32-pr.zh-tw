---
title: while 陳述式
description: 在條件運算式失敗之前執行語句區塊。
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while 語句 HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826671"
---
# <a name="while-statement"></a><span data-ttu-id="4a645-104">while 陳述式</span><span class="sxs-lookup"><span data-stu-id="4a645-104">while Statement</span></span>

<span data-ttu-id="4a645-105">在條件運算式失敗之前執行語句區塊。</span><span class="sxs-lookup"><span data-stu-id="4a645-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="4a645-106">\[*屬性* \]while (*條件* 式 ) {*語句區塊*;}</span><span class="sxs-lookup"><span data-stu-id="4a645-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="4a645-107">參數</span><span class="sxs-lookup"><span data-stu-id="4a645-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a645-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*</span><span class="sxs-lookup"><span data-stu-id="4a645-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="4a645-109">可控制如何編譯語句的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="4a645-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="4a645-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4a645-110">Attribute</span></span>             | <span data-ttu-id="4a645-111">描述</span><span class="sxs-lookup"><span data-stu-id="4a645-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a645-112">展開 (x) </span><span class="sxs-lookup"><span data-stu-id="4a645-112">unroll(x)</span></span>             | <span data-ttu-id="4a645-113">展開迴圈，直到它停止執行為止。</span><span class="sxs-lookup"><span data-stu-id="4a645-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="4a645-114">您可以選擇性地指定迴圈可執行檔最大次數。</span><span class="sxs-lookup"><span data-stu-id="4a645-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4a645-115">loop</span><span class="sxs-lookup"><span data-stu-id="4a645-115">loop</span></span>                  | <span data-ttu-id="4a645-116">在編譯的著色器中使用流程式控制制語句;請勿展開迴圈。</span><span class="sxs-lookup"><span data-stu-id="4a645-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4a645-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="4a645-117">fastopt</span></span>               | <span data-ttu-id="4a645-118">減少編譯時間，但不會產生較不積極的優化。</span><span class="sxs-lookup"><span data-stu-id="4a645-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="4a645-119">如果您使用這個屬性，編譯器將不會展開迴圈。</span><span class="sxs-lookup"><span data-stu-id="4a645-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="4a645-120">這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。</span><span class="sxs-lookup"><span data-stu-id="4a645-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="4a645-121">此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4a645-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="4a645-122">當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4a645-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="4a645-123">編譯器預設會模擬迴圈，以評估它是否可以展開它們。</span><span class="sxs-lookup"><span data-stu-id="4a645-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="4a645-124">如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。</span><span class="sxs-lookup"><span data-stu-id="4a645-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="4a645-125">允許 \_ uav \_ 條件</span><span class="sxs-lookup"><span data-stu-id="4a645-125">allow\_uav\_condition</span></span> | <span data-ttu-id="4a645-126">允許計算著色器迴圈終止條件以 UAV 讀取為基礎。</span><span class="sxs-lookup"><span data-stu-id="4a645-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="4a645-127">迴圈不能包含同步處理內建函式。</span><span class="sxs-lookup"><span data-stu-id="4a645-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="4a645-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*</span><span class="sxs-lookup"><span data-stu-id="4a645-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="4a645-129">條件 [運算式](dx-graphics-hlsl-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="4a645-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="4a645-130">如果運算式評估為 true，則會執行語句區塊。</span><span class="sxs-lookup"><span data-stu-id="4a645-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="4a645-131">當運算式評估為 false 時，迴圈就會結束。</span><span class="sxs-lookup"><span data-stu-id="4a645-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="4a645-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*</span><span class="sxs-lookup"><span data-stu-id="4a645-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="4a645-133">一或多個 [語句](dx-graphics-hlsl-statement-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="4a645-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4a645-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a645-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a645-135">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="4a645-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





