---
title: 'BG_JOB_STATE 列舉 (>deliveryoptimization .h) '
description: BG_JOB_STATE 列舉會針對作業的不同狀態定義常數值。
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- BG_JOB_STATE 列舉
- BG_JOB_STATE 列舉
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968741"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="00ad1-105">BG_JOB_STATE 列舉</span><span class="sxs-lookup"><span data-stu-id="00ad1-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="00ad1-106">**BG_JOB_STATE** 列舉會針對作業的不同狀態定義常數值。</span><span class="sxs-lookup"><span data-stu-id="00ad1-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ad1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00ad1-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="00ad1-108">常數</span><span class="sxs-lookup"><span data-stu-id="00ad1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00ad1-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="00ad1-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-110">指定作業在佇列中並等候執行。</span><span class="sxs-lookup"><span data-stu-id="00ad1-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="00ad1-111">如果使用者在工作傳輸時登出，則作業會轉換成已排入佇列的狀態。</span><span class="sxs-lookup"><span data-stu-id="00ad1-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="00ad1-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-113">不支援。</span><span class="sxs-lookup"><span data-stu-id="00ad1-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="00ad1-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-115">指定要傳送作業的資料。</span><span class="sxs-lookup"><span data-stu-id="00ad1-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="00ad1-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-117">指定將工作暫停 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="00ad1-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="00ad1-118">若要暫停工作，請呼叫 [**IBackgroundCopyJob：：暫**](ibackgroundcopyjob-suspend.md) 止方法。</span><span class="sxs-lookup"><span data-stu-id="00ad1-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="00ad1-119">作業會保持暫止，直到您呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)、 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md)或 [**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="00ad1-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="00ad1-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-121">指定 (服務無法) 傳送檔案時，發生無法恢復的錯誤。</span><span class="sxs-lookup"><span data-stu-id="00ad1-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="00ad1-122">如果您可以更正錯誤，例如拒絕存取的錯誤，請在錯誤修正之後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="00ad1-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="00ad1-123">但是，如果無法修正錯誤，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法來取消作業，或呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以接受成功傳輸的下載作業部分。</span><span class="sxs-lookup"><span data-stu-id="00ad1-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="00ad1-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-125">指定發生可復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="00ad1-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="00ad1-126">確實會根據內部重試設定重試暫時性錯誤狀態中的工作。</span><span class="sxs-lookup"><span data-stu-id="00ad1-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="00ad1-127">如果作業無法進行進度，作業的狀態會變更為 **BG_JOB_STATE_ERROR** (請參閱 [**IBackgroundCopyJob：： SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)) 。</span><span class="sxs-lookup"><span data-stu-id="00ad1-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="00ad1-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-129">指定已成功處理您的作業。</span><span class="sxs-lookup"><span data-stu-id="00ad1-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="00ad1-130">您必須呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法來確認作業已完成，並將檔案提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="00ad1-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="00ad1-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-132">指定您呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以確認您的作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="00ad1-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="00ad1-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="00ad1-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="00ad1-134">指定您呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法來取消作業 (從傳送佇列) 移除作業。</span><span class="sxs-lookup"><span data-stu-id="00ad1-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00ad1-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="00ad1-135">Requirements</span></span>



| <span data-ttu-id="00ad1-136">需求</span><span class="sxs-lookup"><span data-stu-id="00ad1-136">Requirement</span></span> | <span data-ttu-id="00ad1-137">值</span><span class="sxs-lookup"><span data-stu-id="00ad1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ad1-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00ad1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="00ad1-139">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00ad1-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00ad1-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00ad1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="00ad1-141">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00ad1-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00ad1-142">標頭</span><span class="sxs-lookup"><span data-stu-id="00ad1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ad1-143"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="00ad1-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ad1-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00ad1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ad1-145">**IBackgroundCopyJob：： >getstate**</span><span class="sxs-lookup"><span data-stu-id="00ad1-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





