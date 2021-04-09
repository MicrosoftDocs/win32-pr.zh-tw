---
title: helpcontext 屬性
description: '\ HelpcoNtext \ 屬性會指定內容識別碼，讓使用者可在說明檔中查看這個元素的相關資訊。'
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- helpcoNtext 屬性 MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933141"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="44da4-104">helpcontext 屬性</span><span class="sxs-lookup"><span data-stu-id="44da4-104">helpcontext attribute</span></span>

<span data-ttu-id="44da4-105">\[ **HelpcoNtext** \] 屬性會指定內容識別碼，讓使用者可在說明檔中查看此元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="44da4-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="44da4-106">參數</span><span class="sxs-lookup"><span data-stu-id="44da4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44da4-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="44da4-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-108">指定連結 [**庫**](library.md)、 \[ [**importlib**](importlib.md) \] 、[**介面**](interface.md)、介面 [**介面**](dispinterface.md)、[**模組**](module.md)、 [**typedef**](typedef.md)、**方法**、 **\[ \] 屬性** 或 [**coclass**](coclass.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="44da4-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="44da4-109">*helpcoNtext-值*</span><span class="sxs-lookup"><span data-stu-id="44da4-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-110">唯一的整數，識別與目前 MIDL 元素相關聯的解說文字。</span><span class="sxs-lookup"><span data-stu-id="44da4-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="44da4-111">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="44da4-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-112">指定一或多個套用至 MIDL 元素整體的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="44da4-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="44da4-113">*元素*</span><span class="sxs-lookup"><span data-stu-id="44da4-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-114">下列其中一個指示詞： [**library**](library.md)、 \[ [**importlib**](importlib.md) \] 、 [**interface**](interface.md)、 [\*\*\*\*](dispinterface.md)、 [**module、module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。</span><span class="sxs-lookup"><span data-stu-id="44da4-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="44da4-115">*元素名稱*</span><span class="sxs-lookup"><span data-stu-id="44da4-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-116">其他軟體元件可用來描繪目前元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="44da4-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="44da4-117">*定義*</span><span class="sxs-lookup"><span data-stu-id="44da4-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="44da4-118">指定組成元素定義的語句。</span><span class="sxs-lookup"><span data-stu-id="44da4-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44da4-119">備註</span><span class="sxs-lookup"><span data-stu-id="44da4-119">Remarks</span></span>

<span data-ttu-id="44da4-120">\[ **HelpcoNtext** \] 屬性可以套用至下列元素： [**library**](library.md)、 \[ [**importlib**](importlib.md) \] 、 [**interface、interface**](interface.md) [**、**](dispinterface.md) [**module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。</span><span class="sxs-lookup"><span data-stu-id="44da4-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="44da4-121">*HelpcoNtext-值* 是說明檔內的32位內容識別碼，可使用 [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib)和 [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)介面中的 [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation)函式進行抓取。</span><span class="sxs-lookup"><span data-stu-id="44da4-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="44da4-122">範例</span><span class="sxs-lookup"><span data-stu-id="44da4-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="44da4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44da4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44da4-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="44da4-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="44da4-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="44da4-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="44da4-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="44da4-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="44da4-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="44da4-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="44da4-128">**介面**</span><span class="sxs-lookup"><span data-stu-id="44da4-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="44da4-129">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="44da4-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="44da4-130">**模組**</span><span class="sxs-lookup"><span data-stu-id="44da4-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="44da4-131">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="44da4-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="44da4-132">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="44da4-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="44da4-133">**著**</span><span class="sxs-lookup"><span data-stu-id="44da4-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 