---
title: max_is 屬性
description: '\ Max \_ 是 \ 屬性，會指定有效陣列索引的最大值。'
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is 屬性 MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314812"
---
# <a name="max_is-attribute"></a><span data-ttu-id="89756-104">max \_ 為 attribute</span><span class="sxs-lookup"><span data-stu-id="89756-104">max\_is attribute</span></span>

<span data-ttu-id="89756-105">**\[ Max \_ 為 attribute \] 會** 指定有效陣列索引的最大值。</span><span class="sxs-lookup"><span data-stu-id="89756-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="89756-106">參數</span><span class="sxs-lookup"><span data-stu-id="89756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89756-107">*有限運算式清單*</span><span class="sxs-lookup"><span data-stu-id="89756-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="89756-108">指定一或多個 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="89756-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="89756-109">每個運算式都會評估為表示最高有效陣列索引的整數。</span><span class="sxs-lookup"><span data-stu-id="89756-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="89756-110">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="89756-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="89756-111">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="89756-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="89756-112">以逗號分隔多個運算式。</span><span class="sxs-lookup"><span data-stu-id="89756-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89756-113">備註</span><span class="sxs-lookup"><span data-stu-id="89756-113">Remarks</span></span>

<span data-ttu-id="89756-114">Max of 屬性不一定會對應到陣列中的元素數目。 **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="89756-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="89756-115">若為 C 中大小為 *n* 的陣列，其中第一個陣列元素為元素編號零，則有效陣列索引的最大值為 *n*–1。</span><span class="sxs-lookup"><span data-stu-id="89756-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="89756-116">當 **\[ \_ \]** **\[** [**size \_ 為**](size-is.md)attribute 時，max as 屬性不能同時當做 field 屬性使用 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="89756-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="89756-117">雖然使用 **\[ max \_ 是 \]** 具有常數運算式的屬性是合法的，但這麼做並不具效率。</span><span class="sxs-lookup"><span data-stu-id="89756-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="89756-118">例如，使用固定大小陣列：</span><span class="sxs-lookup"><span data-stu-id="89756-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="89756-119">而非：</span><span class="sxs-lookup"><span data-stu-id="89756-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="89756-120">範例</span><span class="sxs-lookup"><span data-stu-id="89756-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="89756-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89756-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89756-122">欄位屬性</span><span class="sxs-lookup"><span data-stu-id="89756-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="89756-123"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="89756-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="89756-124">**最小值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="89756-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="89756-125">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="89756-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 