---
title: bindable 屬性
description: '\ 可系結 \ 屬性工作表示屬性支援資料系結。'
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- 可系結屬性 MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106995150"
---
# <a name="bindable-attribute"></a><span data-ttu-id="9586d-104">bindable 屬性</span><span class="sxs-lookup"><span data-stu-id="9586d-104">bindable attribute</span></span>

<span data-ttu-id="9586d-105">可系結屬性工作表示屬性支援資料系結。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="9586d-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="9586d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9586d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9586d-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="9586d-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-108">指定套用至整個介面的零或多個 IDL 屬性清單。</span><span class="sxs-lookup"><span data-stu-id="9586d-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="9586d-109">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="9586d-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="9586d-110">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="9586d-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-111">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="9586d-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="9586d-112">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="9586d-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-113">指定套用至屬性之函式原型的零或多個屬性，或是 [**介面**](interface.md) 或 [**介面介面中**](dispinterface.md)方法的屬性。</span><span class="sxs-lookup"><span data-stu-id="9586d-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="9586d-114">以下是有效的屬性： [**\[ helpstring \]**](helpstring.md)、 [**\[ helpcoNtext \]**](helpcontext.md)、 [**\[ string \]**](string.md)、 [**\[ defaultbind \]**](defaultbind.md)、 [**\[ displaybind \]**](displaybind.md)、 [**\[ immediatebind \]**](immediatebind.md)、 [**\[ propget \]**](propget.md)、 [**\[ propput \]**](propput.md)、 [**\[ propputref \]**](propputref.md)和 [**\[ vararg \]**](vararg.md)。</span><span class="sxs-lookup"><span data-stu-id="9586d-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="9586d-115">如果指定了 **vararg** ，則最後一個參數必須是 VARIANT 類型的安全陣列。</span><span class="sxs-lookup"><span data-stu-id="9586d-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="9586d-116">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="9586d-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9586d-117">*returntype*</span><span class="sxs-lookup"><span data-stu-id="9586d-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-118">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="9586d-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="9586d-119">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="9586d-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-120">指定將套用可系結 **\[ \] 屬性之** 函式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9586d-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="9586d-121">*params*</span><span class="sxs-lookup"><span data-stu-id="9586d-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="9586d-122">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="9586d-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9586d-123">備註</span><span class="sxs-lookup"><span data-stu-id="9586d-123">Remarks</span></span>

<span data-ttu-id="9586d-124">藉由支援資料系結 **\[ \]** ，可系結屬性可讓用戶端在屬性變更值時收到通知。</span><span class="sxs-lookup"><span data-stu-id="9586d-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="9586d-125"> (如果您希望用戶端收到屬性即將變更的通知，請使用 [**\[ requestedit \]**](requestedit.md)屬性。 ) </span><span class="sxs-lookup"><span data-stu-id="9586d-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="9586d-126">因為可系結屬性會將屬性（property）視為整個屬性（property），所以必須在定義屬性的位置指定該屬性（property）。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="9586d-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="9586d-127">因此，您必須同時在屬性存取函式和屬性設定函數上指定屬性。</span><span class="sxs-lookup"><span data-stu-id="9586d-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="9586d-128">Flags</span><span class="sxs-lookup"><span data-stu-id="9586d-128">Flags</span></span>

<span data-ttu-id="9586d-129">FUNCFLAG \_ FBINDABLE、VARFLAG \_ FBINDABLE</span><span class="sxs-lookup"><span data-stu-id="9586d-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="9586d-130">範例</span><span class="sxs-lookup"><span data-stu-id="9586d-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="9586d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9586d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9586d-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="9586d-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="9586d-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="9586d-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="9586d-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="9586d-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="9586d-135">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9586d-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="9586d-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="9586d-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="9586d-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="9586d-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="9586d-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="9586d-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="9586d-139">**介面**</span><span class="sxs-lookup"><span data-stu-id="9586d-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="9586d-140">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="9586d-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9586d-141">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="9586d-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9586d-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="9586d-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="9586d-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="9586d-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="9586d-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="9586d-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="9586d-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="9586d-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="9586d-146">**字串**</span><span class="sxs-lookup"><span data-stu-id="9586d-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9586d-147">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="9586d-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="9586d-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="9586d-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 