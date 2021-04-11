---
title: propput 屬性
description: '\ Propput \ 屬性指定屬性設定函數。 屬性的名稱必須與函數相同。'
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput 屬性 MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092662"
---
# <a name="propput-attribute"></a><span data-ttu-id="8de52-105">propput 屬性</span><span class="sxs-lookup"><span data-stu-id="8de52-105">propput attribute</span></span>

<span data-ttu-id="8de52-106">**\[ Propput \]** 屬性會指定屬性設定函數。</span><span class="sxs-lookup"><span data-stu-id="8de52-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="8de52-107">屬性的名稱必須與函數相同 *。*</span><span class="sxs-lookup"><span data-stu-id="8de52-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="8de52-108">參數</span><span class="sxs-lookup"><span data-stu-id="8de52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de52-109">*選用屬性-屬性*</span><span class="sxs-lookup"><span data-stu-id="8de52-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="8de52-110">零或多個屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="8de52-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="8de52-111">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="8de52-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8de52-112">遠端程式所傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="8de52-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="8de52-113">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="8de52-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8de52-114">遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8de52-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="8de52-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="8de52-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="8de52-116">遠端程式的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="8de52-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8de52-117">備註</span><span class="sxs-lookup"><span data-stu-id="8de52-117">Remarks</span></span>

<span data-ttu-id="8de52-118">具有 **\[ propput \]** 屬性的函式也必須具有（其最後一個參數）具有 **\[** [**in**](in.md) **\]** 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="8de52-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="8de52-119">最多可以為函式 **\[** 指定 [**propget**](propget.md) **\]** 、 **\[ \] propput** 和 **\[** [**propputref**](propputref.md) **\]** 其中一個。</span><span class="sxs-lookup"><span data-stu-id="8de52-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="8de52-120">如果 lcid 屬性用於函式的參數清單中，而該函式 **\[** [](lcid.md) **\]** 包含具有 **\[ propput \]** 屬性的參數，則 **\[ lcid \]** 參數必須是最後一個的第二個。</span><span class="sxs-lookup"><span data-stu-id="8de52-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="8de52-121">Flags</span><span class="sxs-lookup"><span data-stu-id="8de52-121">Flags</span></span>

<span data-ttu-id="8de52-122">叫用 \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="8de52-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="8de52-123">範例</span><span class="sxs-lookup"><span data-stu-id="8de52-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="8de52-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8de52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de52-125">MIDL 與 MKTYPLIB.EXE 之間的差異</span><span class="sxs-lookup"><span data-stu-id="8de52-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="8de52-126">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="8de52-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8de52-127">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="8de52-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8de52-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="8de52-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="8de52-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="8de52-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="8de52-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="8de52-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 