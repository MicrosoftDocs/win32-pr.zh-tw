---
title: 'IBackgroundCopyJob 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyJob 介面將檔案新增至作業、設定作業的優先權層級、判斷作業的狀態，以及啟動和停止作業。
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025006"
---
# <a name="ibackgroundcopyjob-interface"></a><span data-ttu-id="c9cec-105">IBackgroundCopyJob 介面</span><span class="sxs-lookup"><span data-stu-id="c9cec-105">IBackgroundCopyJob interface</span></span>

<span data-ttu-id="c9cec-106">使用 [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) 介面將檔案新增至作業、設定作業的優先權層級、判斷作業的狀態，以及啟動和停止作業。</span><span class="sxs-lookup"><span data-stu-id="c9cec-106">Use the [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.</span></span>

<span data-ttu-id="c9cec-107">若要建立作業，請呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c9cec-107">To create a job, call the [**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md) method.</span></span> <span data-ttu-id="c9cec-108">若要取得現有作業的 [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) 介面指標，請呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c9cec-108">To get an [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) interface pointer to an existing job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="c9cec-109">成員</span><span class="sxs-lookup"><span data-stu-id="c9cec-109">Members</span></span>

<span data-ttu-id="c9cec-110">**IBackgroundCopyJob** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c9cec-110">The **IBackgroundCopyJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c9cec-111">**IBackgroundCopyJob** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9cec-111">**IBackgroundCopyJob** also has these types of members:</span></span>

-   [<span data-ttu-id="c9cec-112">方法</span><span class="sxs-lookup"><span data-stu-id="c9cec-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9cec-113">方法</span><span class="sxs-lookup"><span data-stu-id="c9cec-113">Methods</span></span>

<span data-ttu-id="c9cec-114">**IBackgroundCopyJob** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c9cec-114">The **IBackgroundCopyJob** interface has these methods.</span></span>



| <span data-ttu-id="c9cec-115">方法</span><span class="sxs-lookup"><span data-stu-id="c9cec-115">Method</span></span>                                                                  | <span data-ttu-id="c9cec-116">描述</span><span class="sxs-lookup"><span data-stu-id="c9cec-116">Description</span></span>                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9cec-117">**取消**</span><span class="sxs-lookup"><span data-stu-id="c9cec-117">**Cancel**</span></span>](ibackgroundcopyjob-cancel.md)                             | <span data-ttu-id="c9cec-118">取消作業，並從用戶端移除暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="c9cec-118">Cancels the job and removes temporary files from the client.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="c9cec-119">**完成**</span><span class="sxs-lookup"><span data-stu-id="c9cec-119">**Complete**</span></span>](ibackgroundcopyjob-complete.md)                         | <span data-ttu-id="c9cec-120">結束作業，並將傳輸的檔案儲存在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="c9cec-120">Ends the job and saves the transferred files on the client.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="c9cec-121">**EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="c9cec-121">**EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)                       | <span data-ttu-id="c9cec-122">傳回列舉值物件的介面指標，您可以用來列舉作業中的檔案。</span><span class="sxs-lookup"><span data-stu-id="c9cec-122">Returns an interface pointer to an enumerator object that you use to enumerate the files in the job.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c9cec-123">**GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="c9cec-123">**GetDisplayName**</span></span>](ibackgroundcopyjob-getdisplayname.md)             | <span data-ttu-id="c9cec-124">抓取識別作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c9cec-124">Retrieves the display name that identifies the job.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="c9cec-125">**GetError**</span><span class="sxs-lookup"><span data-stu-id="c9cec-125">**GetError**</span></span>](ibackgroundcopyjob-geterror.md)                         | <span data-ttu-id="c9cec-126">在發生錯誤之後，捕獲錯誤物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="c9cec-126">Retrieves an interface pointer to the error object after an error occurs.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="c9cec-127">**GetId**</span><span class="sxs-lookup"><span data-stu-id="c9cec-127">**GetId**</span></span>](ibackgroundcopyjob-getid.md)                               | <span data-ttu-id="c9cec-128">抓取佇列中作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9cec-128">Retrieves the identifier of the job in the queue.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="c9cec-129">**GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="c9cec-129">**GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md) | <span data-ttu-id="c9cec-130">抓取在遇到暫時性錯誤狀況之後，繼續嘗試傳送檔案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c9cec-130">Retrieves the length of time that DO continues to try to transfer the file after encountering a transient error condition.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c9cec-131">**GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="c9cec-131">**GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)             | <span data-ttu-id="c9cec-132">抓取您為應用程式設定的事件通知 (回呼) 旗標。</span><span class="sxs-lookup"><span data-stu-id="c9cec-132">Retrieves the event notification (callback) flags you have set for your application.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="c9cec-133">**GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="c9cec-133">**GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)     | <span data-ttu-id="c9cec-134">抓取 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實 (回呼) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c9cec-134">Retrieves a pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (callbacks).</span></span><br/>                                                                                    |
| [<span data-ttu-id="c9cec-135">**GetPriority**</span><span class="sxs-lookup"><span data-stu-id="c9cec-135">**GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)                   | <span data-ttu-id="c9cec-136">抓取您為作業設定的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="c9cec-136">Retrieves the priority level you have set for the job.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="c9cec-137">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="c9cec-137">**GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)                   | <span data-ttu-id="c9cec-138">抓取作業相關的進度資訊，例如傳送至用戶端的位元組數和檔案數目。</span><span class="sxs-lookup"><span data-stu-id="c9cec-138">Retrieves job-related progress information, such as the number of bytes and files transferred to the client.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="c9cec-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="c9cec-139">**GetState**</span></span>](ibackgroundcopyjob-getstate.md)                         | <span data-ttu-id="c9cec-140">捕獲作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9cec-140">Retrieves the state of the job.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="c9cec-141">**GetTimes**</span><span class="sxs-lookup"><span data-stu-id="c9cec-141">**GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)                         | <span data-ttu-id="c9cec-142">抓取與作業相關之活動的時間戳記，例如作業的建立時間。</span><span class="sxs-lookup"><span data-stu-id="c9cec-142">Retrieves time stamps for activities related to the job, such as the time the job was created.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="c9cec-143">**GetType**</span><span class="sxs-lookup"><span data-stu-id="c9cec-143">**GetType**</span></span>](ibackgroundcopyjob-gettype.md)                           | <span data-ttu-id="c9cec-144">抓取正在執行的傳輸類型，例如檔案下載。</span><span class="sxs-lookup"><span data-stu-id="c9cec-144">Retrieves the type of transfer being performed, such as a file download.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="c9cec-145">**繼續**</span><span class="sxs-lookup"><span data-stu-id="c9cec-145">**Resume**</span></span>](ibackgroundcopyjob-resume.md)                             | <span data-ttu-id="c9cec-146">開始新的作業，或重新開機已暫停的工作。</span><span class="sxs-lookup"><span data-stu-id="c9cec-146">Starts a new job or restarts a suspended job.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="c9cec-147">**SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="c9cec-147">**SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md) | <span data-ttu-id="c9cec-148">指定在遇到暫時性錯誤狀況之後，繼續嘗試傳送檔案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c9cec-148">Specifies the length of time that DO continues to try to transfer the file after encountering a transient error condition.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c9cec-149">**SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="c9cec-149">**SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)             | <span data-ttu-id="c9cec-150">指定要接收的事件通知類型。</span><span class="sxs-lookup"><span data-stu-id="c9cec-150">Specifies the type of event notification to receive.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="c9cec-151">**SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="c9cec-151">**SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)     | <span data-ttu-id="c9cec-152">指定 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實 (回呼) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c9cec-152">Specifies a pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (callbacks).</span></span> <span data-ttu-id="c9cec-153">介面會根據您設定的事件通知旗標來接收通知。</span><span class="sxs-lookup"><span data-stu-id="c9cec-153">The interface receives notification based on the event notification flags you set.</span></span><br/> |
| [<span data-ttu-id="c9cec-154">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="c9cec-154">**SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)                   | <span data-ttu-id="c9cec-155">指定相對於傳送佇列中其他作業的作業優先順序。</span><span class="sxs-lookup"><span data-stu-id="c9cec-155">Specifies the priority of the job relative to other jobs in the transfer queue.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c9cec-156">**暫停**</span><span class="sxs-lookup"><span data-stu-id="c9cec-156">**Suspend**</span></span>](ibackgroundcopyjob-suspend.md)                           | <span data-ttu-id="c9cec-157">暫停作業。</span><span class="sxs-lookup"><span data-stu-id="c9cec-157">Pauses the job.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="c9cec-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9cec-158">Requirements</span></span>



| <span data-ttu-id="c9cec-159">需求</span><span class="sxs-lookup"><span data-stu-id="c9cec-159">Requirement</span></span> | <span data-ttu-id="c9cec-160">值</span><span class="sxs-lookup"><span data-stu-id="c9cec-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cec-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9cec-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cec-162">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9cec-162">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9cec-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9cec-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cec-164">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9cec-164">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c9cec-165">標頭</span><span class="sxs-lookup"><span data-stu-id="c9cec-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9cec-166"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9cec-166"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9cec-167">Idl</span><span class="sxs-lookup"><span data-stu-id="c9cec-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9cec-168"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9cec-168"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9cec-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9cec-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9cec-170"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9cec-170"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c9cec-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cec-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cec-172"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9cec-172"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c9cec-173">IID</span><span class="sxs-lookup"><span data-stu-id="c9cec-173">IID</span></span><br/>                      | <span data-ttu-id="c9cec-174">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c9cec-174">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c9cec-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9cec-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cec-176">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="c9cec-176">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="c9cec-177">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="c9cec-177">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> </dl>

 

