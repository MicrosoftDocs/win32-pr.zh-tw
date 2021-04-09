---
title: helpstring 屬性
description: '\ Helpstring \ 屬性會指定用來描述所套用之元素的字元字串。'
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- helpstring 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933128"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="54b55-104">helpstring 屬性</span><span class="sxs-lookup"><span data-stu-id="54b55-104">helpstring attribute</span></span>

<span data-ttu-id="54b55-105">**\[ Helpstring \]** 屬性會指定用來描述所套用之元素的字元字串。</span><span class="sxs-lookup"><span data-stu-id="54b55-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="54b55-106">您可以將 **\[ helpstring \]** 屬性套用至程式庫、importlib、介面、介面介面、模組或 coclass 語句、typedef、屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="54b55-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="54b55-107">參數</span><span class="sxs-lookup"><span data-stu-id="54b55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b55-108">*說明-文字字串*</span><span class="sxs-lookup"><span data-stu-id="54b55-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-109">以零結束的字元字串，其中包含解說文字。</span><span class="sxs-lookup"><span data-stu-id="54b55-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="54b55-110">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="54b55-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-111">零或多個 MIDL 屬性語句。</span><span class="sxs-lookup"><span data-stu-id="54b55-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="54b55-112">*元素*</span><span class="sxs-lookup"><span data-stu-id="54b55-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-113">下列其中一個指示詞： [**library**](library.md)、 **\[** [**importlib**](importlib.md) **\]** 、 [**interface**](interface.md)、 [\*\*\*\*](dispinterface.md)、 [**module、module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。</span><span class="sxs-lookup"><span data-stu-id="54b55-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="54b55-114">*元素名稱*</span><span class="sxs-lookup"><span data-stu-id="54b55-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-115">其他軟體元件可用來描繪目前元素的名稱</span><span class="sxs-lookup"><span data-stu-id="54b55-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="54b55-116">*definition*</span><span class="sxs-lookup"><span data-stu-id="54b55-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-117">指定組成元素定義的語句。</span><span class="sxs-lookup"><span data-stu-id="54b55-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="54b55-118">*idl 語句*</span><span class="sxs-lookup"><span data-stu-id="54b55-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="54b55-119">MIDL 介面定義語句，例如 [**propget**](propget.md) 或 [**propput**](propput.md)。</span><span class="sxs-lookup"><span data-stu-id="54b55-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54b55-120">備註</span><span class="sxs-lookup"><span data-stu-id="54b55-120">Remarks</span></span>

<span data-ttu-id="54b55-121">使用 [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib)和 [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)介面中的 [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation)函式來取出說明字串。</span><span class="sxs-lookup"><span data-stu-id="54b55-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="54b55-122">範例</span><span class="sxs-lookup"><span data-stu-id="54b55-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="54b55-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54b55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b55-124">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="54b55-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="54b55-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="54b55-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="54b55-126">**介面**</span><span class="sxs-lookup"><span data-stu-id="54b55-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="54b55-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="54b55-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="54b55-128">**模組**</span><span class="sxs-lookup"><span data-stu-id="54b55-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="54b55-129">**coclass**</span><span class="sxs-lookup"><span data-stu-id="54b55-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="54b55-130">**著**</span><span class="sxs-lookup"><span data-stu-id="54b55-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="54b55-131">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="54b55-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="54b55-132">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="54b55-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="54b55-133">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="54b55-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 