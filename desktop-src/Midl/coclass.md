---
title: coclass 屬性
description: Coclass 語句會提供元件物件支援的介面清單。
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- coclass 屬性 MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375185"
---
# <a name="coclass-attribute"></a><span data-ttu-id="37a78-104">coclass 屬性</span><span class="sxs-lookup"><span data-stu-id="37a78-104">coclass attribute</span></span>

<span data-ttu-id="37a78-105">**Coclass** 語句會提供元件物件支援的介面清單。</span><span class="sxs-lookup"><span data-stu-id="37a78-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="37a78-106">參數</span><span class="sxs-lookup"><span data-stu-id="37a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a78-107">*coclass-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="37a78-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="37a78-108">**\[** [](uuid.md) **\]** **Coclass** 上需要有 uuid 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a78-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="37a78-109">這是在系統註冊資料庫中註冊為 CLSID 的相同 **\[ uuid \]** 。</span><span class="sxs-lookup"><span data-stu-id="37a78-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="37a78-110">在 **\[** [](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** coclass 定義之前，會接受 helpstring、helpcoNtext、 **\[** [**授權**](licensed.md) **\]** 、 **\[** [**version**](version.md) **\]** 、 **\[** [**control**](control.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 和 **\[** [**appobject**](appobject.md) **\]** 屬性（但非必要 ）。</span><span class="sxs-lookup"><span data-stu-id="37a78-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="37a78-111">*classname*</span><span class="sxs-lookup"><span data-stu-id="37a78-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="37a78-112">類型程式庫中已知通用物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="37a78-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="37a78-113">*介面屬性*</span><span class="sxs-lookup"><span data-stu-id="37a78-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="37a78-114">介面或分配介面的選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="37a78-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="37a78-115">在 **\[** [](source.md) **\]** **\[** [](default.md) **\]** coclass 中的介面或介面介面上接受來源、預設和 **\[** [**受限制**](restricted.md) **\]** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="37a78-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="37a78-116">*介面名稱*</span><span class="sxs-lookup"><span data-stu-id="37a78-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="37a78-117">使用 [**interface**](interface.md) 關鍵字宣告的介面，或以產生 [**介面關鍵字宣告**](dispinterface.md) 的介面介面。</span><span class="sxs-lookup"><span data-stu-id="37a78-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37a78-118">備註</span><span class="sxs-lookup"><span data-stu-id="37a78-118">Remarks</span></span>

<span data-ttu-id="37a78-119">Microsoft 元件物件模型會將類別定義為可讓一組介面之間進行 **QueryInterface** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="37a78-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="37a78-120">範例</span><span class="sxs-lookup"><span data-stu-id="37a78-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="37a78-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37a78-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a78-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="37a78-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="37a78-123">**控制**</span><span class="sxs-lookup"><span data-stu-id="37a78-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="37a78-124">**預設**</span><span class="sxs-lookup"><span data-stu-id="37a78-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="37a78-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="37a78-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="37a78-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="37a78-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="37a78-127">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="37a78-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="37a78-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="37a78-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="37a78-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="37a78-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="37a78-130">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="37a78-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="37a78-131">**介面**</span><span class="sxs-lookup"><span data-stu-id="37a78-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="37a78-132">**licensed**</span><span class="sxs-lookup"><span data-stu-id="37a78-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="37a78-133">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="37a78-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="37a78-134">**限制**</span><span class="sxs-lookup"><span data-stu-id="37a78-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="37a78-135">**源**</span><span class="sxs-lookup"><span data-stu-id="37a78-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="37a78-136">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="37a78-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="37a78-137">**uuid**</span><span class="sxs-lookup"><span data-stu-id="37a78-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="37a78-138">**版本**</span><span class="sxs-lookup"><span data-stu-id="37a78-138">**version**</span></span>](version.md)
</dt> </dl>

 

 