---
title: unique 屬性
description: '\ Unique \ 屬性指定唯一指標。'
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- unique 屬性 MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106994961"
---
# <a name="unique-attribute"></a><span data-ttu-id="add51-104">unique 屬性</span><span class="sxs-lookup"><span data-stu-id="add51-104">unique attribute</span></span>

<span data-ttu-id="add51-105">**\[ Unique \]** 屬性指定唯一指標。</span><span class="sxs-lookup"><span data-stu-id="add51-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="add51-106">參數</span><span class="sxs-lookup"><span data-stu-id="add51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add51-107">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="add51-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-108">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="add51-109">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[ unique \]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="add51-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="add51-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="add51-111">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="add51-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-112">指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="add51-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="add51-113">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="add51-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="add51-114">*宣告子和宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="add51-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-115">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="add51-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="add51-116">如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="add51-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="add51-117">宣告子 *清單* 包含一或多個以逗號分隔的宣告子。</span><span class="sxs-lookup"><span data-stu-id="add51-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="add51-118">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="add51-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="add51-119">*struct 或 union-宣告子*</span><span class="sxs-lookup"><span data-stu-id="add51-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-120">指定 MIDL [**結構**](struct.md)[**或等**](union.md)位宣告子。</span><span class="sxs-lookup"><span data-stu-id="add51-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="add51-121">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="add51-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-122">指定套用至結構成員、聯集成員或函數參數的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="add51-123">有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**\_ length**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[ 字串 \]**、 **\[ ignore \]** 和 **\[ coNtext \_ 控制碼 \]**; 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及 union 屬性 **\[ 參數 \_ 類型 \]**。</span><span class="sxs-lookup"><span data-stu-id="add51-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="add51-124">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="add51-125">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="add51-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-126">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="add51-127">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。</span><span class="sxs-lookup"><span data-stu-id="add51-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="add51-128">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="add51-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-129">指定至少一個要套用 **\[ 唯一 \]** 屬性的指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="add51-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="add51-130">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="add51-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="add51-131">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="add51-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-132">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="add51-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="add51-133">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="add51-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-134">包含零或多個適用于指定之參數類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="add51-135">參數屬性可將方向性屬性移 **\[ 入 \]** 和 **\[ 移 \] 出**; [](ptr.md) **\[ \]** **\[ \] 欄位屬性**  **\[ first \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ 是 \] 、** last、length、 **\[ max、 \_ size、size、以及 switch type、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]** **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="add51-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="add51-136">Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="add51-137">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="add51-138">備註</span><span class="sxs-lookup"><span data-stu-id="add51-138">Remarks</span></span>

