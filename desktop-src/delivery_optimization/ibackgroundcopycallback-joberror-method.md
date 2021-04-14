---
title: 'IBackgroundCopyCallback JobError 方法 (>deliveryoptimization .h) '
description: 傳遞最佳化 (當工作的狀態變更為 BG_JOB_STATE_ERROR 時，) 會呼叫 JobError 方法的執行。
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- JobError 方法
- JobError 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384517"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="a92de-106">IBackgroundCopyCallback：： JobError 方法</span><span class="sxs-lookup"><span data-stu-id="a92de-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="a92de-107">傳遞最佳化 (當工作的狀態變更為 BG_JOB_STATE_ERROR 時，) 會呼叫 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="a92de-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92de-108">語法</span><span class="sxs-lookup"><span data-stu-id="a92de-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="a92de-109">參數</span><span class="sxs-lookup"><span data-stu-id="a92de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92de-110">*pJob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a92de-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92de-111">包含作業相關的資訊，例如發生錯誤之前所傳輸的位元組數和檔案數目。</span><span class="sxs-lookup"><span data-stu-id="a92de-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="a92de-112">它也包含可繼續和取消作業的方法。</span><span class="sxs-lookup"><span data-stu-id="a92de-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="a92de-113">請勿發行 *pJob*;當 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法傳回時，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="a92de-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="a92de-114">*pError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a92de-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92de-115">包含錯誤資訊，例如發生嚴重錯誤時所處理的檔案，以及錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="a92de-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="a92de-116">請勿發行 *pError*;當 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法傳回時，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="a92de-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92de-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a92de-117">Return value</span></span>

<span data-ttu-id="a92de-118">這個方法應該會傳回 **S_OK**;否則，請繼續呼叫這個方法，直到傳回 **S_OK** 為止。</span><span class="sxs-lookup"><span data-stu-id="a92de-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="a92de-119">基於效能的考慮，您應該將傳回不 **S_OK** 值的次數限制為幾次。</span><span class="sxs-lookup"><span data-stu-id="a92de-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="a92de-120">除了傳回錯誤碼之外，請考慮一律傳回 **S_OK** ，並在內部處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="a92de-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="a92de-121">呼叫這個方法的間隔是任意的。</span><span class="sxs-lookup"><span data-stu-id="a92de-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92de-122">備註</span><span class="sxs-lookup"><span data-stu-id="a92de-122">Remarks</span></span>

<span data-ttu-id="a92de-123">判斷錯誤的原因之後，請執行下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="a92de-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="a92de-124">若要取消作業，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a92de-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="a92de-125">若要在發生錯誤之前，接受成功傳輸的部分作業，請呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a92de-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="a92de-126">此選項不適用於上傳作業;您無法完成上傳工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="a92de-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="a92de-127">若要完成處理作業，請修正問題，然後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a92de-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="a92de-128">暫時性錯誤不會產生對 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a92de-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="a92de-129">如果作業遇到 HTTP 403 錯誤，確實會傳回 BG_ERROR_CONTEXT_REMOTE_FILE，否則 BG_ERROR_CONTEXT_NONE。</span><span class="sxs-lookup"><span data-stu-id="a92de-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92de-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a92de-130">Requirements</span></span>



| <span data-ttu-id="a92de-131">需求</span><span class="sxs-lookup"><span data-stu-id="a92de-131">Requirement</span></span> | <span data-ttu-id="a92de-132">值</span><span class="sxs-lookup"><span data-stu-id="a92de-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a92de-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a92de-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a92de-134">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a92de-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a92de-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a92de-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a92de-136">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a92de-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a92de-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a92de-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a92de-138"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="a92de-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a92de-139">Idl</span><span class="sxs-lookup"><span data-stu-id="a92de-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a92de-140"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a92de-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a92de-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="a92de-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a92de-142"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a92de-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a92de-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a92de-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a92de-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a92de-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a92de-145">IID</span><span class="sxs-lookup"><span data-stu-id="a92de-145">IID</span></span><br/>                      | <span data-ttu-id="a92de-146">IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="a92de-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a92de-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a92de-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92de-148">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="a92de-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="a92de-149">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="a92de-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="a92de-150">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="a92de-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a92de-151">**IBackgroundCopyJob：： Cancel**</span><span class="sxs-lookup"><span data-stu-id="a92de-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="a92de-152">**IBackgroundCopyJob：： Resume**</span><span class="sxs-lookup"><span data-stu-id="a92de-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





