---
title: helpstringcoNtext 屬性
description: '\ HelpstringcoNtext \ 屬性指定說明檔中的32位說明內容識別碼。 您可以將 \ helpstringcoNtext \ 屬性套用至程式庫、介面、介面介面、模組、coclass、typedef 語句、屬性、參數和方法。'
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcoNtext 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966425"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="ae095-105">helpstringcoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="ae095-105">helpstringcontext attribute</span></span>

<span data-ttu-id="ae095-106">**\[ HelpstringcoNtext \]** 屬性會指定說明檔中的32位說明內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae095-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="ae095-107">您可以將 **\[ \] helpstringcoNtext** 屬性套用至連結 [**庫**](library.md)、[**介面**](interface.md)、介面 [**介面**](dispinterface.md)、[**模組**](module.md)、 [**coclass**](coclass.md)、 [**typedef**](typedef.md)語句、屬性、參數和方法。</span><span class="sxs-lookup"><span data-stu-id="ae095-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="ae095-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae095-109">*coNtextid*</span><span class="sxs-lookup"><span data-stu-id="ae095-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="ae095-110">唯一的整數，識別與目前 MIDL 語句相關聯的解說文字。</span><span class="sxs-lookup"><span data-stu-id="ae095-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="ae095-111">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="ae095-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ae095-112">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="ae095-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="ae095-113">*idl 語句*</span><span class="sxs-lookup"><span data-stu-id="ae095-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="ae095-114">將套用 **\[ helpstringcoNtext \]** 屬性的 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="ae095-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae095-115">備註</span><span class="sxs-lookup"><span data-stu-id="ae095-115">Remarks</span></span>

<span data-ttu-id="ae095-116">使用 **ITypeLib2** 和 **ITypeInfo2** 介面中的 **GetDocumentation2** 函式來取出說明字串。</span><span class="sxs-lookup"><span data-stu-id="ae095-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="ae095-117">範例</span><span class="sxs-lookup"><span data-stu-id="ae095-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




