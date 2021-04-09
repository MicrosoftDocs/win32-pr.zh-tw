---
title: nonbrowsable 屬性
description: 使用 \ nonbrowsable \ 屬性來標記不應該在屬性瀏覽器中顯示的介面或分配介面成員。
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- nonbrowsable 屬性 MIDL
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933137"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="9831e-104">nonbrowsable 屬性</span><span class="sxs-lookup"><span data-stu-id="9831e-104">nonbrowsable attribute</span></span>

<span data-ttu-id="9831e-105">使用 **\[ nonbrowsable \]** 屬性來標記不應該在屬性瀏覽器中顯示的介面或分配介面成員。</span><span class="sxs-lookup"><span data-stu-id="9831e-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="9831e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9831e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9831e-107">*屬性屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="9831e-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9831e-108">適用于屬性的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9831e-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="9831e-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="9831e-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="9831e-110">方法所傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="9831e-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="9831e-111">*屬性名稱*</span><span class="sxs-lookup"><span data-stu-id="9831e-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9831e-112">屬性或方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="9831e-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="9831e-113">*元件-param 清單*</span><span class="sxs-lookup"><span data-stu-id="9831e-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9831e-114">要傳遞給方法的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="9831e-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9831e-115">備註</span><span class="sxs-lookup"><span data-stu-id="9831e-115">Remarks</span></span>

<span data-ttu-id="9831e-116">某些屬性不應顯示在屬性瀏覽器中。</span><span class="sxs-lookup"><span data-stu-id="9831e-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="9831e-117">這可能是因為取出值會花費很長的時間。</span><span class="sxs-lookup"><span data-stu-id="9831e-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="9831e-118">此範例會防止使用者嘗試抓取 *Count* 屬性，此屬性會傳回動態集內的資料列數目。此數目可能代表非常大型查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="9831e-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="9831e-119">其他屬性可能會在瀏覽器上產生未預期的效果。</span><span class="sxs-lookup"><span data-stu-id="9831e-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="9831e-120">例如，請考慮具有屬性 "IsSelected" 的控制項，以分辨是否已選取控制項。</span><span class="sxs-lookup"><span data-stu-id="9831e-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="9831e-121">如果 "IsSelected" 設為 false，以選取專案為基礎的屬性瀏覽器會流覽不同的物件。</span><span class="sxs-lookup"><span data-stu-id="9831e-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="9831e-122">請注意，標記為 **\[ nonbrowsable \]** 的屬性仍會顯示在物件瀏覽器中，而不會顯示內容值。</span><span class="sxs-lookup"><span data-stu-id="9831e-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="9831e-123">Typeflag 標記法</span><span class="sxs-lookup"><span data-stu-id="9831e-123">Typeflag Representation</span></span>

<span data-ttu-id="9831e-124">FUNCFLAG \_ FNONBROWSABLE 或 VARFLAG FNONBROWSABLE 的存在 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9831e-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="9831e-125">範例</span><span class="sxs-lookup"><span data-stu-id="9831e-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="9831e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9831e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9831e-127">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="9831e-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9831e-128">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="9831e-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9831e-129">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9831e-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 