---
title: 陣列屬性
description: 陣列是索引或元素編號所存取的同質資料集合。
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- 陣列屬性 MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969494"
---
# <a name="arrays-attribute"></a><span data-ttu-id="2037e-104">陣列屬性</span><span class="sxs-lookup"><span data-stu-id="2037e-104">arrays attribute</span></span>

<span data-ttu-id="2037e-105">陣列是索引或元素編號所存取的同質資料集合。</span><span class="sxs-lookup"><span data-stu-id="2037e-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="2037e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2037e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2037e-107">*類型-attr-list*</span><span class="sxs-lookup"><span data-stu-id="2037e-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-108">指定套用至類型的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="2037e-109">有效的型別屬性包括 [**\[ 句 \] 柄**](handle.md)、 [**\[ 切換 \_ 類型 \]**](switch-type.md)、 [**\[ 傳輸 \_ 為 \]**](transmit-as.md); 指標屬性 [**\[ ref \]**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md); 以及使用方式屬性 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)、 [**\[ 字串 \]**](string.md)和 [**\[ 略 \]**](ignore.md)過。</span><span class="sxs-lookup"><span data-stu-id="2037e-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="2037e-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-111">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="2037e-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-112">指定類型識別碼、基底類型、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="2037e-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="2037e-113">類型規格可以包含選擇性的儲存規格。</span><span class="sxs-lookup"><span data-stu-id="2037e-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-114">*指標-decl*</span><span class="sxs-lookup"><span data-stu-id="2037e-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-115">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="2037e-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="2037e-116">指標宣告子與 C 中所使用的指標宣告子相同，它是由 **\*** 指示項、 **目前** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="2037e-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="2037e-117">*陣列-宣告子*</span><span class="sxs-lookup"><span data-stu-id="2037e-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-118">指定陣列的名稱，後面接著陣列的每個維度的下列其中一種結構： "**\[ \]**"、" **\[\*\]** "、"**\[ ***const1*** \]**" 或 "**\[ ***lower .。。*** upper \]**：*較低* 和 *上限* 是代表下限和上限的常數值。</span><span class="sxs-lookup"><span data-stu-id="2037e-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="2037e-119">常數 *下限* 必須評估為零。</span><span class="sxs-lookup"><span data-stu-id="2037e-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-120">*標籤*</span><span class="sxs-lookup"><span data-stu-id="2037e-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-121">指定結構或等位的選擇性標記。</span><span class="sxs-lookup"><span data-stu-id="2037e-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-122">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="2037e-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-123">指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="2037e-124">有效的欄位屬性 [**\[ 包括 \_ first \]**](first-is.md)、 [**\[ last \_ \]**](last-is.md) [**\[ 、length、 \_ length \]**](length-is.md)、 [**\[ \_ max \]**](max-is.md)、 [**\[ size、usage 屬性 \_ 字串和 ignore; 指標屬性 ref、unique 和 ptr; 以及 union 屬性參數類型。 \]**](size-is.md) [**\[ \]**](ref.md) [**\[ \_ \]**](switch-type.md) [**\[ \]**](string.md) [**\[ \]**](ignore.md) [**\[ \]**](unique.md) [**\[ \]**](ptr.md)</span><span class="sxs-lookup"><span data-stu-id="2037e-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="2037e-125">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="2037e-126">請注意，上面列出的屬性（ **\[ first \_ ） \] 是**、 **\[ last \_ \]** 和 [**\[ ignore \]**](ignore.md)對等位無效。</span><span class="sxs-lookup"><span data-stu-id="2037e-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-127">*有限運算式*</span><span class="sxs-lookup"><span data-stu-id="2037e-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-128">指定 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="2037e-128">Specifies a C-language expression.</span></span> <span data-ttu-id="2037e-129">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="2037e-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="2037e-130">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="2037e-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-131">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="2037e-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-132">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="2037e-133">有效的函式屬性為 [**\[ \] 回呼**](callback.md)、 [**\[ local \]**](local.md)、指標屬性 [**\[ ref \]**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md); 以及使用方式屬性 [**\[ 字串 \]**](string.md)和 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="2037e-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="2037e-134">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="2037e-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-135">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2037e-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="2037e-136">*param-attr-list*</span><span class="sxs-lookup"><span data-stu-id="2037e-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2037e-137">指定方向屬性以及套用至陣列參數的一或多個選擇性欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="2037e-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="2037e-138">有效 [**\[ \_ 的 \]**](max-is.md)欄位屬性包括 max、 [**\[ size \_ \]**](size-is.md)、 [**\[ \_ length \]**](length-is.md)、 [**\[ first \_ 是 \]**](first-is.md)和 [**\[ last \_ 。 \]**](last-is.md)</span><span class="sxs-lookup"><span data-stu-id="2037e-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2037e-139">備註</span><span class="sxs-lookup"><span data-stu-id="2037e-139">Remarks</span></span>

<span data-ttu-id="2037e-140">MIDL 中的陣列使用類似于但與 C 和 c + + 不完全相同的樣式。</span><span class="sxs-lookup"><span data-stu-id="2037e-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="2037e-141">如需詳細資訊，請參閱 [MIDL 陣列](midl-arrays.md)。</span><span class="sxs-lookup"><span data-stu-id="2037e-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2037e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2037e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2037e-143">**回撥**</span><span class="sxs-lookup"><span data-stu-id="2037e-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="2037e-144">**const**</span><span class="sxs-lookup"><span data-stu-id="2037e-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="2037e-145">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="2037e-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="2037e-146">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="2037e-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2037e-147">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="2037e-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="2037e-148">**處理**</span><span class="sxs-lookup"><span data-stu-id="2037e-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="2037e-149"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="2037e-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2037e-150">**忽略**</span><span class="sxs-lookup"><span data-stu-id="2037e-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="2037e-151">**last \_**</span><span class="sxs-lookup"><span data-stu-id="2037e-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="2037e-152">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="2037e-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="2037e-153">**當地**</span><span class="sxs-lookup"><span data-stu-id="2037e-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2037e-154">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="2037e-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="2037e-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="2037e-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="2037e-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="2037e-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="2037e-157">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="2037e-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="2037e-158">**字串**</span><span class="sxs-lookup"><span data-stu-id="2037e-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="2037e-159">**結構**</span><span class="sxs-lookup"><span data-stu-id="2037e-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="2037e-160">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="2037e-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="2037e-161">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="2037e-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="2037e-162">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="2037e-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="2037e-163">**獨特**</span><span class="sxs-lookup"><span data-stu-id="2037e-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




