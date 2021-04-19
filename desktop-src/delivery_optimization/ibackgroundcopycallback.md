---
title: 'IBackgroundCopyCallback 介面 (>deliveryoptimization .h) '
description: 執行 IBackgroundCopyCallback 介面，以接收作業已完成、已修改或發生錯誤的通知。 用戶端會使用此介面，而不是輪詢作業的狀態。
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968758"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="73f73-106">IBackgroundCopyCallback 介面</span><span class="sxs-lookup"><span data-stu-id="73f73-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="73f73-107">執行 **IBackgroundCopyCallback** 介面，以接收作業已完成、已修改或發生錯誤的通知。</span><span class="sxs-lookup"><span data-stu-id="73f73-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="73f73-108">用戶端會使用此介面，而不是輪詢作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="73f73-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="73f73-109">成員</span><span class="sxs-lookup"><span data-stu-id="73f73-109">Members</span></span>

<span data-ttu-id="73f73-110">**IBackgroundCopyCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="73f73-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73f73-111">**IBackgroundCopyCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="73f73-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="73f73-112">方法</span><span class="sxs-lookup"><span data-stu-id="73f73-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73f73-113">方法</span><span class="sxs-lookup"><span data-stu-id="73f73-113">Methods</span></span>

<span data-ttu-id="73f73-114">**IBackgroundCopyCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="73f73-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="73f73-115">方法</span><span class="sxs-lookup"><span data-stu-id="73f73-115">Method</span></span>                                                                    | <span data-ttu-id="73f73-116">描述</span><span class="sxs-lookup"><span data-stu-id="73f73-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="73f73-117">**JobError**</span><span class="sxs-lookup"><span data-stu-id="73f73-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="73f73-118">發生錯誤時呼叫。</span><span class="sxs-lookup"><span data-stu-id="73f73-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="73f73-119">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="73f73-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="73f73-120">在修改作業時呼叫。</span><span class="sxs-lookup"><span data-stu-id="73f73-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="73f73-121">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="73f73-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="73f73-122">當作業中的所有檔案都已成功傳送時呼叫。</span><span class="sxs-lookup"><span data-stu-id="73f73-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73f73-123">備註</span><span class="sxs-lookup"><span data-stu-id="73f73-123">Remarks</span></span>

<span data-ttu-id="73f73-124">若要接收通知，請呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法，以指定 **IBackgroundCopyCallback** 執行的介面指標。</span><span class="sxs-lookup"><span data-stu-id="73f73-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="73f73-125">若要指定您要接收的通知，請呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="73f73-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="73f73-126">只要介面指標有效，就會呼叫您的回呼。</span><span class="sxs-lookup"><span data-stu-id="73f73-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="73f73-127">當您的應用程式終止時，通知介面不再有效;請勿保存通知介面。</span><span class="sxs-lookup"><span data-stu-id="73f73-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="73f73-128">如此一來，應用程式的初始化程式應該在您要接收通知的現有工作上呼叫 [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="73f73-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f73-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="73f73-129">Requirements</span></span>



| <span data-ttu-id="73f73-130">需求</span><span class="sxs-lookup"><span data-stu-id="73f73-130">Requirement</span></span> | <span data-ttu-id="73f73-131">值</span><span class="sxs-lookup"><span data-stu-id="73f73-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f73-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73f73-132">Minimum supported client</span></span><br/> | <span data-ttu-id="73f73-133">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73f73-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="73f73-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73f73-134">Minimum supported server</span></span><br/> | <span data-ttu-id="73f73-135">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73f73-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="73f73-136">標頭</span><span class="sxs-lookup"><span data-stu-id="73f73-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f73-137"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="73f73-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="73f73-138">Idl</span><span class="sxs-lookup"><span data-stu-id="73f73-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73f73-139"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="73f73-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="73f73-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="73f73-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="73f73-141"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73f73-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="73f73-142">DLL</span><span class="sxs-lookup"><span data-stu-id="73f73-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f73-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73f73-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="73f73-144">IID</span><span class="sxs-lookup"><span data-stu-id="73f73-144">IID</span></span><br/>                      | <span data-ttu-id="73f73-145">IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="73f73-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="73f73-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73f73-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f73-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="73f73-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="73f73-148">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="73f73-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="73f73-149">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="73f73-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

