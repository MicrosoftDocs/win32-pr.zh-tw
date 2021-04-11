---
title: 'IBackgroundCopyJob Resume 方法 (>deliveryoptimization .h) '
description: 啟用新的作業，或重新開機已暫停的工作。
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume 方法
- Resume 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Resume 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094191"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="c9418-106">IBackgroundCopyJob：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="c9418-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="c9418-107">啟用新的作業，或重新開機已暫停的工作。</span><span class="sxs-lookup"><span data-stu-id="c9418-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9418-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9418-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="c9418-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9418-109">Parameters</span></span>

<span data-ttu-id="c9418-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c9418-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9418-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9418-111">Return value</span></span>

<span data-ttu-id="c9418-112">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="c9418-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="c9418-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9418-113">Return code</span></span>                                                                                          | <span data-ttu-id="c9418-114">Description</span><span class="sxs-lookup"><span data-stu-id="c9418-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9418-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="c9418-116">已成功重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="c9418-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="c9418-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="c9418-118">沒有要傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="c9418-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="c9418-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="c9418-120">無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9418-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9418-121">備註</span><span class="sxs-lookup"><span data-stu-id="c9418-121">Remarks</span></span>

<span data-ttu-id="c9418-122">當您建立作業時，會一開始就暫停作業。</span><span class="sxs-lookup"><span data-stu-id="c9418-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="c9418-123">呼叫 **Resume** 會將作業移至傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="c9418-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="c9418-124">請注意，作業必須包含一或多個檔案，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c9418-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="c9418-125">如果處於 BG_JOB_STATE_TRANSIENT_ERROR 或 BG_JOB_STATE_ERROR 狀態的作業，請在修正錯誤之後，呼叫 **Resume** 方法以重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="c9418-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9418-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9418-126">Requirements</span></span>



| <span data-ttu-id="c9418-127">需求</span><span class="sxs-lookup"><span data-stu-id="c9418-127">Requirement</span></span> | <span data-ttu-id="c9418-128">值</span><span class="sxs-lookup"><span data-stu-id="c9418-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9418-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9418-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9418-130">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9418-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9418-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9418-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9418-132">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9418-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c9418-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c9418-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9418-134"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9418-135">Idl</span><span class="sxs-lookup"><span data-stu-id="c9418-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9418-136"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9418-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9418-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9418-138"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c9418-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c9418-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9418-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9418-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c9418-141">IID</span><span class="sxs-lookup"><span data-stu-id="c9418-141">IID</span></span><br/>                      | <span data-ttu-id="c9418-142">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c9418-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c9418-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9418-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9418-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="c9418-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c9418-145">**IBackgroundCopyJob：： Cancel**</span><span class="sxs-lookup"><span data-stu-id="c9418-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="c9418-146">**IBackgroundCopyJob：：暫止**</span><span class="sxs-lookup"><span data-stu-id="c9418-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





