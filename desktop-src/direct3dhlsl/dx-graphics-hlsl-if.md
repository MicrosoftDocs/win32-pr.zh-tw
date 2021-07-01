---
title: if 陳述式
description: 根據條件運算式的評估，有條件地執行一連串的語句。
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if 語句 HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118953"
---
# <a name="if-statement"></a><span data-ttu-id="166a3-104">if 陳述式</span><span class="sxs-lookup"><span data-stu-id="166a3-104">if Statement</span></span>

<span data-ttu-id="166a3-105">根據條件運算式的評估，有條件地執行一連串的語句。</span><span class="sxs-lookup"><span data-stu-id="166a3-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="166a3-106">\[*屬性* \]如果 (*條件* 式 ) {*語句區塊*;}</span><span class="sxs-lookup"><span data-stu-id="166a3-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="166a3-107">參數</span><span class="sxs-lookup"><span data-stu-id="166a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166a3-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*屬性*</span><span class="sxs-lookup"><span data-stu-id="166a3-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="166a3-109">可控制如何編譯語句的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="166a3-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="166a3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="166a3-110">Attribute</span></span></th>
<th><span data-ttu-id="166a3-111">描述</span><span class="sxs-lookup"><span data-stu-id="166a3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="166a3-112">分支</span><span class="sxs-lookup"><span data-stu-id="166a3-112">branch</span></span></td>
<td><span data-ttu-id="166a3-113">根據指定的條件，只評估 if 語句的其中一個端。</span><span class="sxs-lookup"><span data-stu-id="166a3-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="166a3-114">當您使用 <a href="dx-graphics-hlsl-sm2.md">著色器模型</a> 2.X 或 <a href="dx-graphics-hlsl-sm3.md">著色器模型 3.0</a>時，每次使用動態分支都會耗用資源。</span><span class="sxs-lookup"><span data-stu-id="166a3-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="166a3-115">因此，如果您在以這些設定檔為目標時，過度使用動態分支，您可能會收到編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="166a3-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="166a3-116">扁平化</span><span class="sxs-lookup"><span data-stu-id="166a3-116">flatten</span></span></td>
<td><span data-ttu-id="166a3-117">評估 if 語句的兩邊，並在兩個結果值之間選擇。</span><span class="sxs-lookup"><span data-stu-id="166a3-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="166a3-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*條件*</span><span class="sxs-lookup"><span data-stu-id="166a3-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="166a3-119">條件 [運算式](dx-graphics-hlsl-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="166a3-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="166a3-120">運算式會進行評估，若為 true，則會執行語句區塊。</span><span class="sxs-lookup"><span data-stu-id="166a3-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*語句區塊*</span><span class="sxs-lookup"><span data-stu-id="166a3-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="166a3-122">一或多個 [HLSL 語句](dx-graphics-hlsl-statement-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="166a3-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="166a3-123">備註</span><span class="sxs-lookup"><span data-stu-id="166a3-123">Remarks</span></span>

<span data-ttu-id="166a3-124">當編譯器使用分支方法來編譯 if 語句時，它會產生程式碼，根據指定的條件，只會評估 if 語句的一端。</span><span class="sxs-lookup"><span data-stu-id="166a3-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="166a3-125">例如，在 if 語句中：</span><span class="sxs-lookup"><span data-stu-id="166a3-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="166a3-126">**If** 語句具有隱含的 else 區塊，相當於 x = x。</span><span class="sxs-lookup"><span data-stu-id="166a3-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="166a3-127">因為我們已告知編譯器將分支方法與先前的分支屬性搭配使用，所以已編譯的程式碼將會評估 x，並只執行應該執行的端;如果 x 為零，則會執行 **else** 端，如果不是零，則會執行 **then** 端。</span><span class="sxs-lookup"><span data-stu-id="166a3-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="166a3-128">相反地，如果使用簡 **維屬性，則編譯的程式** 代碼將會評估 **if** 語句的兩邊，並使用 x 的原始值，在兩個結果值之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="166a3-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="166a3-129">以下是簡維屬性使用方式的範例：</span><span class="sxs-lookup"><span data-stu-id="166a3-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="166a3-130">在某些情況下，使用分支或壓平合併屬性可能會產生編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="166a3-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="166a3-131">如果 if 語句的任一邊包含漸層函式（例如 [**tex2D**](dx-graphics-hlsl-tex2d.md)），分支屬性可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="166a3-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="166a3-132">如果 if 語句的任一邊包含 stream append 語句或任何其他具有副作用的語句，則簡維屬性可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="166a3-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="166a3-133">**If** 語句也可以使用選擇性的 else 區塊。</span><span class="sxs-lookup"><span data-stu-id="166a3-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="166a3-134">如果 **if** 運算式為 true，則會處理與 if 語句相關聯之語句區塊中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="166a3-135">否則，會處理與選用的 else 區塊相關聯的語句區塊。</span><span class="sxs-lookup"><span data-stu-id="166a3-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="166a3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="166a3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166a3-137">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="166a3-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





