---
title: first_is 屬性
description: '\ First \_ 是 \ 屬性，它會指定要傳送之第一個陣列元素的索引。'
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is 屬性 MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842291"
---
# <a name="first_is-attribute"></a><span data-ttu-id="99b9b-104">first \_ 是屬性</span><span class="sxs-lookup"><span data-stu-id="99b9b-104">first\_is attribute</span></span>

<span data-ttu-id="99b9b-105">\[**第一個 \_ 是屬性，它會** \] 指定要傳送之第一個陣列元素的索引。</span><span class="sxs-lookup"><span data-stu-id="99b9b-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="99b9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="99b9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b9b-107">*有限運算式清單*</span><span class="sxs-lookup"><span data-stu-id="99b9b-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="99b9b-108">指定一或多個 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="99b9b-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="99b9b-109">每個運算式都會評估為整數，表示要傳送之第一個陣列元素的陣列索引。</span><span class="sxs-lookup"><span data-stu-id="99b9b-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="99b9b-110">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="99b9b-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="99b9b-111">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="99b9b-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="99b9b-112">以逗號分隔多個運算式。</span><span class="sxs-lookup"><span data-stu-id="99b9b-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99b9b-113">備註</span><span class="sxs-lookup"><span data-stu-id="99b9b-113">Remarks</span></span>

<span data-ttu-id="99b9b-114">如果 **\[ 第一個 \_ 是 \]** 屬性不存在，或指定的索引為負數，則陣列元素零會是第一個傳送的元素。</span><span class="sxs-lookup"><span data-stu-id="99b9b-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="99b9b-115">**\[ 第 \_ 一個 \]** 屬性也可以協助判斷對應到最後一個的陣列索引值， **\[** [**\_**](last-is.md) **\]** 或 **\[** 當未指定這些屬性時，[**它的長度 \_ 是**](length-is.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="99b9b-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="99b9b-116">這些陣列索引之間的關聯性為：</span><span class="sxs-lookup"><span data-stu-id="99b9b-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="99b9b-117">下列關聯性也必須保留：</span><span class="sxs-lookup"><span data-stu-id="99b9b-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="99b9b-118">當 **\[** [**max \_ 為**](max-is.md)**\] <= 0** 時，下列關聯性必須保持：</span><span class="sxs-lookup"><span data-stu-id="99b9b-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="99b9b-119">**\[ 第一個 \_ 是 \]** 屬性，不能與 **\[** [**字串**](string.md) **\]** 屬性同時使用。</span><span class="sxs-lookup"><span data-stu-id="99b9b-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="99b9b-120">使用具有 **\[ 第一個 \_ \]** 的常數運算式是屬性，就不適合使用屬性。</span><span class="sxs-lookup"><span data-stu-id="99b9b-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="99b9b-121">它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="99b9b-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="99b9b-122">範例</span><span class="sxs-lookup"><span data-stu-id="99b9b-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="99b9b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99b9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b9b-124">欄位 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="99b9b-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="99b9b-125"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="99b9b-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="99b9b-126">**last \_**</span><span class="sxs-lookup"><span data-stu-id="99b9b-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="99b9b-127">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="99b9b-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="99b9b-128">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="99b9b-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="99b9b-129">**最小值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="99b9b-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="99b9b-130">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="99b9b-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="99b9b-131">**字串**</span><span class="sxs-lookup"><span data-stu-id="99b9b-131">**string**</span></span>](string.md)
</dt> </dl>

 

 