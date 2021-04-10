---
title: 標注屬性
description: '\ 批註 \ 屬性可讓您為指定的方法、參數或結構欄位指定 SAL 批註字串。'
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- 標注屬性 MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683554"
---
# <a name="annotate-attribute"></a><span data-ttu-id="81cfb-104">標注屬性</span><span class="sxs-lookup"><span data-stu-id="81cfb-104">annotate attribute</span></span>

<span data-ttu-id="81cfb-105">**\[ 批註 \]** 屬性可讓您為指定的方法、參數或結構欄位指定 SAL 批註字串。</span><span class="sxs-lookup"><span data-stu-id="81cfb-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="81cfb-106">參數</span><span class="sxs-lookup"><span data-stu-id="81cfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81cfb-107">*string*</span><span class="sxs-lookup"><span data-stu-id="81cfb-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-108">指定的 SAL 批註字串。</span><span class="sxs-lookup"><span data-stu-id="81cfb-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-109">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="81cfb-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-110">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="81cfb-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="81cfb-111">有效的函式屬性包括 [**\[ \] 回呼**](callback.md)、指標屬性 [**\[ \] ref**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md)，以及使用方式屬性 [**\[ 字串 \]**](string.md)、 [**\[ 忽略 \]**](ignore.md)和 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="81cfb-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="81cfb-112">多個屬性必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="81cfb-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-113">*函式宣告子*</span><span class="sxs-lookup"><span data-stu-id="81cfb-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-114">指定函數的型別規範、函式名稱和參數清單。</span><span class="sxs-lookup"><span data-stu-id="81cfb-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-115">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="81cfb-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-116">指定 **基底 \_ 類型**、 [**\[ 結構 \]**](struct.md)、[**等**](union.md)位或 [**\[ 列舉 \]**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="81cfb-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="81cfb-117">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="81cfb-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-118">*指標宣告子*</span><span class="sxs-lookup"><span data-stu-id="81cfb-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-119">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="81cfb-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="81cfb-120">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**\[ const \]**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="81cfb-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-121">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="81cfb-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-122">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="81cfb-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-123">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="81cfb-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-124">指定適用于參數類型的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="81cfb-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="81cfb-125">具有 [**\[ \] in**](in.md)屬性的參數屬性也可以取得 [**\[ \] 方向屬性**](out-idl.md) [**\[ \]**](string.md) [**\[ \_ \]**](length-is.md) [**\[ \]**](unique.md) [**\[ \]**](ptr.md) [**\[ \_ \]**](last-is.md) [**\[ \]**](ref.md) [**\[ \_ ，第 \] 一個**](first-is.md)欄位屬性 [**\[ \_ 是、last、length、max、size、size、以及 switch type、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]**](max-is.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](context-handle.md) [**\[ \_ \]**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="81cfb-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="81cfb-126">Usage 屬性 [**\[ ignore \]**](ignore.md)不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="81cfb-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="81cfb-127">多個屬性必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="81cfb-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="81cfb-128">*符中*</span><span class="sxs-lookup"><span data-stu-id="81cfb-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfb-129">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="81cfb-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="81cfb-130">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**\[ \] 、陣列、陣列和**](../rpc/arrays.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="81cfb-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="81cfb-131">函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="81cfb-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81cfb-132">備註</span><span class="sxs-lookup"><span data-stu-id="81cfb-132">Remarks</span></span>

<span data-ttu-id="81cfb-133">**\[ 批註 \]** 屬性允許覆寫 midl 產生的 SAL 注釋，或將它們加入至 midl 未明確產生注釋的位置。</span><span class="sxs-lookup"><span data-stu-id="81cfb-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="81cfb-134">如果未在命令列上指定 [**/sal**](-sal.md) ，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="81cfb-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="81cfb-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81cfb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81cfb-136">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="81cfb-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="81cfb-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="81cfb-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="81cfb-138">**/sal \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="81cfb-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 