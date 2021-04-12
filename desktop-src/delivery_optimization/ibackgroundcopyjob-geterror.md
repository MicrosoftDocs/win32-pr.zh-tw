---
title: 'IBackgroundCopyJob GetError 方法 (>deliveryoptimization .h) '
description: 在發生錯誤之後抓取錯誤介面。
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- GetError 方法
- GetError 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384658"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="37edd-106">IBackgroundCopyJob：： GetError 方法</span><span class="sxs-lookup"><span data-stu-id="37edd-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="37edd-107">在發生錯誤之後抓取錯誤介面。</span><span class="sxs-lookup"><span data-stu-id="37edd-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="37edd-108">傳遞最佳化 (當工作的狀態為 BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR 時，) 會產生錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="37edd-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="37edd-109">**IBackgroundCopyXXXX** 介面方法的呼叫失敗時，此服務不會建立錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="37edd-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="37edd-110">在開始將資料傳輸 (工作的狀態變更為 BG_JOB_STATE_TRANSFERRING 的工作) 或應用程式結束之前，會提供錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="37edd-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="37edd-111">語法</span><span class="sxs-lookup"><span data-stu-id="37edd-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="37edd-112">參數</span><span class="sxs-lookup"><span data-stu-id="37edd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37edd-113">*ppError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37edd-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37edd-114">提供錯誤代碼的錯誤介面、錯誤的描述，以及發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="37edd-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="37edd-115">此參數也會識別發生錯誤時所要傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="37edd-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="37edd-116">完成時釋放 *ppError* 。</span><span class="sxs-lookup"><span data-stu-id="37edd-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37edd-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="37edd-117">Return value</span></span>

<span data-ttu-id="37edd-118">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="37edd-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="37edd-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="37edd-119">Return code</span></span>                                                                                                           | <span data-ttu-id="37edd-120">Description</span><span class="sxs-lookup"><span data-stu-id="37edd-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37edd-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="37edd-122">已成功產生 error 物件。</span><span class="sxs-lookup"><span data-stu-id="37edd-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="37edd-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="37edd-124">只有在發生錯誤時，才可使用錯誤介面 (BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR) ，以及開始傳送資料 (BG_JOB_STATE_TRANSFERRING) 。</span><span class="sxs-lookup"><span data-stu-id="37edd-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37edd-125">備註</span><span class="sxs-lookup"><span data-stu-id="37edd-125">Remarks</span></span>

<span data-ttu-id="37edd-126">作業在發生嚴重錯誤時，會處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="37edd-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="37edd-127">您可以使用下列其中一個選項來判斷作業是否發生錯誤：</span><span class="sxs-lookup"><span data-stu-id="37edd-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="37edd-128">若要輪詢作業的狀態，請呼叫 [**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37edd-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="37edd-129">如果狀態為 BG_JOB_STATE_ERROR，則作業會處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="37edd-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="37edd-130">若要在發生錯誤時收到通知，請將 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面明確地 (，) 的 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法。</span><span class="sxs-lookup"><span data-stu-id="37edd-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="37edd-131">然後，呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法來註冊回呼，並呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法來設定 BG_NOTIFY_JOB_ERROR 旗標。</span><span class="sxs-lookup"><span data-stu-id="37edd-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="37edd-132">[**IBackgroundCopyError**](ibackgroundcopyerror.md)介面包含您用來判斷錯誤原因的資訊，以及傳輸程式是否可繼續。</span><span class="sxs-lookup"><span data-stu-id="37edd-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="37edd-133">判斷錯誤的原因之後，請執行下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="37edd-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="37edd-134">若要取消作業，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37edd-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="37edd-135">若要在錯誤發生之前儲存成功傳輸的檔案，請呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37edd-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="37edd-136">若要完成處理作業，請修正問題，然後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37edd-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="37edd-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="37edd-137">Requirements</span></span>



| <span data-ttu-id="37edd-138">需求</span><span class="sxs-lookup"><span data-stu-id="37edd-138">Requirement</span></span> | <span data-ttu-id="37edd-139">值</span><span class="sxs-lookup"><span data-stu-id="37edd-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37edd-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37edd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="37edd-141">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37edd-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="37edd-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37edd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="37edd-143">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37edd-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="37edd-144">標頭</span><span class="sxs-lookup"><span data-stu-id="37edd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="37edd-145"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="37edd-146">Idl</span><span class="sxs-lookup"><span data-stu-id="37edd-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37edd-147"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="37edd-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="37edd-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="37edd-149"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="37edd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="37edd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37edd-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37edd-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="37edd-152">IID</span><span class="sxs-lookup"><span data-stu-id="37edd-152">IID</span></span><br/>                      | <span data-ttu-id="37edd-153">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="37edd-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="37edd-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37edd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37edd-155">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="37edd-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="37edd-156">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="37edd-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="37edd-157">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="37edd-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="37edd-158">**IBackgroundCopyJob：： >getstate**</span><span class="sxs-lookup"><span data-stu-id="37edd-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





