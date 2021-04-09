---
title: retval 屬性
description: '\ Retval \ 屬性會指定接收成員傳回值的參數。'
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- retval 屬性 MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842131"
---
# <a name="retval-attribute"></a><span data-ttu-id="65b07-104">retval 屬性</span><span class="sxs-lookup"><span data-stu-id="65b07-104">retval attribute</span></span>

<span data-ttu-id="65b07-105">**\[ Retval \]** 屬性指定接收成員傳回值的參數。</span><span class="sxs-lookup"><span data-stu-id="65b07-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="65b07-106">參數</span><span class="sxs-lookup"><span data-stu-id="65b07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b07-107">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="65b07-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="65b07-108">遠端程式之傳回值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="65b07-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-109">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="65b07-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65b07-110">用來叫用遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="65b07-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-111">*選用-屬性*</span><span class="sxs-lookup"><span data-stu-id="65b07-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="65b07-112">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="65b07-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-113">*資料類型*</span><span class="sxs-lookup"><span data-stu-id="65b07-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="65b07-114">透過參數傳遞的資料型別。</span><span class="sxs-lookup"><span data-stu-id="65b07-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-115">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="65b07-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="65b07-116">參數的識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="65b07-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65b07-117">備註</span><span class="sxs-lookup"><span data-stu-id="65b07-117">Remarks</span></span>

<span data-ttu-id="65b07-118">您可以在描述方法或取得屬性之介面成員的參數上使用 **\[ retval \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="65b07-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="65b07-119"> (在具有 propget 屬性之方法的最後一個參數上需要屬性 **\[** [](propget.md) **\]** 。 ) 參數必須有 **\[** [**out**](out-idl.md) **\]** 屬性，而且必須是指標類型。</span><span class="sxs-lookup"><span data-stu-id="65b07-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="65b07-120">您無法將 **\[** [**選擇性**](optional.md) **\]** 屬性套用至 **\[ \] retval** 參數。</span><span class="sxs-lookup"><span data-stu-id="65b07-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="65b07-121">MIDL 編譯器接受下列參數排序 (從左至右) ：</span><span class="sxs-lookup"><span data-stu-id="65b07-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="65b07-122">未 **\[**) [**defaultvalue**](defaultvalue.md) **\]** 或 **\[** [**選擇性**](optional.md) **\]** 屬性 (參數所需的參數。</span><span class="sxs-lookup"><span data-stu-id="65b07-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="65b07-123">具有或不具有 **\[** [**defaultvalue**](defaultvalue.md)屬性的選擇性參數 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="65b07-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="65b07-124">具有 **\[** [**選擇性**](optional.md) **\]** 屬性且不含 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="65b07-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="65b07-125">**\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="65b07-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="65b07-126">**\[ retval \]** 參數。</span><span class="sxs-lookup"><span data-stu-id="65b07-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="65b07-127">具有 **\[ retval \]** 屬性的參數不會顯示在使用者導向的瀏覽器中。</span><span class="sxs-lookup"><span data-stu-id="65b07-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="65b07-128">Flags</span><span class="sxs-lookup"><span data-stu-id="65b07-128">Flags</span></span>

<span data-ttu-id="65b07-129">IDLFLAG \_ FRETVAL</span><span class="sxs-lookup"><span data-stu-id="65b07-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="65b07-130">範例</span><span class="sxs-lookup"><span data-stu-id="65b07-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="65b07-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65b07-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b07-132">**值**</span><span class="sxs-lookup"><span data-stu-id="65b07-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="65b07-133">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="65b07-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="65b07-134">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="65b07-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="65b07-135">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="65b07-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="65b07-136">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="65b07-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="65b07-137">**選**</span><span class="sxs-lookup"><span data-stu-id="65b07-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="65b07-138">**擴展**</span><span class="sxs-lookup"><span data-stu-id="65b07-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="65b07-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="65b07-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="65b07-140">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="65b07-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 