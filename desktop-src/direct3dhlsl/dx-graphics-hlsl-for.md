---
title: for 陳述式
description: 根據條件運算式的評估，反復執行一系列的語句。
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for 語句 HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092357"
---
# <a name="for-statement"></a><span data-ttu-id="f8780-104">for 陳述式</span><span class="sxs-lookup"><span data-stu-id="f8780-104">for Statement</span></span>

<span data-ttu-id="f8780-105">根據條件運算式的評估，反復執行一系列的語句。</span><span class="sxs-lookup"><span data-stu-id="f8780-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8780-106">\[*屬性* \]針對 (*初始化運算式;條件式反覆運算器*) {*語句區塊*;}</span><span class="sxs-lookup"><span data-stu-id="f8780-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f8780-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8780-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8780-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*</span><span class="sxs-lookup"><span data-stu-id="f8780-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="f8780-109">可控制如何編譯語句的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="f8780-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="f8780-110">未指定屬性時，編譯器會先嘗試發出迴圈的累積版本，如果失敗，或者如果迴圈展開，某些作業會更容易，則會切換回迴圈的展開版本。</span><span class="sxs-lookup"><span data-stu-id="f8780-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="f8780-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f8780-111">Attribute</span></span>             | <span data-ttu-id="f8780-112">描述</span><span class="sxs-lookup"><span data-stu-id="f8780-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8780-113">展開 (x) </span><span class="sxs-lookup"><span data-stu-id="f8780-113">unroll(x)</span></span>             | <span data-ttu-id="f8780-114">展開迴圈，直到它停止執行為止。</span><span class="sxs-lookup"><span data-stu-id="f8780-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="f8780-115">可以選擇性地指定迴圈要執行的最大次數。</span><span class="sxs-lookup"><span data-stu-id="f8780-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="f8780-116">與 **\[ 迴圈 \]** 屬性不相容。</span><span class="sxs-lookup"><span data-stu-id="f8780-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f8780-117">loop</span><span class="sxs-lookup"><span data-stu-id="f8780-117">loop</span></span>                  | <span data-ttu-id="f8780-118">產生使用流程式控制制的程式碼，以執行迴圈的每個反復專案。</span><span class="sxs-lookup"><span data-stu-id="f8780-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="f8780-119">與 **\[ 展開 \]** 屬性不相容。</span><span class="sxs-lookup"><span data-stu-id="f8780-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f8780-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="f8780-120">fastopt</span></span>               | <span data-ttu-id="f8780-121">減少編譯時間，但不會產生較不積極的優化。</span><span class="sxs-lookup"><span data-stu-id="f8780-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="f8780-122">如果您使用這個屬性，編譯器將不會展開迴圈。</span><span class="sxs-lookup"><span data-stu-id="f8780-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="f8780-123">這個屬性只會影響支援 [break](dx-graphics-hlsl-break.md) 指令的著色器模型目標。</span><span class="sxs-lookup"><span data-stu-id="f8780-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="f8780-124">此屬性適用于著色器模型 [與 \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md) （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f8780-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="f8780-125">當編譯器編譯迴圈時，此功能特別適用于 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f8780-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="f8780-126">編譯器預設會模擬迴圈，以評估它是否可以展開它們。</span><span class="sxs-lookup"><span data-stu-id="f8780-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="f8780-127">如果您不想讓編譯器展開迴圈，請使用這個屬性來減少編譯時間。</span><span class="sxs-lookup"><span data-stu-id="f8780-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="f8780-128">允許 \_ uav \_ 條件</span><span class="sxs-lookup"><span data-stu-id="f8780-128">allow\_uav\_condition</span></span> | <span data-ttu-id="f8780-129">允許計算著色器迴圈終止條件以 UAV 讀取為基礎。</span><span class="sxs-lookup"><span data-stu-id="f8780-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="f8780-130">迴圈不能包含同步處理內建函式。</span><span class="sxs-lookup"><span data-stu-id="f8780-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="f8780-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*初始 化*</span><span class="sxs-lookup"><span data-stu-id="f8780-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="f8780-132">迴圈計數器的初始值。</span><span class="sxs-lookup"><span data-stu-id="f8780-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="f8780-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*</span><span class="sxs-lookup"><span data-stu-id="f8780-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="f8780-134">條件 [運算式](dx-graphics-hlsl-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="f8780-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="f8780-135">如果條件運算式評估為 true，則會執行語句區塊。</span><span class="sxs-lookup"><span data-stu-id="f8780-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="f8780-136">當運算式評估為 false 時，迴圈就會結束。</span><span class="sxs-lookup"><span data-stu-id="f8780-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="f8780-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*迭 代*</span><span class="sxs-lookup"><span data-stu-id="f8780-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="f8780-138">更新迴圈計數器的值。</span><span class="sxs-lookup"><span data-stu-id="f8780-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="f8780-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*</span><span class="sxs-lookup"><span data-stu-id="f8780-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="f8780-140">一或多個 [HLSL 語句](dx-graphics-hlsl-statement-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="f8780-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8780-141">備註</span><span class="sxs-lookup"><span data-stu-id="f8780-141">Remarks</span></span>

<span data-ttu-id="f8780-142">**\[ 展開 \]** 和 **\[ loop \]** 屬性是互斥的，並且會在同時指定兩者時產生編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8780-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="f8780-143">如果指定了 **\[ 展開 \]** ，就會忽略 **\[ fastopt \]** 和 **\[ allow \_ uav \_ 條件 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8780-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8780-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8780-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8780-145">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="f8780-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





