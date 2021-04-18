---
title: out 屬性
description: '\\ 屬性會識別從被呼叫程式傳回至呼叫程式的指標參數， (從伺服器到用戶端) 。'
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- out 屬性 MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965234"
---
# <a name="out-attribute"></a><span data-ttu-id="75b36-104">out 屬性</span><span class="sxs-lookup"><span data-stu-id="75b36-104">out attribute</span></span>

<span data-ttu-id="75b36-105">\[ **Out** \] 屬性會識別從呼叫程式傳回至呼叫程式的指標參數， (從伺服器到用戶端) 。</span><span class="sxs-lookup"><span data-stu-id="75b36-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="75b36-106">參數</span><span class="sxs-lookup"><span data-stu-id="75b36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b36-107">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="75b36-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-108">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="75b36-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="75b36-109">有效的函式屬性為 \[ [**回呼**](callback.md) \] 、 \[ [**local**](local.md)、 \] 指標屬性 \[ [**ref**](ref.md) \] 、 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] ; 以及使用方式屬性 \[ [**字串**](string.md) \] 、 \[ [**忽略**](ignore.md) \] 和 \[ [**內容 \_ 控制碼**](context-handle.md) \] 。</span><span class="sxs-lookup"><span data-stu-id="75b36-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="75b36-110">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="75b36-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-111">指定 [基底 \_ 類型](midl-base-types.md)、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="75b36-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="75b36-112">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="75b36-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="75b36-113">*指標宣告子*</span><span class="sxs-lookup"><span data-stu-id="75b36-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-114">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="75b36-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="75b36-115">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="75b36-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="75b36-116">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="75b36-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-117">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="75b36-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="75b36-118">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="75b36-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-119">指定適用于指定之參數類型的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="75b36-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="75b36-120">具有 out 屬性的參數屬性 \[  \] 也可以取得方向屬性 \[  \] \[ ，[**第一個欄位屬性 \_ 是**](first-is.md) \] 、 \[ [**last \_**](last-is.md) \] 、 \[ [**length、 \_**](length-is.md) \] max、size、 \[ [**\_**](max-is.md) \] \[ [**\_ size**](size-is.md) \] 、and \[ [**switch \_ type**](switch-type.md)、 \] 指標屬性 \[ [**ref**](ref.md) \] 、 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] ; 以及 usage 屬性 \[ [**內容 \_ 控制碼**](context-handle.md) \] 和 \[ [**字串**](string.md) \] 。</span><span class="sxs-lookup"><span data-stu-id="75b36-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="75b36-121">Usage 屬性 \[ [**ignore**](ignore.md) \] 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="75b36-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="75b36-122">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="75b36-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="75b36-123">*符中*</span><span class="sxs-lookup"><span data-stu-id="75b36-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="75b36-124">指定標準宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="75b36-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="75b36-125">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="75b36-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="75b36-126">函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="75b36-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75b36-127">備註</span><span class="sxs-lookup"><span data-stu-id="75b36-127">Remarks</span></span>

<span data-ttu-id="75b36-128">\[ **Out** \] 屬性工作表示在記憶體中作為指標的參數和其相關聯的資料，會從被呼叫的程式傳回給呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="75b36-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="75b36-129">\[ **Out** \] 屬性必須是指標。</span><span class="sxs-lookup"><span data-stu-id="75b36-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="75b36-130">在參數宣告中，DCE IDL 編譯器需要有明確的 \* ，做為指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="75b36-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="75b36-131">Microsoft IDL 提供的延伸模組會捨棄這項需求，並允許陣列或先前定義的指標類型。</span><span class="sxs-lookup"><span data-stu-id="75b36-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="75b36-132">中的相關屬性（attribute） \[ [](in.md) \] 表示參數是從呼叫程式傳遞至被呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="75b36-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="75b36-133">\[ **In** \] 和 \[ **out** \] 屬性指定傳遞參數的方向。</span><span class="sxs-lookup"><span data-stu-id="75b36-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="75b36-134">參數可以定義為 \[  \] 僅限 in、 \[ **out** \] 或 \[ **in**、 **out** \] 。</span><span class="sxs-lookup"><span data-stu-id="75b36-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="75b36-135">\[  \] 當呼叫遠端程式時，系統會假設不定義 out 參數，而伺服器會設定物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="75b36-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="75b36-136">因為最上層指標/參數必須一律指向有效的儲存體，因此不能是 **Null**，所以 \[  \] 無法套用至最上層的 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] 指標。</span><span class="sxs-lookup"><span data-stu-id="75b36-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="75b36-137">\[**唯一** \] 或 \[ **ptr** \] 指標的參數必須是 \[ [**in**](in.md) \] 或 \[ **in**、 **out** \] 參數。</span><span class="sxs-lookup"><span data-stu-id="75b36-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="75b36-138">範例</span><span class="sxs-lookup"><span data-stu-id="75b36-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="75b36-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75b36-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b36-140">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="75b36-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="75b36-141">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="75b36-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="75b36-142">**回撥**</span><span class="sxs-lookup"><span data-stu-id="75b36-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="75b36-143">**const**</span><span class="sxs-lookup"><span data-stu-id="75b36-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="75b36-144">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="75b36-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="75b36-145">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="75b36-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="75b36-146">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="75b36-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="75b36-147">**忽略**</span><span class="sxs-lookup"><span data-stu-id="75b36-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="75b36-148">**在**</span><span class="sxs-lookup"><span data-stu-id="75b36-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="75b36-149">**last \_**</span><span class="sxs-lookup"><span data-stu-id="75b36-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="75b36-150">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="75b36-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="75b36-151">**當地**</span><span class="sxs-lookup"><span data-stu-id="75b36-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="75b36-152">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="75b36-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="75b36-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="75b36-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="75b36-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="75b36-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="75b36-155">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="75b36-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="75b36-156">**字串**</span><span class="sxs-lookup"><span data-stu-id="75b36-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="75b36-157">**結構**</span><span class="sxs-lookup"><span data-stu-id="75b36-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="75b36-158">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="75b36-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="75b36-159">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="75b36-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="75b36-160">**獨特**</span><span class="sxs-lookup"><span data-stu-id="75b36-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 