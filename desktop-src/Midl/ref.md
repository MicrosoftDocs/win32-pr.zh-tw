---
title: ref 屬性
description: '\ Ref \ 屬性會識別參考指標。 它只會用來表示間接取值層級。'
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- ref 屬性 MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842155"
---
# <a name="ref-attribute"></a><span data-ttu-id="63659-105">ref 屬性</span><span class="sxs-lookup"><span data-stu-id="63659-105">ref attribute</span></span>

<span data-ttu-id="63659-106">**\[ Ref \]** 屬性會識別參考指標。</span><span class="sxs-lookup"><span data-stu-id="63659-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="63659-107">它只會用來表示間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="63659-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="63659-108">參數</span><span class="sxs-lookup"><span data-stu-id="63659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63659-109">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="63659-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-110">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="63659-111">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[ \] ref**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md)和 **\]** **\[** [**忽略**](ignore.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="63659-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="63659-112">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="63659-113">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="63659-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-114">指定 [基底類型](midl-base-types.md)、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="63659-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="63659-115">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="63659-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="63659-116">*標準-宣告子*</span><span class="sxs-lookup"><span data-stu-id="63659-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-117">指定標準 C 宣告子，例如識別碼、指標宣告子或陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="63659-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="63659-118">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="63659-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="63659-119">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="63659-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-120">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="63659-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="63659-121">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="63659-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="63659-122">宣告子 *清單* 包含一或多個以逗號分隔的宣告子。</span><span class="sxs-lookup"><span data-stu-id="63659-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="63659-123">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="63659-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="63659-124">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="63659-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-125">指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="63659-126">有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md) **\]** ; 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="63659-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="63659-127">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="63659-128">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="63659-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-129">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="63659-130">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="63659-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="63659-131">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="63659-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-132">指定至少一個要套用 **\[ ref \]** 屬性的指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="63659-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="63659-133">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="63659-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="63659-134">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="63659-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-135">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="63659-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="63659-136">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="63659-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63659-137">包含零或多個適用于指定之參數類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="63659-138">參數屬性可將方向性屬性 **\[** 移 [**入**](in.md) **\]** 和 **\[** [**移出**](out-idl.md) **\]** ; 欄位屬性 **\[** [**first \_ 是**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md)、 **\]** **\[** [**max、 \_**](max-is.md) **\]** size、 **\[** [**size \_**](size-is.md) **\]** 、以及 **\[** [**switch \_ type**](switch-type.md)、 **\]** 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 usage 屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 和 **\[** [**字串**](string.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="63659-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="63659-139">Usage 屬性 **\[** [**ignore**](ignore.md) **\]** 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="63659-140">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63659-141">備註</span><span class="sxs-lookup"><span data-stu-id="63659-141">Remarks</span></span>

<span data-ttu-id="63659-142">指標屬性可以套用為型別屬性（attribute），做為套用至結構成員、等位成員或參數的欄位屬性。或作為套用至函式傳回型別的函式屬性。</span><span class="sxs-lookup"><span data-stu-id="63659-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="63659-143">指標屬性也可以與 **\[** [**指標 \_ default**](pointer-default.md)關鍵字一起出現 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="63659-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="63659-144">參考指標具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="63659-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="63659-145">一律指向有效的儲存體;絕不會有 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="63659-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="63659-146">參考指標一律可以取值。</span><span class="sxs-lookup"><span data-stu-id="63659-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="63659-147">在呼叫期間永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="63659-147">Never changes during a call.</span></span> <span data-ttu-id="63659-148">參考指標一律會指向用戶端上和呼叫之後的相同儲存體。</span><span class="sxs-lookup"><span data-stu-id="63659-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="63659-149">不會在用戶端上配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="63659-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="63659-150">從伺服器傳回的資料會寫入至呼叫之前，由參考指標的值所指定的現有儲存體。</span><span class="sxs-lookup"><span data-stu-id="63659-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="63659-151">不會造成別名。</span><span class="sxs-lookup"><span data-stu-id="63659-151">Does not cause aliasing.</span></span> <span data-ttu-id="63659-152">參考指標所指向的儲存體無法從函式中的任何其他名稱到達。</span><span class="sxs-lookup"><span data-stu-id="63659-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="63659-153">參考指標不能當做函式所傳回指標的類型使用。</span><span class="sxs-lookup"><span data-stu-id="63659-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="63659-154">如果未指定最上層指標參數的屬性，則會將它視為參考指標。</span><span class="sxs-lookup"><span data-stu-id="63659-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="63659-155">範例</span><span class="sxs-lookup"><span data-stu-id="63659-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="63659-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63659-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63659-157">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="63659-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="63659-158">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="63659-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="63659-159">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="63659-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="63659-160">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="63659-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="63659-161">**回撥**</span><span class="sxs-lookup"><span data-stu-id="63659-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="63659-162">**const**</span><span class="sxs-lookup"><span data-stu-id="63659-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="63659-163">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="63659-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="63659-164">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="63659-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="63659-165">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="63659-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="63659-166">**處理**</span><span class="sxs-lookup"><span data-stu-id="63659-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="63659-167">**忽略**</span><span class="sxs-lookup"><span data-stu-id="63659-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="63659-168">**last \_**</span><span class="sxs-lookup"><span data-stu-id="63659-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="63659-169">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="63659-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="63659-170">**當地**</span><span class="sxs-lookup"><span data-stu-id="63659-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="63659-171">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="63659-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="63659-172">**擴展**</span><span class="sxs-lookup"><span data-stu-id="63659-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="63659-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="63659-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="63659-174">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="63659-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="63659-175">**字串**</span><span class="sxs-lookup"><span data-stu-id="63659-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="63659-176">**結構**</span><span class="sxs-lookup"><span data-stu-id="63659-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="63659-177">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="63659-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="63659-178">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="63659-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="63659-179">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="63659-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="63659-180">**獨特**</span><span class="sxs-lookup"><span data-stu-id="63659-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 