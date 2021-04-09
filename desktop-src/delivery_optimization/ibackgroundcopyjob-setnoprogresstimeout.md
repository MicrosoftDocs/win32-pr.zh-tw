---
title: 'IBackgroundCopyJob SetNoProgressTimeout 方法 (>deliveryoptimization .h) '
description: 設定在發生暫時性錯誤狀況時，) 嘗試傳送檔案的時間長度傳遞最佳化 (。 如果有進度，則會重設計時器。
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- SetNoProgressTimeout 方法
- SetNoProgressTimeout 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetNoProgressTimeout 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025162"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="bed46-107">IBackgroundCopyJob：： SetNoProgressTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="bed46-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="bed46-108">設定在發生暫時性錯誤狀況時，) 嘗試傳送檔案的時間長度傳遞最佳化 (。</span><span class="sxs-lookup"><span data-stu-id="bed46-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="bed46-109">如果有進度，則會重設計時器。</span><span class="sxs-lookup"><span data-stu-id="bed46-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed46-110">語法</span><span class="sxs-lookup"><span data-stu-id="bed46-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="bed46-111">參數</span><span class="sxs-lookup"><span data-stu-id="bed46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed46-112">*RetryPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bed46-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bed46-113">未進行任何進度之後，嘗試傳輸檔案的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bed46-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="bed46-114">高優先順序作業的預設重試期間為3600秒 (1 小時) ，而低優先順序作業為86400秒 (24 小時) 。</span><span class="sxs-lookup"><span data-stu-id="bed46-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed46-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bed46-115">Return value</span></span>

<span data-ttu-id="bed46-116">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="bed46-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="bed46-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bed46-117">Return code</span></span>                                                                                          | <span data-ttu-id="bed46-118">Description</span><span class="sxs-lookup"><span data-stu-id="bed46-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bed46-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="bed46-120">已成功設定重試期限。</span><span class="sxs-lookup"><span data-stu-id="bed46-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="bed46-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="bed46-122">無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bed46-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bed46-123">備註</span><span class="sxs-lookup"><span data-stu-id="bed46-123">Remarks</span></span>

<span data-ttu-id="bed46-124">如果在重試期間未進行任何進度，則會將工作的狀態從 BG_JOB_STATE_TRANSIENT_ERROR 移至 BG_JOB_STATE_ERROR。</span><span class="sxs-lookup"><span data-stu-id="bed46-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="bed46-125">如果您要求錯誤通知，則會呼叫您的 [**JobError**](https://www.bing.com/search?q=**JobError**) 回呼。</span><span class="sxs-lookup"><span data-stu-id="bed46-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed46-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="bed46-126">Requirements</span></span>



| <span data-ttu-id="bed46-127">需求</span><span class="sxs-lookup"><span data-stu-id="bed46-127">Requirement</span></span> | <span data-ttu-id="bed46-128">值</span><span class="sxs-lookup"><span data-stu-id="bed46-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed46-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bed46-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bed46-130">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bed46-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bed46-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bed46-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bed46-132">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bed46-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bed46-133">標頭</span><span class="sxs-lookup"><span data-stu-id="bed46-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed46-134"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="bed46-135">Idl</span><span class="sxs-lookup"><span data-stu-id="bed46-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bed46-136"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="bed46-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="bed46-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bed46-138"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="bed46-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bed46-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bed46-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bed46-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="bed46-141">IID</span><span class="sxs-lookup"><span data-stu-id="bed46-141">IID</span></span><br/>                      | <span data-ttu-id="bed46-142">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="bed46-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bed46-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bed46-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed46-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="bed46-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="bed46-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="bed46-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





