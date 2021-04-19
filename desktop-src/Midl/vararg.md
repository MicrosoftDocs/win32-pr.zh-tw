---
title: vararg 屬性
description: '\ Vararg \ 屬性指定函式接受不定數目的參數。 若要完成這項操作，最後一個參數必須是 VARIANT 型別的安全陣列，其中包含所有剩餘的參數。'
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- vararg 屬性 MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "107001079"
---
# <a name="vararg-attribute"></a><span data-ttu-id="70718-105">vararg 屬性</span><span class="sxs-lookup"><span data-stu-id="70718-105">vararg attribute</span></span>

<span data-ttu-id="70718-106">**\[ Vararg \]** 屬性指定函式接受不定數目的參數。</span><span class="sxs-lookup"><span data-stu-id="70718-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="70718-107">若要完成這項操作，最後一個參數必須是 **VARIANT** 型別的安全陣列，其中包含所有剩餘的參數。</span><span class="sxs-lookup"><span data-stu-id="70718-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="70718-108">參數</span><span class="sxs-lookup"><span data-stu-id="70718-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70718-109">*選用-屬性*</span><span class="sxs-lookup"><span data-stu-id="70718-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-110">指定要套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="70718-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="70718-111">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="70718-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="70718-112">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="70718-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-113">完成時遠端程式所傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="70718-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="70718-114">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="70718-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-115">遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="70718-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="70718-116">*選用-param-屬性*</span><span class="sxs-lookup"><span data-stu-id="70718-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-117">指定要在屬性清單之後立即套用至函數參數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="70718-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="70718-118">*param 清單*</span><span class="sxs-lookup"><span data-stu-id="70718-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-119">指定所有參數，並儲存最後的、變化的參數。</span><span class="sxs-lookup"><span data-stu-id="70718-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70718-120">*last-param 名稱*</span><span class="sxs-lookup"><span data-stu-id="70718-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="70718-121">不同參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="70718-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70718-122">備註</span><span class="sxs-lookup"><span data-stu-id="70718-122">Remarks</span></span>

<span data-ttu-id="70718-123">您無法將 **\[** [**選擇性**](optional.md) **\]** 或 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性套用至具有 **\[ \] vararg** 屬性之函式中的任何參數。</span><span class="sxs-lookup"><span data-stu-id="70718-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="70718-124">範例</span><span class="sxs-lookup"><span data-stu-id="70718-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="70718-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70718-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70718-126">**值**</span><span class="sxs-lookup"><span data-stu-id="70718-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="70718-127">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="70718-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="70718-128">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="70718-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="70718-129">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="70718-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="70718-130">**選**</span><span class="sxs-lookup"><span data-stu-id="70718-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 