<span data-ttu-id="add51-139">指標屬性可以套用為類型屬性;作為套用至結構成員、等位成員或參數的欄位屬性;或作為套用至函式傳回型別的函式屬性。</span><span class="sxs-lookup"><span data-stu-id="add51-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="add51-140">指標屬性也可以與 **\[** [**指標 \_ default**](pointer-default.md)關鍵字一起出現 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="add51-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="add51-141">唯一指標具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="add51-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="add51-142">的值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="add51-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="add51-143">從 **Null** 呼叫到非 **null**、從非 null 到 **null**，或從一個非 **null** **值到另** 一個非 null 值時，可能會變更。</span><span class="sxs-lookup"><span data-stu-id="add51-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="add51-144">可以在用戶端上配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="add51-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="add51-145">當唯一指標從 **Null** 變更為非 **Null** 時，從伺服器傳回的資料會寫入至新的儲存體。</span><span class="sxs-lookup"><span data-stu-id="add51-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="add51-146">可以在用戶端上使用現有的記憶體，而不需要配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="add51-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="add51-147">當唯一指標在從一個非 **Null** 值呼叫期間變更為另一個時，會假設指標指向相同型別的資料物件。</span><span class="sxs-lookup"><span data-stu-id="add51-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="add51-148">從伺服器傳回的資料會寫入至在呼叫之前，由 unique 指標的值所指定的現有儲存體。</span><span class="sxs-lookup"><span data-stu-id="add51-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="add51-149">可以是用戶端上的孤立記憶體。</span><span class="sxs-lookup"><span data-stu-id="add51-149">Can orphan memory on the client.</span></span> <span data-ttu-id="add51-150">如果唯一指標在呼叫期間變更為 **Null** ，而且用戶端沒有其他方法可取值儲存體，則不會釋放非 **Null** 唯一指標所參考的記憶體。</span><span class="sxs-lookup"><span data-stu-id="add51-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="add51-151">不會造成別名。</span><span class="sxs-lookup"><span data-stu-id="add51-151">Does not cause aliasing.</span></span> <span data-ttu-id="add51-152">就像參考指標所指向的儲存體一樣，無法從函式中的任何其他名稱連接到由唯一指標所指向的儲存體。</span><span class="sxs-lookup"><span data-stu-id="add51-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="add51-153">存根會呼叫使用者提供的記憶體管理函式 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function) 和 [**midl 使用者可 \_ \_ 自由**](/windows/desktop/Rpc/the-midl-user-free-function) 配置和解除配置唯一指標與其參考的所需記憶體。</span><span class="sxs-lookup"><span data-stu-id="add51-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="add51-154">下列限制適用于唯一的指標：</span><span class="sxs-lookup"><span data-stu-id="add51-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="add51-155">**\[ Unique \]** 屬性無法套用至系結控制碼參數， ([**處理 \_ t**](handle-t.md)) 和內容控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="add51-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="add51-156">**\[ 唯一 \]** 的屬性無法套用至僅 **\[** [](out-idl.md) **\]** 有 **\[ out \]** 方向屬性)  (參數的最上層指標參數。</span><span class="sxs-lookup"><span data-stu-id="add51-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="add51-157">依預設，參數清單中的最上層指標是 **\[** [**ref**](ref.md) **\]** 指標。</span><span class="sxs-lookup"><span data-stu-id="add51-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="add51-158">即使介面指定 **指標 \_ 預設 (唯一)**，也是如此。</span><span class="sxs-lookup"><span data-stu-id="add51-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="add51-159">參數清單中的 **\[ \]** 最上層參數必須指定為唯一的屬性，才能成為唯一的指標。</span><span class="sxs-lookup"><span data-stu-id="add51-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="add51-160">唯一指標不能用來描述陣列或聯集 arm 的大小，因為唯一指標的值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="add51-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="add51-161">這項限制可防止產生 **Null** 值做為陣列大小或聯集 arm 大小的錯誤。</span><span class="sxs-lookup"><span data-stu-id="add51-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="add51-162">範例</span><span class="sxs-lookup"><span data-stu-id="add51-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="add51-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="add51-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add51-164">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="add51-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="add51-165">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="add51-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="add51-166">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="add51-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="add51-167">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="add51-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="add51-168">**回撥**</span><span class="sxs-lookup"><span data-stu-id="add51-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="add51-169">**const**</span><span class="sxs-lookup"><span data-stu-id="add51-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="add51-170">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="add51-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="add51-171">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="add51-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="add51-172">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="add51-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="add51-173">**處理**</span><span class="sxs-lookup"><span data-stu-id="add51-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="add51-174">**處理 \_ t**</span><span class="sxs-lookup"><span data-stu-id="add51-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="add51-175">**忽略**</span><span class="sxs-lookup"><span data-stu-id="add51-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="add51-176">**last \_**</span><span class="sxs-lookup"><span data-stu-id="add51-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="add51-177">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="add51-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="add51-178">**當地**</span><span class="sxs-lookup"><span data-stu-id="add51-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="add51-179">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="add51-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="add51-180">midl \_ 使用者 \_ 配置</span><span class="sxs-lookup"><span data-stu-id="add51-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="add51-181">midl \_ 使用者 \_ 免費</span><span class="sxs-lookup"><span data-stu-id="add51-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="add51-182">**擴展**</span><span class="sxs-lookup"><span data-stu-id="add51-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="add51-183">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="add51-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="add51-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="add51-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="add51-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="add51-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="add51-186">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="add51-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="add51-187">**字串**</span><span class="sxs-lookup"><span data-stu-id="add51-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="add51-188">**結構**</span><span class="sxs-lookup"><span data-stu-id="add51-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="add51-189">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="add51-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="add51-190">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="add51-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="add51-191">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="add51-191">**union**</span></span>](union.md)
</dt> </dl>

 

 