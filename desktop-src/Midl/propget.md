---
title: propget 屬性
description: '\ Propget \ 屬性會指定屬性存取子函數。 屬性的名稱必須與函數相同。'
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget 屬性 MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023320"
---
# <a name="propget-attribute"></a><span data-ttu-id="43412-105">propget 屬性</span><span class="sxs-lookup"><span data-stu-id="43412-105">propget attribute</span></span>

<span data-ttu-id="43412-106">**\[ Propget \]** 屬性會指定屬性存取子函數。</span><span class="sxs-lookup"><span data-stu-id="43412-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="43412-107">屬性的名稱必須與函數相同。</span><span class="sxs-lookup"><span data-stu-id="43412-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="43412-108">參數</span><span class="sxs-lookup"><span data-stu-id="43412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43412-109">*選用屬性-屬性*</span><span class="sxs-lookup"><span data-stu-id="43412-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="43412-110">零或多個屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="43412-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="43412-111">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="43412-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="43412-112">遠端程式所傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="43412-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="43412-113">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="43412-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="43412-114">遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="43412-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="43412-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="43412-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="43412-116">遠端程式的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="43412-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43412-117">備註</span><span class="sxs-lookup"><span data-stu-id="43412-117">Remarks</span></span>

<span data-ttu-id="43412-118">具有 propget 屬性（attribute）的函式也應該具有 **\[** [**out**](out-idl.md) **\]** 和 **\[** [**retval**](retval.md)屬性（property）做為指標類型的最後一個參數 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="43412-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="43412-119">如果最後一個參數沒有 \[ out、retval \] 屬性，則會將函式的傳回值視為 \[ out、retval \] 參數。</span><span class="sxs-lookup"><span data-stu-id="43412-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="43412-120">例如，具有原型的函式</span><span class="sxs-lookup"><span data-stu-id="43412-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="43412-121">被視為</span><span class="sxs-lookup"><span data-stu-id="43412-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="43412-122">最多可以為函式指定 **\[ \] propget**、 **\[** [**propput**](propput.md) **\]** 和 **\[** [**propputref**](propputref.md)其中一個 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="43412-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="43412-123">如果 lcid 屬性用於函式的參數清單中，而該函式 **\[** [](lcid.md) **\]** 包含具有 **\[** [**propput**](propput.md) **\]** 屬性的參數，則 **\[ lcid \]** 參數必須是最後一個的第二個。</span><span class="sxs-lookup"><span data-stu-id="43412-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="43412-124">Flags</span><span class="sxs-lookup"><span data-stu-id="43412-124">Flags</span></span>

<span data-ttu-id="43412-125">叫用 \_ PROPERTYGET</span><span class="sxs-lookup"><span data-stu-id="43412-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="43412-126">範例</span><span class="sxs-lookup"><span data-stu-id="43412-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="43412-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43412-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43412-128">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="43412-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="43412-129">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="43412-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="43412-130">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="43412-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="43412-131">**擴展**</span><span class="sxs-lookup"><span data-stu-id="43412-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="43412-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="43412-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="43412-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="43412-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="43412-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="43412-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="43412-135">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="43412-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 