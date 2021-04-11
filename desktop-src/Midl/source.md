---
title: source 屬性
description: '\ Source \ 屬性工作表示 coclass、屬性或方法的成員是事件來源。 對於 coclass 的成員而言，這個屬性工作表示會呼叫該成員，而不是實作為成員。'
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- source 屬性 MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933114"
---
# <a name="source-attribute"></a><span data-ttu-id="8841c-105">source 屬性</span><span class="sxs-lookup"><span data-stu-id="8841c-105">source attribute</span></span>

<span data-ttu-id="8841c-106">**\[ Source \]** 屬性工作表示 [**coclass**](coclass.md)、屬性或方法的成員是事件來源。</span><span class="sxs-lookup"><span data-stu-id="8841c-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="8841c-107">對於 **coclass** 的成員而言，這個屬性工作表示會呼叫該成員，而不是實作為成員。</span><span class="sxs-lookup"><span data-stu-id="8841c-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="8841c-108">參數</span><span class="sxs-lookup"><span data-stu-id="8841c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8841c-109">*coclass-屬性*</span><span class="sxs-lookup"><span data-stu-id="8841c-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-110">將套用至 [**coclass**](coclass.md)的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="8841c-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="8841c-111">*coclass-名稱*</span><span class="sxs-lookup"><span data-stu-id="8841c-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-112">[**Coclass**](coclass.md)的名稱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8841c-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="8841c-113">*選用-屬性*</span><span class="sxs-lookup"><span data-stu-id="8841c-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-114">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="8841c-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-115">*語句類型*</span><span class="sxs-lookup"><span data-stu-id="8841c-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-116">可以是 [**介面或介面介面**](interface.md)。 [](dispinterface.md)</span><span class="sxs-lookup"><span data-stu-id="8841c-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8841c-117">*語句-名稱*</span><span class="sxs-lookup"><span data-stu-id="8841c-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-118">介面 [**或分配**](dispinterface.md)[**介面**](interface.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="8841c-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8841c-119">*物件類型*</span><span class="sxs-lookup"><span data-stu-id="8841c-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-120">方法傳回的物件類型。</span><span class="sxs-lookup"><span data-stu-id="8841c-120">The type of the object that the method returns.</span></span> <span data-ttu-id="8841c-121">此物件是事件的來源。</span><span class="sxs-lookup"><span data-stu-id="8841c-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="8841c-122">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="8841c-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-123">[**介面**](interface.md)[**或分配介面中**](dispinterface.md)方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="8841c-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8841c-124">*選擇性-參數-清單*</span><span class="sxs-lookup"><span data-stu-id="8841c-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8841c-125">零或多個方法參數。</span><span class="sxs-lookup"><span data-stu-id="8841c-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8841c-126">備註</span><span class="sxs-lookup"><span data-stu-id="8841c-126">Remarks</span></span>

<span data-ttu-id="8841c-127">在屬性或方法上， **\[ source \]** 屬性會指出成員會傳回屬於事件來源的物件或變異數。</span><span class="sxs-lookup"><span data-stu-id="8841c-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="8841c-128">物件會執行 **IConnectionPointContainer**。</span><span class="sxs-lookup"><span data-stu-id="8841c-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="8841c-129">Flags</span><span class="sxs-lookup"><span data-stu-id="8841c-129">Flags</span></span>

<span data-ttu-id="8841c-130">IMPLTYPEFLAG \_ FSOURCE、VARFLAG \_ 來源、FUNCFLAG \_ 來源</span><span class="sxs-lookup"><span data-stu-id="8841c-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="8841c-131">範例</span><span class="sxs-lookup"><span data-stu-id="8841c-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="8841c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8841c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8841c-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="8841c-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="8841c-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="8841c-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="8841c-135">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8841c-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="8841c-136">**介面**</span><span class="sxs-lookup"><span data-stu-id="8841c-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="8841c-137">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="8841c-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8841c-138">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="8841c-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8841c-139">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="8841c-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 