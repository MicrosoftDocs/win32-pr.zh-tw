---
description: SWbemMethod 物件的 OutParameters 屬性是 SWbemObject 物件，其屬性定義了此方法的 out 參數和傳回型別。 這是唯讀的屬性。
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: 'SWbemMethod. OutParameters 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983732"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="5a4b2-104">SWbemMethod. OutParameters 屬性</span><span class="sxs-lookup"><span data-stu-id="5a4b2-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="5a4b2-105">[**SWbemMethod**](swbemmethod.md)物件的 **OutParameters** 屬性是 [**SWbemObject**](swbemobject.md)物件，其屬性定義了此方法的 out 參數和傳回型別。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="5a4b2-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-106">This property is read-only.</span></span>

<span data-ttu-id="5a4b2-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5a4b2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4b2-109">語法</span><span class="sxs-lookup"><span data-stu-id="5a4b2-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="5a4b2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5a4b2-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5a4b2-111">備註</span><span class="sxs-lookup"><span data-stu-id="5a4b2-111">Remarks</span></span>

<span data-ttu-id="5a4b2-112">如需如何使用這個屬性從提供者方法取得輸出參數的詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="5a4b2-113">請注意，對這個物件所做的任何變更都不會反映在基礎方法定義中。</span><span class="sxs-lookup"><span data-stu-id="5a4b2-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a4b2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a4b2-114">Requirements</span></span>



| <span data-ttu-id="5a4b2-115">需求</span><span class="sxs-lookup"><span data-stu-id="5a4b2-115">Requirement</span></span> | <span data-ttu-id="5a4b2-116">值</span><span class="sxs-lookup"><span data-stu-id="5a4b2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4b2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a4b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a4b2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a4b2-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a4b2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a4b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a4b2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a4b2-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a4b2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5a4b2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a4b2-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b2-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a4b2-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5a4b2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a4b2-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b2-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a4b2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5a4b2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a4b2-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b2-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a4b2-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="5a4b2-127">CLSID</span></span><br/>                    | <span data-ttu-id="5a4b2-128">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="5a4b2-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="5a4b2-129">IID</span><span class="sxs-lookup"><span data-stu-id="5a4b2-129">IID</span></span><br/>                      | <span data-ttu-id="5a4b2-130">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="5a4b2-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="5a4b2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a4b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4b2-132">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="5a4b2-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="5a4b2-133">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="5a4b2-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="5a4b2-134">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5a4b2-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="5a4b2-135">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="5a4b2-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="5a4b2-136">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="5a4b2-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




