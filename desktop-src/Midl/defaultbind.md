---
title: defaultbind 屬性
description: '\ Defaultbind \ 屬性工作表示最能代表物件的單一、可系結屬性。'
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- defaultbind 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023449"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="a7893-104">defaultbind 屬性</span><span class="sxs-lookup"><span data-stu-id="a7893-104">defaultbind attribute</span></span>

<span data-ttu-id="a7893-105">**\[ Defaultbind \]** 屬性工作表示最能代表物件的單一、可系結屬性。</span><span class="sxs-lookup"><span data-stu-id="a7893-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="a7893-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7893-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a7893-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-108">指定套用至整個介面的一或多個屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a7893-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a7893-109">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="a7893-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-110">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="a7893-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-111">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7893-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-112">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a7893-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-113">指定套用至函數的一或多個屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a7893-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="a7893-114">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="a7893-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-115">*returntype*</span><span class="sxs-lookup"><span data-stu-id="a7893-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-116">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="a7893-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-117">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a7893-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-118">指定將套用 **\[ defaultbind \]** 屬性的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="a7893-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="a7893-119">*params*</span><span class="sxs-lookup"><span data-stu-id="a7893-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a7893-120">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="a7893-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7893-121">備註</span><span class="sxs-lookup"><span data-stu-id="a7893-121">Remarks</span></span>

<span data-ttu-id="a7893-122">具有 **\[ defaultbind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7893-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="a7893-123">介面或分配介面中只有一個屬性可以有 **\[ defaultbind \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7893-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="a7893-124">如果容器具有與物件系結的使用者模型，而不是系結至物件的屬性，則會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a7893-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="a7893-125">物件可以支援資料系結，但不能有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a7893-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="a7893-126">Flags</span><span class="sxs-lookup"><span data-stu-id="a7893-126">Flags</span></span>

<span data-ttu-id="a7893-127">FUNCFLAG \_ FDEFAULTBIND、VARFLAG \_ FDEFAULTBIND</span><span class="sxs-lookup"><span data-stu-id="a7893-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="a7893-128">範例</span><span class="sxs-lookup"><span data-stu-id="a7893-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="a7893-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7893-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7893-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="a7893-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="a7893-131">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a7893-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a7893-132">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="a7893-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a7893-133">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="a7893-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a7893-134">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="a7893-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 