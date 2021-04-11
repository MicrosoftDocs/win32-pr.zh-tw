---
title: ptr 屬性
description: '\ Ptr \ 屬性會將指標指定為完整指標。'
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- ptr 屬性 MIDL
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314800"
---
# <a name="ptr-attribute"></a><span data-ttu-id="0ec39-104">ptr 屬性</span><span class="sxs-lookup"><span data-stu-id="0ec39-104">ptr attribute</span></span>

<span data-ttu-id="0ec39-105">**\[ Ptr \]** 屬性會將指標指定為完整指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="0ec39-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ec39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ec39-107">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="0ec39-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-108">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="0ec39-109">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md)或 **\[ \] ptr**; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0ec39-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="0ec39-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-111">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="0ec39-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-112">指定 [基底類型](midl-base-types.md)、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ec39-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="0ec39-113">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="0ec39-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-114">*標準-宣告子*</span><span class="sxs-lookup"><span data-stu-id="0ec39-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-115">指定標準 C 宣告子，例如識別碼、指標宣告子或陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="0ec39-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="0ec39-116">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="0ec39-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-117">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="0ec39-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-118">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="0ec39-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="0ec39-119">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="0ec39-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="0ec39-120">宣告子 *清單* 包含一或多個以逗號分隔的宣告子。</span><span class="sxs-lookup"><span data-stu-id="0ec39-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="0ec39-121">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0ec39-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-122">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="0ec39-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-123">指定套用至結構或等位成員或函數參數的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="0ec39-124">有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[ ptr \]**; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0ec39-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="0ec39-125">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-126">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="0ec39-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-127">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="0ec39-128">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0ec39-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-129">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="0ec39-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-130">指定至少一個要套用 **\[ ptr \]** 屬性的指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="0ec39-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="0ec39-131">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="0ec39-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-132">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="0ec39-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-133">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec39-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0ec39-134">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="0ec39-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0ec39-135">包含零或多個適用于指定之參數類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="0ec39-136">參數 [**屬性可以採用和**](in.md)[**輸出**](out-idl.md)方向屬性;欄位屬性 [**first \_ 是**](first-is.md)、 [**last \_**](last-is.md)、length、 [**max \_**](length-is.md)、 [**max、 \_**](max-is.md)size、and [**switch \_ type**](switch-type.md)、指標屬性 [**ref**](ref.md)、 [**unique**](unique.md)或 **\[ ptr \]**; 以及 usage 屬性 [**內容 \_ 控制碼**](context-handle.md)和 [**字串**](string.md)。 [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="0ec39-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="0ec39-137">Usage 屬性 [**ignore**](ignore.md) 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="0ec39-138">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec39-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ec39-139">備註</span><span class="sxs-lookup"><span data-stu-id="0ec39-139">Remarks</span></span>

<span data-ttu-id="0ec39-140">**\[ Ptr \]** 屬性指定的完整指標會使用 C 語言指標的完整功能。</span><span class="sxs-lookup"><span data-stu-id="0ec39-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="0ec39-141">完整指標的值可以是 **null** ，而且可以在呼叫期間從 **null** 變更為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ec39-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="0ec39-142">具有完整指標的儲存區可由應用程式中的其他名稱所指向，以支援別名和迴圈。</span><span class="sxs-lookup"><span data-stu-id="0ec39-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="0ec39-143">這項功能在遠端程序呼叫中需要更多的額外負荷來識別指標所參考的資料、判斷值是否為 **Null**，以及探索兩個指標是否指向相同的資料。</span><span class="sxs-lookup"><span data-stu-id="0ec39-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="0ec39-144">使用的完整指標：</span><span class="sxs-lookup"><span data-stu-id="0ec39-144">Use full pointers for:</span></span>

-   <span data-ttu-id="0ec39-145">遠端傳回值。</span><span class="sxs-lookup"><span data-stu-id="0ec39-145">Remote return values.</span></span>
-   <span data-ttu-id="0ec39-146">當輸出參數的大小未知時，即為雙指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="0ec39-147">**Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-147">**NULL** pointers.</span></span>

<span data-ttu-id="0ec39-148">完整 (和唯一的) 指標不能用來描述陣列或等位的大小，因為這些指標可以有 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="0ec39-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="0ec39-149">MIDL 的這項限制可防止在將 **Null** 值當做大小使用時可能產生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0ec39-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="0ec39-150">參考和唯一指標會假設為沒有資料的別名。</span><span class="sxs-lookup"><span data-stu-id="0ec39-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="0ec39-151">從唯一或參考指標開始，而且只在下列情況下，只包含唯一或參考指標的導向圖形都不會包含 reconvergence 和迴圈。</span><span class="sxs-lookup"><span data-stu-id="0ec39-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="0ec39-152">為了避免別名，所有指標值都應該從相同指標類別的輸入指標取得。</span><span class="sxs-lookup"><span data-stu-id="0ec39-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="0ec39-153">如果有一個以上的指標指向相同的記憶體位置，則所有這類指標都必須是完整的指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="0ec39-154">在某些情況下，可以混合完整和唯一的指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="0ec39-155">只要指派不違反變更唯一指標值的限制，就可以將唯一指標的值指派給完整指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="0ec39-156">但是，當您將唯一指標指派為完整指標的值時，可能會導致別名。</span><span class="sxs-lookup"><span data-stu-id="0ec39-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="0ec39-157">混合完整和唯一指標可能會導致別名，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="0ec39-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="0ec39-158">雖然 "t >left" 和 "t->right" 指向唯一的記憶體位置，但 "t->左 >.pdata" 和 "t >右 >.pdata" 都有別名。</span><span class="sxs-lookup"><span data-stu-id="0ec39-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="0ec39-159">基於這個理由，別名支援演算法必須遵循所有指標 (包括唯一和參考指標，) 最後可能會到達完整指標。</span><span class="sxs-lookup"><span data-stu-id="0ec39-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="0ec39-160">範例</span><span class="sxs-lookup"><span data-stu-id="0ec39-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="0ec39-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ec39-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec39-162">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="0ec39-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="0ec39-163">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="0ec39-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="0ec39-164">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="0ec39-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ec39-165">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="0ec39-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="0ec39-166">**回撥**</span><span class="sxs-lookup"><span data-stu-id="0ec39-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="0ec39-167">**const**</span><span class="sxs-lookup"><span data-stu-id="0ec39-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0ec39-168">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0ec39-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="0ec39-169">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="0ec39-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="0ec39-170">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="0ec39-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="0ec39-171">**處理**</span><span class="sxs-lookup"><span data-stu-id="0ec39-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="0ec39-172"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="0ec39-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0ec39-173">**忽略**</span><span class="sxs-lookup"><span data-stu-id="0ec39-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="0ec39-174">**last \_**</span><span class="sxs-lookup"><span data-stu-id="0ec39-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="0ec39-175">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="0ec39-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="0ec39-176">**當地**</span><span class="sxs-lookup"><span data-stu-id="0ec39-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="0ec39-177">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="0ec39-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="0ec39-178">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="0ec39-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="0ec39-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="0ec39-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0ec39-180">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="0ec39-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="0ec39-181">**字串**</span><span class="sxs-lookup"><span data-stu-id="0ec39-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="0ec39-182">**結構**</span><span class="sxs-lookup"><span data-stu-id="0ec39-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="0ec39-183">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="0ec39-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="0ec39-184">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="0ec39-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="0ec39-185">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="0ec39-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="0ec39-186">**獨特**</span><span class="sxs-lookup"><span data-stu-id="0ec39-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 