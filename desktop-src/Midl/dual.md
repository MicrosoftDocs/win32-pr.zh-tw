---
title: dual 屬性
description: 雙重屬性（attribute）會識別透過 IDispatch 公開屬性和方法的介面，以及直接透過 VTBL 來公開屬性和方法。
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- 雙重屬性 MIDL
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933220"
---
# <a name="dual-attribute"></a><span data-ttu-id="3f2a9-104">dual 屬性</span><span class="sxs-lookup"><span data-stu-id="3f2a9-104">dual attribute</span></span>

<span data-ttu-id="3f2a9-105">**雙重** 屬性（attribute）會識別透過 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)公開屬性和方法的介面，以及直接透過 VTBL 來公開屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="3f2a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f2a9-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="3f2a9-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="3f2a9-108">指定介面的通用唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="3f2a9-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="3f2a9-109">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="3f2a9-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3f2a9-110">指定零個或多個其他 MIDL 屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3f2a9-111">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="3f2a9-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3f2a9-112">將套用 **雙重** 屬性之介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f2a9-113">備註</span><span class="sxs-lookup"><span data-stu-id="3f2a9-113">Remarks</span></span>

<span data-ttu-id="3f2a9-114">**雙重** 屬性所識別的介面必須與 Automation 相容，並且衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="3f2a9-115">在分配介面上不允許此屬性。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="3f2a9-116">**雙重** 屬性會建立同時為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面和元件物件模型 (COM) 介面的介面。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="3f2a9-117">雙介面之 VTBL 的前七個專案是 **IDispatch** 的七個成員，而其餘專案則用於直接存取雙重介面的成員。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="3f2a9-118">針對雙重介面成員指定的所有參數和傳回型別都必須是自動化相容的類型。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="3f2a9-119">雙重介面的所有成員都必須傳遞 HRESULT 作為函數傳回值。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="3f2a9-120">需要傳回其他值的成員（例如屬性存取子函數）應該將最後一個參數指定為 [**out**](out-idl.md)， [**retval**](retval.md)，表示傳回函數值的 output 參數。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="3f2a9-121">此外，需要支援多個地區設定的成員應傳遞 [**lcid**](lcid.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="3f2a9-122">雙重介面可提供直接的 VTBL 系結速度和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 系結的彈性。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="3f2a9-123">基於這個理由，建議您盡可能使用雙重介面。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="3f2a9-124">如果您的應用程式藉由在介面呼叫內轉換 *this* 指標來存取物件資料，您應該針對自己的 vtbl 指標檢查物件中的 vtbl 指標，以確定您已連接到適當的 proxy。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="3f2a9-125">在介面上指定 **雙重** 表示介面與 Automation 相容，因此會同時 \_ 設定 TYPEFLAG FDUAL 和 TYPEFLAG \_ FOLEAUTOMATION 旗標。</span><span class="sxs-lookup"><span data-stu-id="3f2a9-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="3f2a9-126">Flags</span><span class="sxs-lookup"><span data-stu-id="3f2a9-126">Flags</span></span>

<span data-ttu-id="3f2a9-127">TYPEFLAG \_ FDUAL、TYPEFLAG \_ FOLEAUTOMATION</span><span class="sxs-lookup"><span data-stu-id="3f2a9-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="3f2a9-128">範例</span><span class="sxs-lookup"><span data-stu-id="3f2a9-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="3f2a9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f2a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2a9-130">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3f2a9-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3f2a9-131">**介面**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="3f2a9-132">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="3f2a9-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="3f2a9-134">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="3f2a9-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3f2a9-135">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="3f2a9-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3f2a9-136">**擴展**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3f2a9-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="3f2a9-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 