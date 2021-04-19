---
title: hidden 屬性
description: '\ Hidden \ 屬性工作表示專案存在，但不應該在使用者導向的瀏覽器中顯示。'
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- hidden 屬性 MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968898"
---
# <a name="hidden-attribute"></a><span data-ttu-id="1ae14-104">hidden 屬性</span><span class="sxs-lookup"><span data-stu-id="1ae14-104">hidden attribute</span></span>

<span data-ttu-id="1ae14-105">**\[ Hidden \]** 屬性工作表示專案存在，但不應該在使用者導向的瀏覽器中顯示。</span><span class="sxs-lookup"><span data-stu-id="1ae14-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="1ae14-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ae14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae14-107">*其他屬性*</span><span class="sxs-lookup"><span data-stu-id="1ae14-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-108">零或多個選擇性 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="1ae14-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-109">*元素*</span><span class="sxs-lookup"><span data-stu-id="1ae14-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-110">下列其中一個指示詞： [**coclass**](coclass.md)、 [**介面**](dispinterface.md)、 [**介面**](interface.md)或連結 [**庫**](library.md)。</span><span class="sxs-lookup"><span data-stu-id="1ae14-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-111">*元素名稱*</span><span class="sxs-lookup"><span data-stu-id="1ae14-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-112">其他軟體元件可用來描繪目前元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae14-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-113">*定義*</span><span class="sxs-lookup"><span data-stu-id="1ae14-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-114">指定組成元素定義的語句。</span><span class="sxs-lookup"><span data-stu-id="1ae14-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-115">*函數類型*</span><span class="sxs-lookup"><span data-stu-id="1ae14-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-116">函數的傳回類型。</span><span class="sxs-lookup"><span data-stu-id="1ae14-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-117">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="1ae14-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-118">用來叫用函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae14-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="1ae14-119">*選擇性-參數-清單*</span><span class="sxs-lookup"><span data-stu-id="1ae14-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae14-120">零或多個函數參數。</span><span class="sxs-lookup"><span data-stu-id="1ae14-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ae14-121">備註</span><span class="sxs-lookup"><span data-stu-id="1ae14-121">Remarks</span></span>

<span data-ttu-id="1ae14-122">**\[ Hidden \]** 屬性可讓您從介面 (移除成員，方法是將其防護以進一步使用) ，同時維持與現有程式碼的相容性。</span><span class="sxs-lookup"><span data-stu-id="1ae14-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="1ae14-123">您可以對屬性、方法和 [**coclass**](coclass.md) [**、**](dispinterface.md)介面、[**介面**](interface.md)和連結 [**庫**](library.md)語句使用 **\[ hidden \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1ae14-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="1ae14-124">針對程式庫指定時， **\[ 隱藏 \]** 的屬性會防止整個程式庫顯示。</span><span class="sxs-lookup"><span data-stu-id="1ae14-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="1ae14-125">此用法是與控制項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1ae14-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="1ae14-126">主機需要建立新的類型程式庫，以包裝控制項與擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="1ae14-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="1ae14-127">Flags</span><span class="sxs-lookup"><span data-stu-id="1ae14-127">Flags</span></span>

<span data-ttu-id="1ae14-128">VARFLAG \_ FHIDDEN、FUNCFLAG \_ FHIDDEN、TYPEFLAG \_ FHIDDEN</span><span class="sxs-lookup"><span data-stu-id="1ae14-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="1ae14-129">範例</span><span class="sxs-lookup"><span data-stu-id="1ae14-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="1ae14-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ae14-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae14-131">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="1ae14-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="1ae14-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="1ae14-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="1ae14-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="1ae14-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="1ae14-134">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1ae14-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1ae14-135">**介面**</span><span class="sxs-lookup"><span data-stu-id="1ae14-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="1ae14-136">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="1ae14-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="1ae14-137">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="1ae14-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1ae14-138">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="1ae14-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 