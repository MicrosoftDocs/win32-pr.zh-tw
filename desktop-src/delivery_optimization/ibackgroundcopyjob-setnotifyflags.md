---
title: 'IBackgroundCopyJob SetNotifyFlags 方法 (>deliveryoptimization .h) '
description: 指定您想要接收的事件通知類型，例如作業傳輸事件。
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- SetNotifyFlags 方法
- SetNotifyFlags 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetNotifyFlags 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508623"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="48a61-106">IBackgroundCopyJob：： SetNotifyFlags 方法</span><span class="sxs-lookup"><span data-stu-id="48a61-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="48a61-107">指定您想要接收的事件通知類型，例如作業傳輸事件。</span><span class="sxs-lookup"><span data-stu-id="48a61-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a61-108">語法</span><span class="sxs-lookup"><span data-stu-id="48a61-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="48a61-109">參數</span><span class="sxs-lookup"><span data-stu-id="48a61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a61-110">*NotifyFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48a61-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a61-111">設定下列一或多個旗標，以識別您想要接收的事件。</span><span class="sxs-lookup"><span data-stu-id="48a61-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="48a61-112">值</span><span class="sxs-lookup"><span data-stu-id="48a61-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="48a61-113">意義</span><span class="sxs-lookup"><span data-stu-id="48a61-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="48a61-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="48a61-115">已傳送作業中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="48a61-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="48a61-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="48a61-117">發生錯誤了。</span><span class="sxs-lookup"><span data-stu-id="48a61-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="48a61-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="48a61-119">不支援。</span><span class="sxs-lookup"><span data-stu-id="48a61-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="48a61-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="48a61-121">作業已修改。</span><span class="sxs-lookup"><span data-stu-id="48a61-121">The job has been modified.</span></span> <span data-ttu-id="48a61-122">例如，屬性值已變更、工作的狀態已變更，或進度會轉移檔。</span><span class="sxs-lookup"><span data-stu-id="48a61-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="48a61-123">如果已指定命令列通知，則會忽略此旗標。</span><span class="sxs-lookup"><span data-stu-id="48a61-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="48a61-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="48a61-125">已傳送作業中的檔案。</span><span class="sxs-lookup"><span data-stu-id="48a61-125">A file in the job has been transferred.</span></span> <span data-ttu-id="48a61-126">如果已指定命令列通知，則會忽略此旗標。</span><span class="sxs-lookup"><span data-stu-id="48a61-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="48a61-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="48a61-128">不支援。</span><span class="sxs-lookup"><span data-stu-id="48a61-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a61-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a61-129">Return value</span></span>

<span data-ttu-id="48a61-130">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="48a61-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="48a61-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="48a61-131">Return code</span></span>                                                                                          | <span data-ttu-id="48a61-132">Description</span><span class="sxs-lookup"><span data-stu-id="48a61-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48a61-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="48a61-134">已成功設定事件通知的類型。</span><span class="sxs-lookup"><span data-stu-id="48a61-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="48a61-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="48a61-136">無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="48a61-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48a61-137">備註</span><span class="sxs-lookup"><span data-stu-id="48a61-137">Remarks</span></span>

<span data-ttu-id="48a61-138">使用 **SetNotifyFlags** 方法搭配 [**IBackgroundCopyJob：： SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)。</span><span class="sxs-lookup"><span data-stu-id="48a61-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a61-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="48a61-139">Requirements</span></span>



| <span data-ttu-id="48a61-140">需求</span><span class="sxs-lookup"><span data-stu-id="48a61-140">Requirement</span></span> | <span data-ttu-id="48a61-141">值</span><span class="sxs-lookup"><span data-stu-id="48a61-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a61-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48a61-142">Minimum supported client</span></span><br/> | <span data-ttu-id="48a61-143">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48a61-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48a61-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48a61-144">Minimum supported server</span></span><br/> | <span data-ttu-id="48a61-145">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48a61-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="48a61-146">標頭</span><span class="sxs-lookup"><span data-stu-id="48a61-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a61-147"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="48a61-148">Idl</span><span class="sxs-lookup"><span data-stu-id="48a61-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48a61-149"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="48a61-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="48a61-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="48a61-151"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="48a61-152">DLL</span><span class="sxs-lookup"><span data-stu-id="48a61-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a61-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a61-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="48a61-154">IID</span><span class="sxs-lookup"><span data-stu-id="48a61-154">IID</span></span><br/>                      | <span data-ttu-id="48a61-155">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="48a61-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="48a61-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48a61-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a61-157">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="48a61-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="48a61-158">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="48a61-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="48a61-159">**IBackgroundCopyJob::GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="48a61-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="48a61-160">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="48a61-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





