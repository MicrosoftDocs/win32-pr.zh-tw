---
title: default 屬性
description: '\ Default \ 屬性工作表示在 coclass 內定義的介面或介面介面，代表預設的可程式性介面。 這個屬性是供宏語言使用。'
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- 預設屬性 MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463009"
---
# <a name="default-attribute"></a><span data-ttu-id="22a5e-105">default 屬性</span><span class="sxs-lookup"><span data-stu-id="22a5e-105">default attribute</span></span>

<span data-ttu-id="22a5e-106">**\[ 預設 \]** 屬性會指出在 [**coclass**](coclass.md)內定義的 [**介面**](interface.md)[**或介面介面，**](dispinterface.md)代表預設的可程式性介面。</span><span class="sxs-lookup"><span data-stu-id="22a5e-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="22a5e-107">這個屬性是供宏語言使用。</span><span class="sxs-lookup"><span data-stu-id="22a5e-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="22a5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="22a5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a5e-109">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="22a5e-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="22a5e-110">指定 [**coclass**](coclass.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="22a5e-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="22a5e-111">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="22a5e-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="22a5e-112">指定其他 [**coclass**](coclass.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="22a5e-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="22a5e-113">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="22a5e-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="22a5e-114">*coclass-名稱*</span><span class="sxs-lookup"><span data-stu-id="22a5e-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="22a5e-115">指定其他軟體元件可以參考此 [**coclass**](coclass.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="22a5e-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="22a5e-116">*選用-interface 屬性*</span><span class="sxs-lookup"><span data-stu-id="22a5e-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="22a5e-117">**\[** [**Source**](source.md) **\]** 屬性（指定介面或分配介面為傳出）是唯一可在此處使用的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="22a5e-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="22a5e-118">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="22a5e-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="22a5e-119">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="22a5e-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22a5e-120">備註</span><span class="sxs-lookup"><span data-stu-id="22a5e-120">Remarks</span></span>

<span data-ttu-id="22a5e-121">[**Coclass**](coclass.md)最多隻能有兩個 **\[ 預設 \]** 成員。</span><span class="sxs-lookup"><span data-stu-id="22a5e-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="22a5e-122">其中一個代表外寄 (來源) 介面或分配介面，另一個則代表傳入的 (接收) 介面或多介面。</span><span class="sxs-lookup"><span data-stu-id="22a5e-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="22a5e-123">如果未針對 **coclass** 或 **cotype** 的任何成員指定 **\[ \] 預設** 屬性，則會將未受限制屬性的第一個傳出和傳入成員 **\[** [](restricted.md) **\]** 視為預設值。</span><span class="sxs-lookup"><span data-stu-id="22a5e-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="22a5e-124">Flags</span><span class="sxs-lookup"><span data-stu-id="22a5e-124">Flags</span></span>

<span data-ttu-id="22a5e-125">IMPLTYPEFLAG \_ FDEFAULT</span><span class="sxs-lookup"><span data-stu-id="22a5e-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="22a5e-126">範例</span><span class="sxs-lookup"><span data-stu-id="22a5e-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="22a5e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22a5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a5e-128">**coclass**</span><span class="sxs-lookup"><span data-stu-id="22a5e-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="22a5e-129">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="22a5e-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="22a5e-130">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="22a5e-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="22a5e-131">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="22a5e-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="22a5e-132">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="22a5e-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="22a5e-133">**限制**</span><span class="sxs-lookup"><span data-stu-id="22a5e-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="22a5e-134">**源**</span><span class="sxs-lookup"><span data-stu-id="22a5e-134">**source**</span></span>](source.md)
</dt> </dl>

 

 