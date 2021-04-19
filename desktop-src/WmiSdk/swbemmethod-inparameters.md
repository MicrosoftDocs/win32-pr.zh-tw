---
description: SWbemMethod 物件的 InParameters 屬性是 SWbemObject 物件，其屬性會定義此方法的輸入參數。
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: 'SWbemMethod. InParameters 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8df897f876673f6b4afe875e718401ae4c217e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977234"
---
# <a name="swbemmethodinparameters-property"></a><span data-ttu-id="ae739-103">SWbemMethod. InParameters 屬性</span><span class="sxs-lookup"><span data-stu-id="ae739-103">SWbemMethod.InParameters property</span></span>

<span data-ttu-id="ae739-104">[**SWbemMethod**](swbemmethod.md)物件的 **InParameters** 屬性是 [**SWbemObject**](swbemobject.md)物件，其屬性會定義此方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ae739-104">The **InParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span> <span data-ttu-id="ae739-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae739-105">This property is read-only.</span></span> <span data-ttu-id="ae739-106">請注意，對這個物件所做的任何變更都不會反映在基礎方法定義中。</span><span class="sxs-lookup"><span data-stu-id="ae739-106">Note that any changes that are made to this object are not reflected in the underlying method definition.</span></span>

<span data-ttu-id="ae739-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ae739-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ae739-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ae739-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae739-109">語法</span><span class="sxs-lookup"><span data-stu-id="ae739-109">Syntax</span></span>


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="ae739-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ae739-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ae739-111">備註</span><span class="sxs-lookup"><span data-stu-id="ae739-111">Remarks</span></span>

<span data-ttu-id="ae739-112">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ae739-112">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae739-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae739-113">Requirements</span></span>



| <span data-ttu-id="ae739-114">需求</span><span class="sxs-lookup"><span data-stu-id="ae739-114">Requirement</span></span> | <span data-ttu-id="ae739-115">值</span><span class="sxs-lookup"><span data-stu-id="ae739-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae739-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae739-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae739-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae739-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae739-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae739-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae739-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae739-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae739-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ae739-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae739-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae739-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae739-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ae739-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae739-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae739-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae739-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ae739-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae739-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae739-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae739-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae739-126">CLSID</span></span><br/>                    | <span data-ttu-id="ae739-127">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="ae739-127">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="ae739-128">IID</span><span class="sxs-lookup"><span data-stu-id="ae739-128">IID</span></span><br/>                      | <span data-ttu-id="ae739-129">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="ae739-129">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ae739-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae739-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae739-131">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="ae739-131">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="ae739-132">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="ae739-132">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="ae739-133">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ae739-133">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="ae739-134">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="ae739-134">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="ae739-135">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="ae739-135">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




