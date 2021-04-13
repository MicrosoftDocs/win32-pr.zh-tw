---
title: id 屬性
description: '\ Id \ 屬性會指定成員函式的 DISPID (屬性或方法，在介面或) 的介面中。'
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- id 屬性 MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375032"
---
# <a name="id-attribute"></a><span data-ttu-id="17e4d-104">id 屬性</span><span class="sxs-lookup"><span data-stu-id="17e4d-104">id attribute</span></span>

<span data-ttu-id="17e4d-105">**\[ Id \]** 屬性會指定成員函式的 DISPID (屬性或方法，在介面或) 的介面中。</span><span class="sxs-lookup"><span data-stu-id="17e4d-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="17e4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="17e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e4d-107">*識別碼-num*</span><span class="sxs-lookup"><span data-stu-id="17e4d-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="17e4d-108">函數的 DISPID。</span><span class="sxs-lookup"><span data-stu-id="17e4d-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="17e4d-109">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="17e4d-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="17e4d-110">指定零個或更多 MIDL 介面屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="17e4d-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="17e4d-111">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="17e4d-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="17e4d-112">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="17e4d-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="17e4d-113">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="17e4d-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="17e4d-114">在 IDL 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="17e4d-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="17e4d-115">*選擇性-參數-清單*</span><span class="sxs-lookup"><span data-stu-id="17e4d-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="17e4d-116">零或多個函數參數。</span><span class="sxs-lookup"><span data-stu-id="17e4d-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17e4d-117">備註</span><span class="sxs-lookup"><span data-stu-id="17e4d-117">Remarks</span></span>

<span data-ttu-id="17e4d-118">當您想要指派標準 DISPID (例如 dispid **\[ \]** \_ 值、dispid \_ NEWENUM 等 ) 至方法或屬性，或當您執行您自己的 **IDispatch：： invoke** 而不是委派給 **DispInvoke** / **ITypeInfo：： invoke** 時，請使用 id 屬性。</span><span class="sxs-lookup"><span data-stu-id="17e4d-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="17e4d-119">如果您未在介面上使用 **\[ id \]** 屬性，MIDL 編譯器將為您指派 DISPID。</span><span class="sxs-lookup"><span data-stu-id="17e4d-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="17e4d-120">但是，當您使用屬性和方法來指定分配介面時，您必須針對每個屬性和方法指定 DISPID。</span><span class="sxs-lookup"><span data-stu-id="17e4d-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="17e4d-121">*識別碼-num* 是32位的正整數值。</span><span class="sxs-lookup"><span data-stu-id="17e4d-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="17e4d-122">負的識別碼是保留供 Automation 使用。</span><span class="sxs-lookup"><span data-stu-id="17e4d-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="17e4d-123">範例</span><span class="sxs-lookup"><span data-stu-id="17e4d-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="17e4d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17e4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e4d-125">**介面**</span><span class="sxs-lookup"><span data-stu-id="17e4d-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="17e4d-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="17e4d-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="17e4d-127">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="17e4d-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="17e4d-128">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="17e4d-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="17e4d-129">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17e4d-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 