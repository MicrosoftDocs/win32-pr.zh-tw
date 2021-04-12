---
title: defaultvalue 屬性
description: '\ Defaultvalue \ 屬性可讓您指定具類型選擇性參數的預設值。'
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- defaultvalue 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314980"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="1ea77-104">defaultvalue 屬性</span><span class="sxs-lookup"><span data-stu-id="1ea77-104">defaultvalue attribute</span></span>

<span data-ttu-id="1ea77-105">**\[ Defaultvalue \]** 屬性可讓您指定具類型選擇性參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="1ea77-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="1ea77-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ea77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea77-107">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="1ea77-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-108">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ea77-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="1ea77-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-110">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="1ea77-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-111">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="1ea77-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-112">指定將套用 **\[ defaultvalue \]** 屬性的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="1ea77-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-113">*強制-param 清單*</span><span class="sxs-lookup"><span data-stu-id="1ea77-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-114">指定一或多個必要參數。</span><span class="sxs-lookup"><span data-stu-id="1ea77-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-115">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="1ea77-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-116">指定適用于參數的一或多個屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="1ea77-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-117">*param 類型*</span><span class="sxs-lookup"><span data-stu-id="1ea77-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-118">指出選用參數的類型。</span><span class="sxs-lookup"><span data-stu-id="1ea77-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-119">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="1ea77-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-120">指定選擇性參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ea77-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1ea77-121">*選用-param 清單*</span><span class="sxs-lookup"><span data-stu-id="1ea77-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea77-122">指定零個或多個額外的參數，每個參數都必須有預設值。</span><span class="sxs-lookup"><span data-stu-id="1ea77-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ea77-123">備註</span><span class="sxs-lookup"><span data-stu-id="1ea77-123">Remarks</span></span>

<span data-ttu-id="1ea77-124">您為參數指定的預設值可以是任何常數，也可以是解析成常數的運算式（可由 **VARIANT** 表示）。</span><span class="sxs-lookup"><span data-stu-id="1ea77-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="1ea77-125">具體而言，您無法將 **\[ defaultvalue \]** 屬性套用至屬於結構、陣列或 **SAFEARRAY** 類型的參數。</span><span class="sxs-lookup"><span data-stu-id="1ea77-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="1ea77-126">MIDL 編譯器接受下列參數排序 (從左至右) ：</span><span class="sxs-lookup"><span data-stu-id="1ea77-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="1ea77-127">必要參數 (沒有 **\[ \] defaultvalue** 或 **\[** [**選擇性**](optional.md) **\]** 屬性的參數) ，</span><span class="sxs-lookup"><span data-stu-id="1ea77-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="1ea77-128">具有或不具有 **\[ defaultvalue \]** 屬性的選擇性參數，</span><span class="sxs-lookup"><span data-stu-id="1ea77-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="1ea77-129">具有 **\[ 選擇性 \]** 屬性且不含 **\[ defaultvalue \]** 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="1ea77-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="1ea77-130">**\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="1ea77-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="1ea77-131">**\[**[**retval**](retval.md) **\]** 參數</span><span class="sxs-lookup"><span data-stu-id="1ea77-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="1ea77-132">範例</span><span class="sxs-lookup"><span data-stu-id="1ea77-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="1ea77-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ea77-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea77-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="1ea77-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="1ea77-135">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1ea77-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1ea77-136">**介面**</span><span class="sxs-lookup"><span data-stu-id="1ea77-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="1ea77-137">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="1ea77-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="1ea77-138">**選**</span><span class="sxs-lookup"><span data-stu-id="1ea77-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="1ea77-139">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="1ea77-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1ea77-140">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="1ea77-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1ea77-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="1ea77-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="1ea77-142">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="1ea77-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 