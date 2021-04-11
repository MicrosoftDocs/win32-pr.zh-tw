---
title: size_is 屬性
description: 使用 \ size \_ 為 \ 屬性來指定記憶體的大小、元素中配置給大小指標的指標、調整大小指標大小的指標，以及單一或多維度陣列。
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is 屬性 MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681769"
---
# <a name="size_is-attribute"></a><span data-ttu-id="f4ba0-104">大小 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="f4ba0-104">size\_is attribute</span></span>

<span data-ttu-id="f4ba0-105">使用 \[ **size \_ 為** \] attribute 來指定記憶體大小、元素中配置給調整大小指標的指標、調整大小指標大小的指標，以及單一或多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="f4ba0-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4ba0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ba0-107">*有限運算式清單*</span><span class="sxs-lookup"><span data-stu-id="f4ba0-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ba0-108">指定一或多個 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="f4ba0-109">每個運算式都會評估為非負整數，代表配置給大小指標或陣列的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="f4ba0-110">如果是陣列，則會指定單一運算式，代表該陣列第一個維度的配置大小（以元素為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="f4ba0-111">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="f4ba0-112">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="f4ba0-113">使用逗號作為隱含參數的預留位置，或分隔多個運算式。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4ba0-114">備註</span><span class="sxs-lookup"><span data-stu-id="f4ba0-114">Remarks</span></span>

<span data-ttu-id="f4ba0-115">如果您使用 [ \[ **大小 \_ 為**] \] 屬性來配置多維度陣列的記憶體，而且您正在使用陣列 \[ \] 標記法，請記住，只有多維陣列的第一個維度可在執行時間以動態方式判斷。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="f4ba0-116">其他維度必須以靜態方式指定。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="f4ba0-117">如需使用 \[ **大小 \_ 為** \] 具有多個指標層級之屬性的詳細資訊，讓伺服器能夠將動態大小的資料陣列傳回給用戶端（如範例 Proc7 所示），請參閱 [多層級的指標](/windows/desktop/Rpc/multiple-levels-of-pointers)。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="f4ba0-118">您可以使用 [ \[ **大小 \_** ] \] 或 [**[ \_ 最大值**](max-is.md)] (，但不能同時使用相同的屬性清單) 來指定在執行時間決定其上限的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="f4ba0-119">但是請注意， \[ **size \_ 是** \] attribute 無法用於固定的陣列維度。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="f4ba0-120">\[ **Max \_ 是** \] 屬性指定最大有效陣列索引。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="f4ba0-121">因此，指定 \[ size \_ 是 (n) \] 相當於指定 \[ max \_ (n-1) \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="f4ba0-122">\[ [**In**](in.md) \] 或 \[ in、 [**out**](out-idl.md) \] 符合標準的陣列參數（包含 \[ [**字串**](string.md) \] 屬性）不需要 \[ **大小 \_ 為** \] attribute 或 \[ [**max \_**](max-is.md) \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="f4ba0-123">在此情況下，配置的大小取決於輸入字串的 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="f4ba0-124">具有字串屬性的所有其他符合標準的陣列都 \[ \] 必須是屬性的 \[ **大小 \_** \] 或 \[ **最大 \_** 值 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="f4ba0-125">雖然使用 \[ **size \_ 是** 具有常數的屬性是合法的 \] ，但這麼做並不具效率。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="f4ba0-126">例如，使用固定大小陣列：</span><span class="sxs-lookup"><span data-stu-id="f4ba0-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="f4ba0-127">而非：</span><span class="sxs-lookup"><span data-stu-id="f4ba0-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="f4ba0-128">您可以使用 [ \[ **大小 \_** ] \] 和 [長度] \[ [**\_ 都是**](length-is.md) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="f4ba0-129">當您這樣做時，[ \[ **大小] 屬性 \_ 會** 控制配置給 \] 資料的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="f4ba0-130">[ \[ **長度] \_ 是**[ \] 屬性] 指定要傳輸的元素數目。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="f4ba0-131">大小所指定的記憶體數量 \[ **\_ 是** \] ，而且 \[ **長度 \_ 是** \] 屬性不需要相同的。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="f4ba0-132">比方說，您的用戶端可能會將 \[ in、out \] 參數傳遞至伺服器，並指定大小為的大型記憶體配置 \[ **\_** \] ，即使它指定要以長度傳遞的少量資料元素 \[ **\_ 也是** 一樣 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="f4ba0-133">這可讓伺服器在陣列中填入超過其所接收的資料，然後再傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="f4ba0-134">一般情況下，同時指定 \[ **size \_** \] 和 \[ [**length \_**](length-is.md)在 \] \[ in \] 或 \[ out \] 參數中並不實用。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="f4ba0-135">在這兩種情況下， \[ **大小 \_ 都會** \] 控制記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="f4ba0-136">您的應用程式可以使用 \[ **大小 \_ ，** \] 因為配置的陣列元素比 (的 \[) **長度 \_ 所** 指定的更多 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="f4ba0-137">不過，這樣做會沒有效率。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-137">However, this would be inefficient.</span></span> <span data-ttu-id="f4ba0-138">為大小指定相同的值 \[ **\_** \] ，且 \[ **長度 \_ 為**，也會沒有效率 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="f4ba0-139">它會在參數封送處理期間產生額外的負荷。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="f4ba0-140">如果 size 的值 \[ **\_ 為** \] 且 \[ **length \_** \] 永遠相同，請省略 \[ **length \_ 為** \] attribute。</span><span class="sxs-lookup"><span data-stu-id="f4ba0-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="f4ba0-141">範例</span><span class="sxs-lookup"><span data-stu-id="f4ba0-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="f4ba0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4ba0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ba0-143">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-144">欄位屬性</span><span class="sxs-lookup"><span data-stu-id="f4ba0-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="f4ba0-145">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-146"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="f4ba0-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-147">**在**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-148">**last \_**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-149">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-150">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-151">**最小值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-152">**擴展**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f4ba0-153">**字串**</span><span class="sxs-lookup"><span data-stu-id="f4ba0-153">**string**</span></span>](string.md)
</dt> </dl>

 

 