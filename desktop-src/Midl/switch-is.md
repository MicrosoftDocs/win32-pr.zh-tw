---
title: switch_is 屬性
description: '\ 參數 \_ 是 \ 屬性，它會指定運算式或識別碼，做為選取聯集成員的聯集判別。'
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is 屬性 MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932720"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="a08ff-104">切換 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="a08ff-104">switch\_is attribute</span></span>

<span data-ttu-id="a08ff-105">**\[ 參數 \_ 為 \]** attribute 指定運算式或識別碼，做為選取聯集成員的聯集判別。</span><span class="sxs-lookup"><span data-stu-id="a08ff-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="a08ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="a08ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08ff-107">*結構標記*</span><span class="sxs-lookup"><span data-stu-id="a08ff-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-108">指定結構的選擇性標記。</span><span class="sxs-lookup"><span data-stu-id="a08ff-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-109">*有限-expr*</span><span class="sxs-lookup"><span data-stu-id="a08ff-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-110">指定 MIDL 所支援的 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="a08ff-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="a08ff-111">幾乎所有的 C 語言運算式都受到支援。</span><span class="sxs-lookup"><span data-stu-id="a08ff-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="a08ff-112">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="a08ff-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="a08ff-113">MIDL 不允許運算式中的函式呼叫，也不允許前置和後置遞增以及前置和後置遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="a08ff-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-114">*欄位-attr-list*</span><span class="sxs-lookup"><span data-stu-id="a08ff-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-115">指定適用于聯集成員的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="a08ff-116">有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md); **\]** 以及本身聯集的成員（union attribute **\[** [**switch \_ 型**](switch-type.md)別） **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a08ff-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="a08ff-117">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-118">*union 類型規範*</span><span class="sxs-lookup"><span data-stu-id="a08ff-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-119">指定聯 [**集**](union.md) 類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="a08ff-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="a08ff-120">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="a08ff-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-121">*宣告子和宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="a08ff-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-122">指定標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="a08ff-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="a08ff-123">在遠端程序呼叫中傳輸的等位中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="a08ff-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="a08ff-124">未傳輸的等位中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="a08ff-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-125">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a08ff-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-126">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a08ff-127">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。</span><span class="sxs-lookup"><span data-stu-id="a08ff-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-128">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="a08ff-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-129">指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="a08ff-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="a08ff-130">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="a08ff-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-131">*指標宣告子*</span><span class="sxs-lookup"><span data-stu-id="a08ff-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-132">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="a08ff-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="a08ff-133">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="a08ff-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-134">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a08ff-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-135">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a08ff-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-136">*param-attr-list*</span><span class="sxs-lookup"><span data-stu-id="a08ff-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-137">指定適用于指定之參數類型的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="a08ff-138">參數屬性可以取得和 **\[ \] 輸出** 方向 **\[ \] 性屬性，** **\[ 第一個 \_ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** 欄位屬性 **\[ \_ 是、最後一個、長度為、最大值、大小為，以及切換類型、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="a08ff-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="a08ff-139">Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="a08ff-140">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a08ff-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a08ff-141">*聯集類型*</span><span class="sxs-lookup"><span data-stu-id="a08ff-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a08ff-142">識別聯 [**集**](union.md) 類型規範。</span><span class="sxs-lookup"><span data-stu-id="a08ff-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a08ff-143">備註</span><span class="sxs-lookup"><span data-stu-id="a08ff-143">Remarks</span></span>

<span data-ttu-id="a08ff-144">與 **\[ \_ 參數 \]** 相關聯的判別必須在與聯集相同的邏輯層級上定義：</span><span class="sxs-lookup"><span data-stu-id="a08ff-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="a08ff-145">當 union 是參數時，聯集判別必須是另一個參數。</span><span class="sxs-lookup"><span data-stu-id="a08ff-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="a08ff-146">當聯集是結構的欄位時，判別必須是相同結構的另一個欄位。</span><span class="sxs-lookup"><span data-stu-id="a08ff-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="a08ff-147">結構或函數參數清單中的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="a08ff-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="a08ff-148">聯集可以在判別之前或之後。</span><span class="sxs-lookup"><span data-stu-id="a08ff-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="a08ff-149">參數的屬性可以顯示為欄位屬性，或做為參數屬性。 **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="a08ff-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a08ff-150">範例</span><span class="sxs-lookup"><span data-stu-id="a08ff-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="a08ff-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a08ff-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08ff-152">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="a08ff-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a08ff-153">**回撥**</span><span class="sxs-lookup"><span data-stu-id="a08ff-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="a08ff-154">**const**</span><span class="sxs-lookup"><span data-stu-id="a08ff-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a08ff-155">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="a08ff-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a08ff-156">封裝聯集</span><span class="sxs-lookup"><span data-stu-id="a08ff-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="a08ff-157">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="a08ff-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a08ff-158">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="a08ff-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="a08ff-159">**忽略**</span><span class="sxs-lookup"><span data-stu-id="a08ff-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a08ff-160">**last \_**</span><span class="sxs-lookup"><span data-stu-id="a08ff-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="a08ff-161">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="a08ff-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="a08ff-162">**當地**</span><span class="sxs-lookup"><span data-stu-id="a08ff-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a08ff-163">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="a08ff-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="a08ff-164">Nonencapsulated 聯集</span><span class="sxs-lookup"><span data-stu-id="a08ff-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="a08ff-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a08ff-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a08ff-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="a08ff-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a08ff-167">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="a08ff-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="a08ff-168">**字串**</span><span class="sxs-lookup"><span data-stu-id="a08ff-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="a08ff-169">**結構**</span><span class="sxs-lookup"><span data-stu-id="a08ff-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a08ff-170">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a08ff-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="a08ff-171">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="a08ff-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a08ff-172">**獨特**</span><span class="sxs-lookup"><span data-stu-id="a08ff-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




