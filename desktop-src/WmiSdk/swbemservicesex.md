---
description: 擴充 SWbemServices 的功能。
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: 'SWbemServicesEx 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114856"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="e1551-103">SWbemServicesEx 物件</span><span class="sxs-lookup"><span data-stu-id="e1551-103">SWbemServicesEx object</span></span>

<span data-ttu-id="e1551-104">**SWbemServicesEx** 物件會擴充 [**SWbemServices**](swbemservices.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="e1551-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="e1551-105">[**Put**](swbemservicesex-put.md)和 [**PutAsync**](swbemservicesex-putasync.md)方法可讓您將類別或實例儲存至多個命名空間，或儲存至與建立實例的命名空間不同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e1551-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="e1551-106">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="e1551-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="e1551-107">成員</span><span class="sxs-lookup"><span data-stu-id="e1551-107">Members</span></span>

<span data-ttu-id="e1551-108">**SWbemServicesEx** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e1551-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="e1551-109">方法</span><span class="sxs-lookup"><span data-stu-id="e1551-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1551-110">方法</span><span class="sxs-lookup"><span data-stu-id="e1551-110">Methods</span></span>

<span data-ttu-id="e1551-111">**SWbemServicesEx** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e1551-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="e1551-112">方法</span><span class="sxs-lookup"><span data-stu-id="e1551-112">Method</span></span>                                       | <span data-ttu-id="e1551-113">描述</span><span class="sxs-lookup"><span data-stu-id="e1551-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1551-114">**把**</span><span class="sxs-lookup"><span data-stu-id="e1551-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="e1551-115">將物件儲存至系結至 **SWbemServicesEx** 物件的命名空間，並傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其中包含寫入資料的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="e1551-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="e1551-116">**PutAsync**</span><span class="sxs-lookup"><span data-stu-id="e1551-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="e1551-117">以非同步方式將物件儲存到命名空間。</span><span class="sxs-lookup"><span data-stu-id="e1551-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="e1551-118">備註</span><span class="sxs-lookup"><span data-stu-id="e1551-118">Remarks</span></span>

<span data-ttu-id="e1551-119">此類別中的方法可以在半同步模式或非同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="e1551-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="e1551-120">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e1551-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1551-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1551-121">Requirements</span></span>



| <span data-ttu-id="e1551-122">需求</span><span class="sxs-lookup"><span data-stu-id="e1551-122">Requirement</span></span> | <span data-ttu-id="e1551-123">值</span><span class="sxs-lookup"><span data-stu-id="e1551-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1551-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1551-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e1551-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1551-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1551-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1551-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e1551-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1551-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1551-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e1551-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1551-129"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1551-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1551-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e1551-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1551-131"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e1551-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e1551-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e1551-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1551-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1551-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1551-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1551-134">CLSID</span></span><br/>                    | <span data-ttu-id="e1551-135">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="e1551-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="e1551-136">IID</span><span class="sxs-lookup"><span data-stu-id="e1551-136">IID</span></span><br/>                      | <span data-ttu-id="e1551-137">IID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="e1551-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="e1551-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1551-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1551-139">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="e1551-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="e1551-140">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="e1551-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

