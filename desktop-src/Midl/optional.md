---
title: optional 屬性
description: '\ Optional \ 屬性指定成員函式的選擇性參數。'
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- 選擇性屬性 MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842263"
---
# <a name="optional-attribute"></a><span data-ttu-id="7dc23-104">optional 屬性</span><span class="sxs-lookup"><span data-stu-id="7dc23-104">optional attribute</span></span>

<span data-ttu-id="7dc23-105">**\[ 選擇性 \]** 屬性會指定成員函式的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="7dc23-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="7dc23-106">參數</span><span class="sxs-lookup"><span data-stu-id="7dc23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc23-107">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="7dc23-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc23-108">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="7dc23-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7dc23-109">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="7dc23-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc23-110">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc23-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7dc23-111">*其他屬性*</span><span class="sxs-lookup"><span data-stu-id="7dc23-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc23-112">零或多個選擇性 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="7dc23-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7dc23-113">*參數類型*</span><span class="sxs-lookup"><span data-stu-id="7dc23-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc23-114">選用參數的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7dc23-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7dc23-115">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="7dc23-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc23-116">指定選擇性參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc23-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7dc23-117">備註</span><span class="sxs-lookup"><span data-stu-id="7dc23-117">Remarks</span></span>

<span data-ttu-id="7dc23-118">只有當參數的類型為 **variant** 或 **variant** 時， **\[ \] 選擇性** 的屬性才有效 \* 。</span><span class="sxs-lookup"><span data-stu-id="7dc23-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="7dc23-119">MIDL 編譯器接受下列參數排序 (從左至右) ：</span><span class="sxs-lookup"><span data-stu-id="7dc23-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="7dc23-120">必要參數 (沒有 **\[** [**defaultvalue**](defaultvalue.md) **\]** 或 **\[ 選擇性 \]** 屬性的參數) ，</span><span class="sxs-lookup"><span data-stu-id="7dc23-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="7dc23-121">具有或不具有 **\[** [**defaultvalue**](defaultvalue.md)屬性的選擇性參數 **\]** ，</span><span class="sxs-lookup"><span data-stu-id="7dc23-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="7dc23-122">具有 **\[ 選擇性 \]** 屬性且不含 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="7dc23-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="7dc23-123">**\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="7dc23-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="7dc23-124">**\[**[**retval**](retval.md) **\]** 參數</span><span class="sxs-lookup"><span data-stu-id="7dc23-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="7dc23-125">您無法將 **\[ 選擇性 \]** 屬性套用至也有 **\[** [**lcid**](lcid.md) **\]** 或 **\[** [**retval**](retval.md) **\]** 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="7dc23-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="7dc23-126">範例</span><span class="sxs-lookup"><span data-stu-id="7dc23-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="7dc23-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dc23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc23-128">**值**</span><span class="sxs-lookup"><span data-stu-id="7dc23-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="7dc23-129">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7dc23-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7dc23-130">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="7dc23-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="7dc23-131">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="7dc23-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7dc23-132">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="7dc23-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7dc23-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="7dc23-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 