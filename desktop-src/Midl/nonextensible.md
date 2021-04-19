---
title: nonextensible 屬性
description: '\ Nonextensible \ 屬性指定 IDispatch 的實作為只包含介面描述中所列的屬性和方法，而且無法在執行時間以其他成員擴充。'
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nonextensible 屬性 MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965837"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="e304f-104">nonextensible 屬性</span><span class="sxs-lookup"><span data-stu-id="e304f-104">nonextensible attribute</span></span>

<span data-ttu-id="e304f-105">**\[ Nonextensible \]** 屬性會指定 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)執行只包含介面描述中所列出的屬性和方法，而且在執行時間無法以其他成員擴充。</span><span class="sxs-lookup"><span data-stu-id="e304f-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="e304f-106"> (根據預設，自動化會假設介面可能會在執行時間加入成員;也就是說，它會假設它們是可擴充的。 ) </span><span class="sxs-lookup"><span data-stu-id="e304f-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="e304f-107">參數</span><span class="sxs-lookup"><span data-stu-id="e304f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e304f-108">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="e304f-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="e304f-109">指定 [**介面**](interface.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e304f-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e304f-110">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="e304f-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e304f-111">指定零個或更多 MIDL 介面屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="e304f-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="e304f-112">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="e304f-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e304f-113">指定 [**介面**](interface.md)[**或分配介面的**](dispinterface.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="e304f-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e304f-114">*介面定義*</span><span class="sxs-lookup"><span data-stu-id="e304f-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="e304f-115">指定組成介面 [**或分配**](dispinterface.md)[**介面**](interface.md)定義的 IDL 語句。</span><span class="sxs-lookup"><span data-stu-id="e304f-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e304f-116">備註</span><span class="sxs-lookup"><span data-stu-id="e304f-116">Remarks</span></span>

<span data-ttu-id="e304f-117">您可以將 **\[ nonextensible \]** 屬性套用至介面或介面介面。</span><span class="sxs-lookup"><span data-stu-id="e304f-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="e304f-118">不過，介面也必須有 **\[** [**雙重**](dual.md) **\]** 屬性和 **\[** [**oleautomation**](oleautomation.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e304f-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="e304f-119">Flags</span><span class="sxs-lookup"><span data-stu-id="e304f-119">Flags</span></span>

<span data-ttu-id="e304f-120">TYPEFLAG \_ FNONEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="e304f-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="e304f-121">範例</span><span class="sxs-lookup"><span data-stu-id="e304f-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e304f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e304f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e304f-123">型別程式庫的內容</span><span class="sxs-lookup"><span data-stu-id="e304f-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="e304f-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="e304f-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="e304f-125">**雙**</span><span class="sxs-lookup"><span data-stu-id="e304f-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="e304f-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e304f-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e304f-127">**介面**</span><span class="sxs-lookup"><span data-stu-id="e304f-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e304f-128">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="e304f-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e304f-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="e304f-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="e304f-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="e304f-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 