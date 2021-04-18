---
title: last_is 屬性
description: Field 屬性 \ last \_ 是 \ 指定要傳送之最後一個陣列元素的索引。 當指定的索引為零或負數時，不會傳送任何陣列元素。
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is 屬性 MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507907"
---
# <a name="last_is-attribute"></a><span data-ttu-id="ad6fd-105">last \_ 是屬性</span><span class="sxs-lookup"><span data-stu-id="ad6fd-105">last\_is attribute</span></span>

<span data-ttu-id="ad6fd-106">Field 屬性 **\[ last \_ 是 \]** 指定要傳送之最後一個陣列元素的索引。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="ad6fd-107">當指定的索引為零或負數時，不會傳送任何陣列元素。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="ad6fd-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad6fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad6fd-109">*有限運算式清單*</span><span class="sxs-lookup"><span data-stu-id="ad6fd-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ad6fd-110">指定一或多個 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="ad6fd-111">每個運算式都會評估為整數，表示要傳送之最後一個陣列元素的陣列索引。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="ad6fd-112">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="ad6fd-113">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="ad6fd-114">以逗號分隔多個運算式。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad6fd-115">備註</span><span class="sxs-lookup"><span data-stu-id="ad6fd-115">Remarks</span></span>

<span data-ttu-id="ad6fd-116">**\[ 最後一個 \_ 屬性 \] 會** 決定 **\[** [**\_**](length-is.md) **\]** 當未指定 **\[ 長度 \_ \]** 時，對應至長度的陣列索引值為屬性。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="ad6fd-117">這些陣列索引之間的關聯性如下： length = last-first + 1。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="ad6fd-118">如果第一個指定的陣列索引值大於 **\[** [**\_**](first-is.md) **\]** **\[ \_ \] last** 所指定的值，則會傳送零個元素。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="ad6fd-119">**\[ 最後一個 \_ 是 \]** 屬性，因為 **\[** [**長度 \_ 是**](length-is.md) **\]** 屬性或 **\[** [**字串**](string.md)屬性，所以不能同時做為欄位屬性使用 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="ad6fd-120">使用具有 last 的常數運算式 **\[ \_ 是 \]** 屬性，就不適合使用屬性。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="ad6fd-121">它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="ad6fd-122">當 max 指定的值 **\[** [**\_**](max-is.md) **\]** 等於或大於零時，下列關聯性必須成立： 0 <= last \_ <= max \_ 是。</span><span class="sxs-lookup"><span data-stu-id="ad6fd-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="ad6fd-123">範例</span><span class="sxs-lookup"><span data-stu-id="ad6fd-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="ad6fd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad6fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6fd-125">欄位屬性</span><span class="sxs-lookup"><span data-stu-id="ad6fd-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="ad6fd-126">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="ad6fd-127"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="ad6fd-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ad6fd-128">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="ad6fd-129">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="ad6fd-130">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 