---
title: 'IBackgroundCopyJob Complete 方法 (>deliveryoptimization. h) '
description: 結束作業，並將傳輸的檔案儲存在用戶端上。
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete 方法
- Complete 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Complete 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103656"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="3beeb-106">IBackgroundCopyJob：： Complete 方法</span><span class="sxs-lookup"><span data-stu-id="3beeb-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="3beeb-107">結束作業，並將傳輸的檔案儲存在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="3beeb-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3beeb-108">語法</span><span class="sxs-lookup"><span data-stu-id="3beeb-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="3beeb-109">參數</span><span class="sxs-lookup"><span data-stu-id="3beeb-109">Parameters</span></span>

<span data-ttu-id="3beeb-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3beeb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3beeb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3beeb-111">Return value</span></span>

<span data-ttu-id="3beeb-112">這個方法會傳回下列 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3beeb-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="3beeb-113">方法也可能會傳回與將已傳送檔案的暫存複本重新命名為其指定名稱相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3beeb-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="3beeb-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3beeb-114">Return code</span></span>                                                                                          | <span data-ttu-id="3beeb-115">Description</span><span class="sxs-lookup"><span data-stu-id="3beeb-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3beeb-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="3beeb-117">所有檔案都已成功傳輸。</span><span class="sxs-lookup"><span data-stu-id="3beeb-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="3beeb-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="3beeb-119">若為下載，無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="3beeb-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="3beeb-120">針對上傳，必須 BG_JOB_STATE_TRANSFERRED 工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="3beeb-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3beeb-121">備註</span><span class="sxs-lookup"><span data-stu-id="3beeb-121">Remarks</span></span>

<span data-ttu-id="3beeb-122">如果工作的狀態為 **BG_JOB_STATE_TRANSFERRED**，則所有檔案都已成功傳輸。</span><span class="sxs-lookup"><span data-stu-id="3beeb-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="3beeb-123">若要檢查作業的狀態，請呼叫 [**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3beeb-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="3beeb-124">當所有檔案都已傳送至用戶端時，您也可以執行 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面來接收通知。</span><span class="sxs-lookup"><span data-stu-id="3beeb-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="3beeb-125">確實會保留少於30天的工作。</span><span class="sxs-lookup"><span data-stu-id="3beeb-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="3beeb-126">將會移除所有較舊的作業。</span><span class="sxs-lookup"><span data-stu-id="3beeb-126">All older jobs will be removed.</span></span> <span data-ttu-id="3beeb-127">不支援 [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) 群組原則。</span><span class="sxs-lookup"><span data-stu-id="3beeb-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="3beeb-128">針對下載作業，您可以在傳輸程式期間隨時呼叫 **Complete** 方法;不過，只有在呼叫這個方法之前成功傳送至用戶端的檔案才會儲存。</span><span class="sxs-lookup"><span data-stu-id="3beeb-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="3beeb-129">例如，如果您在處理五個檔案的第三個檔案時呼叫 **Complete** 方法，則只會儲存前兩個檔案。</span><span class="sxs-lookup"><span data-stu-id="3beeb-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="3beeb-130">若要判斷已傳送的檔案，請呼叫 [**IBackgroundCopyFile：： GetProgress**](ibackgroundcopyfile-getprogress-method.md)方法，並將 **BytesTransferred** 成員與 [**BG_FILE_PROGRESS**](bg-file-progress.md)結構的 **BytesTotal** 成員進行比較。</span><span class="sxs-lookup"><span data-stu-id="3beeb-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="3beeb-131">針對上傳作業，只有在作業的狀態為 **BG_JOB_STATE_TRANSFERRED** 時，您才能呼叫 **Complete** 方法。</span><span class="sxs-lookup"><span data-stu-id="3beeb-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="3beeb-132">檔案的擁有者是進行呼叫的使用者。</span><span class="sxs-lookup"><span data-stu-id="3beeb-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="3beeb-133">例如，如果系統管理員完成他人的工作，系統管理員不會擁有該檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="3beeb-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3beeb-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3beeb-134">Requirements</span></span>



| <span data-ttu-id="3beeb-135">需求</span><span class="sxs-lookup"><span data-stu-id="3beeb-135">Requirement</span></span> | <span data-ttu-id="3beeb-136">值</span><span class="sxs-lookup"><span data-stu-id="3beeb-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beeb-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3beeb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3beeb-138">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3beeb-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3beeb-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3beeb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3beeb-140">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3beeb-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3beeb-141">標頭</span><span class="sxs-lookup"><span data-stu-id="3beeb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3beeb-142"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3beeb-143">Idl</span><span class="sxs-lookup"><span data-stu-id="3beeb-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3beeb-144"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3beeb-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="3beeb-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="3beeb-146"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3beeb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3beeb-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3beeb-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3beeb-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3beeb-149">IID</span><span class="sxs-lookup"><span data-stu-id="3beeb-149">IID</span></span><br/>                      | <span data-ttu-id="3beeb-150">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="3beeb-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3beeb-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3beeb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3beeb-152">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="3beeb-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3beeb-153">**IBackgroundCopyJob：： Cancel**</span><span class="sxs-lookup"><span data-stu-id="3beeb-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="3beeb-154">**IBackgroundCopyJob：： >getstate**</span><span class="sxs-lookup"><span data-stu-id="3beeb-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





