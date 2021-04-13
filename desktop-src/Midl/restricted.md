---
title: restricted 屬性
description: '\ 限制 \ 屬性指定無法任意呼叫模組、介面或分配介面的程式庫或成員。'
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- 受限制的屬性 MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375181"
---
# <a name="restricted-attribute"></a><span data-ttu-id="72b19-104">restricted 屬性</span><span class="sxs-lookup"><span data-stu-id="72b19-104">restricted attribute</span></span>

<span data-ttu-id="72b19-105">**\[ 受限制 \]** 的屬性會指定無法任意呼叫程式庫或模組、介面或分配介面的成員。</span><span class="sxs-lookup"><span data-stu-id="72b19-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="72b19-106">參數</span><span class="sxs-lookup"><span data-stu-id="72b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b19-107">*其他屬性*</span><span class="sxs-lookup"><span data-stu-id="72b19-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="72b19-108">零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="72b19-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="72b19-109">*語句類型*</span><span class="sxs-lookup"><span data-stu-id="72b19-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="72b19-110">下列其中一項：連結 [**庫**](library.md)、[**模組**](module.md)、[**介面、介面**](interface.md)介面。 [](dispinterface.md)</span><span class="sxs-lookup"><span data-stu-id="72b19-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="72b19-111">*語句-名稱*</span><span class="sxs-lookup"><span data-stu-id="72b19-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="72b19-112">軟體用來參考這個語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="72b19-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="72b19-113">*定義*</span><span class="sxs-lookup"><span data-stu-id="72b19-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="72b19-114">用來定義這個語句內容的 MIDL 語言元素。</span><span class="sxs-lookup"><span data-stu-id="72b19-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72b19-115">備註</span><span class="sxs-lookup"><span data-stu-id="72b19-115">Remarks</span></span>

<span data-ttu-id="72b19-116">這個屬性可讓您控制對介面、程式庫、模組和分配介面之元素的存取。</span><span class="sxs-lookup"><span data-stu-id="72b19-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="72b19-117">例如，它可以防止宏程式設計人員使用資料項目。</span><span class="sxs-lookup"><span data-stu-id="72b19-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="72b19-118">您可以將此屬性套用至 [**coclass**](coclass.md)的成員，與成員是否為分配介面或介面無關，而不論成員是否為接收 (傳入) 或來源 (傳出) 。</span><span class="sxs-lookup"><span data-stu-id="72b19-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="72b19-119">**Coclass** 的成員不能同時有 **\[ 受 \] 限制** 的和 **\[ 預設 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="72b19-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="72b19-120">Flags</span><span class="sxs-lookup"><span data-stu-id="72b19-120">Flags</span></span>

<span data-ttu-id="72b19-121">IMPLTYPEFLAG \_ FRESTRICTED、FUNCFLAG \_ FRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="72b19-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="72b19-122">範例</span><span class="sxs-lookup"><span data-stu-id="72b19-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="72b19-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72b19-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b19-124">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="72b19-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="72b19-125">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="72b19-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="72b19-126">**介面**</span><span class="sxs-lookup"><span data-stu-id="72b19-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="72b19-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="72b19-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="72b19-128">**模組**</span><span class="sxs-lookup"><span data-stu-id="72b19-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="72b19-129">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="72b19-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="72b19-130">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="72b19-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="72b19-131">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="72b19-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 