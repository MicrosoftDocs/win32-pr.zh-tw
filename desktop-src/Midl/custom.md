---
title: Custom Attribute - 自訂屬性
description: '\ Custom \ 屬性會建立使用者定義的屬性。'
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- 自訂屬性 MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968691"
---
# <a name="custom-attribute"></a><span data-ttu-id="3406b-104">Custom Attribute - 自訂屬性</span><span class="sxs-lookup"><span data-stu-id="3406b-104">custom attribute</span></span>

<span data-ttu-id="3406b-105">**\[ 自訂 \]** 屬性會建立使用者定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="3406b-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="3406b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3406b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3406b-107">*屬性識別碼*</span><span class="sxs-lookup"><span data-stu-id="3406b-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="3406b-108">自訂屬性的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3406b-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3406b-109">*屬性-值*</span><span class="sxs-lookup"><span data-stu-id="3406b-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="3406b-110">屬性保存的值。</span><span class="sxs-lookup"><span data-stu-id="3406b-110">The value that the attribute holds.</span></span> <span data-ttu-id="3406b-111">值必須是可以放入 VARIANT 型別的一個值。</span><span class="sxs-lookup"><span data-stu-id="3406b-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="3406b-112">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="3406b-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3406b-113">適用于此元素的其他屬性，例如 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**helpstring**](helpstring.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="3406b-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="3406b-114">*元素類型*</span><span class="sxs-lookup"><span data-stu-id="3406b-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3406b-115">要套用自訂屬性的元素類型。</span><span class="sxs-lookup"><span data-stu-id="3406b-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="3406b-116">這可以是程式庫語句、類型資訊、變數、函數或參數。</span><span class="sxs-lookup"><span data-stu-id="3406b-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="3406b-117">您無法在 coclass 的成員上使用自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="3406b-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="3406b-118">*元素名稱*</span><span class="sxs-lookup"><span data-stu-id="3406b-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3406b-119">元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="3406b-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3406b-120">備註</span><span class="sxs-lookup"><span data-stu-id="3406b-120">Remarks</span></span>

<span data-ttu-id="3406b-121">使用 **\[ 自訂 \]** 屬性來定義您自己的屬性。</span><span class="sxs-lookup"><span data-stu-id="3406b-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="3406b-122">例如，您可以建立字串值屬性，以提供類別的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="3406b-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="3406b-123">若要取出自訂屬性值，請呼叫下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="3406b-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="3406b-124">ITypeLib2：： GetCustData (rguid，pvarVal) </span><span class="sxs-lookup"><span data-stu-id="3406b-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="3406b-125">ITypeInfo2：： GetCustData (rguid，pvarVal) </span><span class="sxs-lookup"><span data-stu-id="3406b-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="3406b-126">ITypeInfo2：： GetFuncCustData (index、rguid、pvarVal) </span><span class="sxs-lookup"><span data-stu-id="3406b-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="3406b-127">ITypeInfo2：： GetVarCustData (index、rguid、pvarval) </span><span class="sxs-lookup"><span data-stu-id="3406b-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="3406b-128">ITypeInfo2：： GetParamCustData (indexFunc、indexParam、rguid、pvarVal) </span><span class="sxs-lookup"><span data-stu-id="3406b-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="3406b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3406b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3406b-130">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3406b-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3406b-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="3406b-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="3406b-132">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="3406b-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="3406b-133">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="3406b-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3406b-134">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="3406b-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3406b-135">**uuid**</span><span class="sxs-lookup"><span data-stu-id="3406b-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 