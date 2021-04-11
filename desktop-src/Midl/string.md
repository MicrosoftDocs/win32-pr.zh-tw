---
title: string 屬性
description: '\ 字串 \ 屬性工作表示一維 char、wchar \_ t、byte (或對等的) 陣列，或對這類陣列的指標必須視為字串。'
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- 字串屬性 MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933189"
---
# <a name="string-attribute"></a><span data-ttu-id="274fd-104">string 屬性</span><span class="sxs-lookup"><span data-stu-id="274fd-104">string attribute</span></span>

<span data-ttu-id="274fd-105">**\[ 字串 \]** 屬性工作表示一維 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**byte**](byte.md) (或對等的) 陣列，或是這類陣列的指標必須視為字串。</span><span class="sxs-lookup"><span data-stu-id="274fd-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="274fd-106">字串也可以是陣列 (或陣列的指標) ，其欄位全都是 **byte** 類型的結構。</span><span class="sxs-lookup"><span data-stu-id="274fd-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="274fd-107">參數</span><span class="sxs-lookup"><span data-stu-id="274fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="274fd-108">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="274fd-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-109">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="274fd-110">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[ 字串 \]** 和 **\[** [**略**](ignore.md)過 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="274fd-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="274fd-111">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-112">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="274fd-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-113">指定 [基底類型](midl-base-types.md)、 [**結構**](struct.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="274fd-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="274fd-114">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="274fd-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-115">*標準-宣告子*</span><span class="sxs-lookup"><span data-stu-id="274fd-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-116">指定標準 C 宣告子，例如識別碼、指標宣告子或陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="274fd-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="274fd-117">如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="274fd-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="274fd-118">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="274fd-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-119">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="274fd-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="274fd-120">如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="274fd-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="274fd-121">宣告子 *清單* 包含一或多個以逗號分隔的宣告子。</span><span class="sxs-lookup"><span data-stu-id="274fd-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="274fd-122">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="274fd-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-123">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="274fd-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-124">指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="274fd-125">這兩個有效的欄位屬性是 **\[** [**最大 \_**](max-is.md)值， **\]** 且 **\[** [**大小 \_ 為**](size-is.md) **\]** ; 使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**、指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[ unique \]** 或 **\[** [**ptr**](ptr.md) **\]** ，以及 union 屬性 **\[ 參數 \_ 類型 \]**。</span><span class="sxs-lookup"><span data-stu-id="274fd-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="274fd-126">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-127">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="274fd-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-128">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="274fd-129">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。</span><span class="sxs-lookup"><span data-stu-id="274fd-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-130">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="274fd-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-131">指定套用 **\[ 字串 \]** 屬性的選擇性指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="274fd-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="274fd-132">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="274fd-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="274fd-133">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="274fd-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-134">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="274fd-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="274fd-135">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="274fd-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="274fd-136">包含零或多個適用于指定之參數類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="274fd-137">參數屬性可以取得和 **\[ 輸出 \]** 方向 **\[ 性 \] 屬性;** 欄位屬性 **\[** [**最大值 \_**](max-is.md)為 **\]** ，而 **\[** [**大小 \_ 為**](size-is.md) **\]** ; 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用屬性 **\[ 內容 \_ 句 \] 柄** 和 **\[ 字串 \]**。</span><span class="sxs-lookup"><span data-stu-id="274fd-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="274fd-138">Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="274fd-139">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="274fd-140">備註</span><span class="sxs-lookup"><span data-stu-id="274fd-140">Remarks</span></span>

<span data-ttu-id="274fd-141">如果 **\[ \] 字串** 屬性搭配在執行時間決定界限的陣列使用，則您也必須指定 [ **\[ \_ \]** **\[ \_ \]** 大小] 或 [最大值] 屬性，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="274fd-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="274fd-142">**\[ 字串 \]** 屬性不能與指定傳輸專案範圍的屬性搭配使用，例如 **\[ \_ \]** **\[ first \_ 是 \]**、last 和 **\[ length \_ \]**。</span><span class="sxs-lookup"><span data-stu-id="274fd-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="274fd-143">在多維陣列上使用時， **\[ 字串 \]** 屬性會套用至最右邊的陣列。</span><span class="sxs-lookup"><span data-stu-id="274fd-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="274fd-144">若要定義計數位符串，請勿使用 **\[ 字串 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="274fd-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="274fd-145">使用字元陣列或以字元為基礎的指標，如下所示：</span><span class="sxs-lookup"><span data-stu-id="274fd-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="274fd-146">**\[ 字串 \]** 屬性會指定存根應使用語言提供的方法來判斷字串的長度。</span><span class="sxs-lookup"><span data-stu-id="274fd-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="274fd-147">在 C 中宣告字串時，您必須配置空間給標記字串結尾的額外字元。</span><span class="sxs-lookup"><span data-stu-id="274fd-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="274fd-148">範例</span><span class="sxs-lookup"><span data-stu-id="274fd-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="274fd-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="274fd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="274fd-150">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="274fd-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="274fd-151">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="274fd-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="274fd-152">**回撥**</span><span class="sxs-lookup"><span data-stu-id="274fd-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="274fd-153">**字元**</span><span class="sxs-lookup"><span data-stu-id="274fd-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="274fd-154">**const**</span><span class="sxs-lookup"><span data-stu-id="274fd-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="274fd-155">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="274fd-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="274fd-156">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="274fd-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="274fd-157">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="274fd-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="274fd-158">**處理**</span><span class="sxs-lookup"><span data-stu-id="274fd-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="274fd-159"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="274fd-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="274fd-160">**忽略**</span><span class="sxs-lookup"><span data-stu-id="274fd-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="274fd-161">**last \_**</span><span class="sxs-lookup"><span data-stu-id="274fd-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="274fd-162">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="274fd-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="274fd-163">**當地**</span><span class="sxs-lookup"><span data-stu-id="274fd-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="274fd-164">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="274fd-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="274fd-165">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="274fd-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="274fd-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="274fd-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="274fd-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="274fd-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="274fd-168">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="274fd-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="274fd-169">**結構**</span><span class="sxs-lookup"><span data-stu-id="274fd-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="274fd-170">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="274fd-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="274fd-171">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="274fd-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="274fd-172">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="274fd-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="274fd-173">**獨特**</span><span class="sxs-lookup"><span data-stu-id="274fd-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="274fd-174">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="274fd-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 