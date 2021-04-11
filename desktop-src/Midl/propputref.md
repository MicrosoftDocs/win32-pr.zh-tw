---
title: propputref 屬性
description: '\ Propputref \ 屬性會指定使用參考而非值的屬性設定函數。'
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref 屬性 MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933115"
---
# <a name="propputref-attribute"></a><span data-ttu-id="a5c59-104">propputref 屬性</span><span class="sxs-lookup"><span data-stu-id="a5c59-104">propputref attribute</span></span>

<span data-ttu-id="a5c59-105">**\[ Propputref \]** 屬性會指定使用參考而非值的屬性設定函數。</span><span class="sxs-lookup"><span data-stu-id="a5c59-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="a5c59-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c59-107">*選用屬性-屬性*</span><span class="sxs-lookup"><span data-stu-id="a5c59-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c59-108">零或多個屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="a5c59-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a5c59-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="a5c59-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c59-110">遠端程式所傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a5c59-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a5c59-111">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a5c59-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c59-112">遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5c59-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a5c59-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="a5c59-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c59-114">遠端程式的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="a5c59-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5c59-115">備註</span><span class="sxs-lookup"><span data-stu-id="a5c59-115">Remarks</span></span>

<span data-ttu-id="a5c59-116">具有 **\[ propputref \]** 屬性的函式也必須具有（其最後一個參數）具有 **\[** [**in**](in.md)屬性（attribute）的指標 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a5c59-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="a5c59-117">屬性的名稱必須與函數相同。</span><span class="sxs-lookup"><span data-stu-id="a5c59-117">The property must have the same name as the function.</span></span> <span data-ttu-id="a5c59-118">最多可以為函式 **\[** [](propget.md) **\]** 指定 propget、 **\[** [**propput**](propput.md) **\]** 和 **\[ \] propputref** 屬性的其中一個。</span><span class="sxs-lookup"><span data-stu-id="a5c59-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="a5c59-119">Flags</span><span class="sxs-lookup"><span data-stu-id="a5c59-119">Flags</span></span>

<span data-ttu-id="a5c59-120">叫用 \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="a5c59-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="a5c59-121">範例</span><span class="sxs-lookup"><span data-stu-id="a5c59-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="a5c59-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5c59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c59-123">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a5c59-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a5c59-124">**在**</span><span class="sxs-lookup"><span data-stu-id="a5c59-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="a5c59-125">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="a5c59-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a5c59-126">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="a5c59-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a5c59-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="a5c59-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="a5c59-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="a5c59-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="a5c59-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a5c59-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 