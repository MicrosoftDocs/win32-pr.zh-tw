---
title: 'IBackgroundCopyJob GetNotifyFlags 方法 (>deliveryoptimization .h) '
description: 捕獲作業的事件通知旗標。
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- GetNotifyFlags 方法
- GetNotifyFlags 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetNotifyFlags 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317247"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="a04ac-106">IBackgroundCopyJob：： GetNotifyFlags 方法</span><span class="sxs-lookup"><span data-stu-id="a04ac-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="a04ac-107">捕獲作業的事件通知旗標。</span><span class="sxs-lookup"><span data-stu-id="a04ac-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="a04ac-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a04ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="a04ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04ac-110">*pNotifyFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a04ac-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04ac-111">識別應用程式所接收的事件。</span><span class="sxs-lookup"><span data-stu-id="a04ac-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="a04ac-112">下表列出事件通知旗標值。</span><span class="sxs-lookup"><span data-stu-id="a04ac-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="a04ac-113">值</span><span class="sxs-lookup"><span data-stu-id="a04ac-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="a04ac-114">意義</span><span class="sxs-lookup"><span data-stu-id="a04ac-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="a04ac-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="a04ac-116">已傳送作業中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="a04ac-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="a04ac-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="a04ac-118">發生錯誤了。</span><span class="sxs-lookup"><span data-stu-id="a04ac-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="a04ac-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="a04ac-120">事件通知已停用。</span><span class="sxs-lookup"><span data-stu-id="a04ac-120">Event notification is disabled.</span></span> <span data-ttu-id="a04ac-121">如果設定，則會忽略其他旗標。</span><span class="sxs-lookup"><span data-stu-id="a04ac-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="a04ac-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="a04ac-123">作業已修改。</span><span class="sxs-lookup"><span data-stu-id="a04ac-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04ac-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="a04ac-124">Return value</span></span>

<span data-ttu-id="a04ac-125">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="a04ac-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a04ac-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a04ac-126">Return code</span></span>                                                                              | <span data-ttu-id="a04ac-127">Description</span><span class="sxs-lookup"><span data-stu-id="a04ac-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="a04ac-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a04ac-129">已成功抓取事件通知旗標。</span><span class="sxs-lookup"><span data-stu-id="a04ac-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a04ac-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a04ac-130">Requirements</span></span>



| <span data-ttu-id="a04ac-131">需求</span><span class="sxs-lookup"><span data-stu-id="a04ac-131">Requirement</span></span> | <span data-ttu-id="a04ac-132">值</span><span class="sxs-lookup"><span data-stu-id="a04ac-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04ac-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a04ac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a04ac-134">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a04ac-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a04ac-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a04ac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a04ac-136">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a04ac-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a04ac-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a04ac-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04ac-138"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a04ac-139">Idl</span><span class="sxs-lookup"><span data-stu-id="a04ac-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a04ac-140"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a04ac-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="a04ac-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a04ac-142"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a04ac-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a04ac-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04ac-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04ac-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a04ac-145">IID</span><span class="sxs-lookup"><span data-stu-id="a04ac-145">IID</span></span><br/>                      | <span data-ttu-id="a04ac-146">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a04ac-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a04ac-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a04ac-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04ac-148">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="a04ac-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a04ac-149">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="a04ac-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="a04ac-150">**IBackgroundCopyJob::GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="a04ac-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="a04ac-151">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="a04ac-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





