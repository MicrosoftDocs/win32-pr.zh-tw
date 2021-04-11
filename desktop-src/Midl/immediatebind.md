---
title: immediatebind 屬性
description: '\ Immediatebind \ 屬性工作表示資料庫將會立即收到資料系結物件屬性之所有變更的通知。'
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind 屬性 MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185569"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="e05d0-104">immediatebind 屬性</span><span class="sxs-lookup"><span data-stu-id="e05d0-104">immediatebind attribute</span></span>

<span data-ttu-id="e05d0-105">**\[ Immediatebind \]** 屬性指出資料庫將會立即收到資料系結物件屬性之所有變更的通知。</span><span class="sxs-lookup"><span data-stu-id="e05d0-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="e05d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e05d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05d0-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="e05d0-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-108">指定套用至整個介面的一或多個屬性清單。</span><span class="sxs-lookup"><span data-stu-id="e05d0-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="e05d0-109">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="e05d0-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-110">指定 [**介面**](interface.md)[**或分配介面的**](dispinterface.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="e05d0-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e05d0-111">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="e05d0-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-112">零或多個函數屬性。</span><span class="sxs-lookup"><span data-stu-id="e05d0-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e05d0-113">*returntype*</span><span class="sxs-lookup"><span data-stu-id="e05d0-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-114">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="e05d0-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e05d0-115">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="e05d0-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-116">在 IDL 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="e05d0-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e05d0-117">*params*</span><span class="sxs-lookup"><span data-stu-id="e05d0-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="e05d0-118">零或多個函數參數。</span><span class="sxs-lookup"><span data-stu-id="e05d0-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e05d0-119">備註</span><span class="sxs-lookup"><span data-stu-id="e05d0-119">Remarks</span></span>

<span data-ttu-id="e05d0-120">**\[ Immediatebind \]** 屬性可讓控制項區分需要通知資料庫每項變更的屬性，以及不需要通知資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e05d0-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="e05d0-121">例如，即使控制項尚未遺失焦點，也應該立即將 checkbox 控制項的每個變更傳送到基礎資料庫。</span><span class="sxs-lookup"><span data-stu-id="e05d0-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="e05d0-122">不過，若為 listbox 控制項，則會在反白顯示不同的選取專案時進行變更。</span><span class="sxs-lookup"><span data-stu-id="e05d0-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="e05d0-123">在控制項失去焦點之前通知資料庫變更，將不會有效率且不需要。</span><span class="sxs-lookup"><span data-stu-id="e05d0-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="e05d0-124">**\[ Immediatebind \]** 屬性可讓您藉由在應立即回報變更的表單上設定 immediatebind 位，來指定個別的屬性。</span><span class="sxs-lookup"><span data-stu-id="e05d0-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="e05d0-125">具有 **\[ immediatebind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e05d0-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="e05d0-126">Flags</span><span class="sxs-lookup"><span data-stu-id="e05d0-126">Flags</span></span>

<span data-ttu-id="e05d0-127">FUNCFLAG \_ FIMMEDIATEBIND、VARFLAG \_ FIMMEDIATEBIND</span><span class="sxs-lookup"><span data-stu-id="e05d0-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="e05d0-128">範例</span><span class="sxs-lookup"><span data-stu-id="e05d0-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="e05d0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e05d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05d0-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="e05d0-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="e05d0-131">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="e05d0-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="e05d0-132">**介面**</span><span class="sxs-lookup"><span data-stu-id="e05d0-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e05d0-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="e05d0-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="e05d0-134">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="e05d0-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e05d0-135">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="e05d0-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e05d0-136">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e05d0-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 