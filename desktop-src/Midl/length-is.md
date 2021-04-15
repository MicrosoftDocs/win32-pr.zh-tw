---
title: length_is 屬性
description: '\ Length \_ 是 \ 屬性，可指定要傳送的陣列元素數目。 您必須指定非負數值。'
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is 屬性 MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463108"
---
# <a name="length_is-attribute"></a><span data-ttu-id="ce11c-105">長度 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="ce11c-105">length\_is attribute</span></span>

<span data-ttu-id="ce11c-106">[ **\[ 長度 \_ ] \] 是**[屬性] 指定要傳送的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="ce11c-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="ce11c-107">您必須指定非負數值。</span><span class="sxs-lookup"><span data-stu-id="ce11c-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="ce11c-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce11c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce11c-109">*有限運算式清單*</span><span class="sxs-lookup"><span data-stu-id="ce11c-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ce11c-110">指定一或多個 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="ce11c-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="ce11c-111">每個運算式都會評估為整數，表示要傳送的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="ce11c-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="ce11c-112">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="ce11c-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="ce11c-113">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="ce11c-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="ce11c-114">以逗號分隔多個運算式。</span><span class="sxs-lookup"><span data-stu-id="ce11c-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce11c-115">備註</span><span class="sxs-lookup"><span data-stu-id="ce11c-115">Remarks</span></span>

<span data-ttu-id="ce11c-116">[ **\[ 長度 \_ ] \] 是**[屬性]，會決定 **\[** [**\_**](last-is.md) **\]** 當未指定 **\[ \_ \] last** 時，對應到 last 的陣列索引值是屬性。</span><span class="sxs-lookup"><span data-stu-id="ce11c-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="ce11c-117">這些陣列索引之間的關聯性如下： length = last-first + 1。</span><span class="sxs-lookup"><span data-stu-id="ce11c-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="ce11c-118">**\[ Length \_ 是 \]** attribute 無法與 **\[** [**最後一個 \_ 是**](last-is.md) **\]** 屬性或 **\[** [**字串**](string.md) **\]** 屬性同時使用。</span><span class="sxs-lookup"><span data-stu-id="ce11c-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="ce11c-119">若要定義 **\[ 長度 \_ 為 \]** 或 last 的計數位符串為 **\[** [**\_**](last-is.md) **\]** 屬性，請使用不含 **\[** [**字串**](string.md)屬性的字元陣列或指標 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="ce11c-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="ce11c-120">使用 **\[ 長度 \_ 為 \]** attribute 的常數運算式是不適當的屬性使用方式。</span><span class="sxs-lookup"><span data-stu-id="ce11c-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="ce11c-121">它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="ce11c-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="ce11c-122">您可以使用 [ **\[** [**大小 \_**](size-is.md) ] **\]** 和 [長度] **\[ \_ 都 \] 是** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ce11c-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="ce11c-123">當您這樣做時，[大小] 屬性 **\[ \_ 會 \]** 控制配置給資料的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="ce11c-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="ce11c-124">[ **\[ 長度 \_ ] \] 是**[屬性] 指定要傳輸的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ce11c-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="ce11c-125">大小所指定的記憶體數量 **\[ \_ 是 \]** ，而且 **\[ 長度 \_ 是 \]** 屬性不需要相同的。</span><span class="sxs-lookup"><span data-stu-id="ce11c-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="ce11c-126">比方說，您的用戶端可能會將 **\[ in**、 **out \]** 參數傳遞至伺服器，並指定 **\[ 大小 \_ 為 \]** 的大型記憶體配置，即使它指定要以長度傳遞的少量資料元素 **\[ \_ 也是 \]** 一樣。</span><span class="sxs-lookup"><span data-stu-id="ce11c-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="ce11c-127">這可讓伺服器在陣列中填入超過其所接收的資料，然後再傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="ce11c-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="ce11c-128">一般情況下，同時指定 **\[** [**size \_**](size-is.md) **\]** 和 **\[ length \_ \]** 在 **\[** [**in**](in.md) **\]** 或 **\[** [**out**](out-idl.md) **\]** 參數中並不實用。</span><span class="sxs-lookup"><span data-stu-id="ce11c-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="ce11c-129">在這兩種情況下， **\[ 大小 \_ 都會 \]** 控制記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="ce11c-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="ce11c-130">您的應用程式可以使用 **\[ 大小 \_ ， \]** 因為配置的陣列元素比 (的) **\[ 長度 \_ 所 \]** 指定的更多。</span><span class="sxs-lookup"><span data-stu-id="ce11c-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="ce11c-131">不過，這樣做會沒有效率。</span><span class="sxs-lookup"><span data-stu-id="ce11c-131">However, this would be inefficient.</span></span> <span data-ttu-id="ce11c-132">為 **\[ \_ 大小 \]** 指定相同的值，且 **\[ 長度 \_ 為 \]**，也會沒有效率。</span><span class="sxs-lookup"><span data-stu-id="ce11c-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="ce11c-133">因為它會在參數封送處理期間產生額外的負擔。</span><span class="sxs-lookup"><span data-stu-id="ce11c-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="ce11c-134">當 **\[ \_ size \]** 的值和 **\[ \_ length \]** 永遠相同時，請省略 **\[ length \_ \] 為** attribute。</span><span class="sxs-lookup"><span data-stu-id="ce11c-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="ce11c-135">範例</span><span class="sxs-lookup"><span data-stu-id="ce11c-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="ce11c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce11c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce11c-137">欄位屬性</span><span class="sxs-lookup"><span data-stu-id="ce11c-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="ce11c-138">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="ce11c-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="ce11c-139"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="ce11c-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ce11c-140">**last \_**</span><span class="sxs-lookup"><span data-stu-id="ce11c-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="ce11c-141">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ce11c-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="ce11c-142">**最小值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ce11c-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="ce11c-143">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ce11c-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="ce11c-144">**字串**</span><span class="sxs-lookup"><span data-stu-id="ce11c-144">**string**</span></span>](string.md)
</dt> </dl>

 

 