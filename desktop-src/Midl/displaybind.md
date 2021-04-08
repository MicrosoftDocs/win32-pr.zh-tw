---
title: displaybind 屬性
description: '\ Displaybind \ 屬性工作表示應該向使用者顯示為可系結的屬性。'
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- displaybind 屬性 MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681891"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="e9f77-104">displaybind 屬性</span><span class="sxs-lookup"><span data-stu-id="e9f77-104">displaybind attribute</span></span>

<span data-ttu-id="e9f77-105">**\[ Displaybind \]** 屬性工作表示應該向使用者顯示為可系結的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9f77-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="e9f77-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9f77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f77-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="e9f77-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-108">指定介面屬性的選擇性清單。</span><span class="sxs-lookup"><span data-stu-id="e9f77-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e9f77-109">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="e9f77-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-110">介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9f77-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e9f77-111">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="e9f77-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-112">指定套用至函式傳回型別的一或多個屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="e9f77-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="e9f77-113">*returntype*</span><span class="sxs-lookup"><span data-stu-id="e9f77-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-114">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="e9f77-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e9f77-115">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="e9f77-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-116">指定將套用 **\[ displaybind \]** 屬性的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="e9f77-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e9f77-117">*params*</span><span class="sxs-lookup"><span data-stu-id="e9f77-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f77-118">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="e9f77-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f77-119">備註</span><span class="sxs-lookup"><span data-stu-id="e9f77-119">Remarks</span></span>

<span data-ttu-id="e9f77-120">具有 **\[ displaybind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9f77-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="e9f77-121">物件可以支援資料系結，但不能有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e9f77-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="e9f77-122">Flags</span><span class="sxs-lookup"><span data-stu-id="e9f77-122">Flags</span></span>

<span data-ttu-id="e9f77-123">FUNCFLAG \_ FDISPLAYBIND、VARFLAG \_ FDISPLAYBIND</span><span class="sxs-lookup"><span data-stu-id="e9f77-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="e9f77-124">範例</span><span class="sxs-lookup"><span data-stu-id="e9f77-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="e9f77-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9f77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f77-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="e9f77-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="e9f77-127">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="e9f77-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="e9f77-128">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="e9f77-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e9f77-129">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="e9f77-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e9f77-130">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9f77-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 