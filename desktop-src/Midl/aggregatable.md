---
title: aggregatable 屬性
description: '\ 聚合 \ 屬性工作表示類別支援匯總。'
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- 聚合屬性 MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314842"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="dd6fc-104">aggregatable 屬性</span><span class="sxs-lookup"><span data-stu-id="dd6fc-104">aggregatable attribute</span></span>

<span data-ttu-id="dd6fc-105">匯總屬性指出類別支援匯總。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="dd6fc-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="dd6fc-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd6fc-107">*coclass-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="dd6fc-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dd6fc-108">適用于類別的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="dd6fc-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="dd6fc-109">*coclass-名稱*</span><span class="sxs-lookup"><span data-stu-id="dd6fc-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd6fc-110">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd6fc-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="dd6fc-111">*coclass-介面清單*</span><span class="sxs-lookup"><span data-stu-id="dd6fc-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dd6fc-112">類別的介面清單。</span><span class="sxs-lookup"><span data-stu-id="dd6fc-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd6fc-113">備註</span><span class="sxs-lookup"><span data-stu-id="dd6fc-113">Remarks</span></span>

<span data-ttu-id="dd6fc-114">在 [**coclass**](coclass.md)語句上使用可匯總屬性，讓使用者知道類別支援匯總。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="dd6fc-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="dd6fc-115">也就是說，類別可讓容器類別公開其介面，如同這些介面是容器本身的介面。</span><span class="sxs-lookup"><span data-stu-id="dd6fc-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="dd6fc-116">這個屬性的 typeflag 標記法為 TYPEFLAG \_ FAGGREGATABLE。</span><span class="sxs-lookup"><span data-stu-id="dd6fc-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="dd6fc-117">範例</span><span class="sxs-lookup"><span data-stu-id="dd6fc-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="dd6fc-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd6fc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6fc-119">**coclass**</span><span class="sxs-lookup"><span data-stu-id="dd6fc-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="dd6fc-120">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dd6fc-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="dd6fc-121">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="dd6fc-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dd6fc-122">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="dd6fc-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 