---
title: 完成和取消作業
description: 若要完成傳送作業，請呼叫 IBackgroundCopyJob Complete 方法。
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- 傳送工作 BITS，取消
- 取消作業位
- 傳送工作 BITS，完成
- 完成作業位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462076"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="c15b6-107">完成和取消作業</span><span class="sxs-lookup"><span data-stu-id="c15b6-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="c15b6-108">若要完成傳送作業，請呼叫 [**IBackgroundCopyJob：： complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法。</span><span class="sxs-lookup"><span data-stu-id="c15b6-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="c15b6-109">若為下載工作，您可以在作業狀態為 [已 \_ \_) 傳輸的 BG 工作狀態] 之前，先呼叫 Complete 方法 (，然後再將作業的狀態傳送給工作狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c15b6-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="c15b6-110">只有位在您呼叫 **Complete** 方法之前成功傳送至用戶端的檔案，才可供使用者使用。</span><span class="sxs-lookup"><span data-stu-id="c15b6-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="c15b6-111">針對上傳作業，只有在作業的狀態為 [BG 作業狀態已傳送] 時，才會呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="c15b6-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="c15b6-112">若要判斷作業的狀態是否為 BG \_ 作業 \_ 狀態 \_ 傳輸，請 [輪詢](polling-for-the-status-of-the-job.md) 作業的狀態屬性或註冊，以接收 bg \_ 通知作業已 \_ \_ 傳送 [事件通知](registering-a-com-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="c15b6-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="c15b6-113">若要取消傳送作業，請呼叫 [**IBackgroundCopyJob：： cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法。</span><span class="sxs-lookup"><span data-stu-id="c15b6-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="c15b6-114">**Cancel** 方法會從傳送佇列中移除工作，並從用戶端移除暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="c15b6-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="c15b6-115">一般來說，如果您無法解決與作業相關聯的錯誤，您就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c15b6-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="c15b6-116">如果上傳未完成， [**取消**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法會取消上傳。</span><span class="sxs-lookup"><span data-stu-id="c15b6-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="c15b6-117">如果上傳已完成，且作業的類型為 BG \_ 作業 \_ 類型 \_ 上傳 \_ 回復，則方法會取消回復。</span><span class="sxs-lookup"><span data-stu-id="c15b6-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="c15b6-118">如果您未在90天內呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法或 [**IBackgroundCopyJob：： Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法 (預設 [JobInactivityTimeout](group-policies.md) 群組原則) ，服務就會取消作業。</span><span class="sxs-lookup"><span data-stu-id="c15b6-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="c15b6-119">如果服務取消此作業，則不會將下載的檔案和回復檔案提供給用戶端;作業取消不會影響已成功上傳的檔案。</span><span class="sxs-lookup"><span data-stu-id="c15b6-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="c15b6-120">您應該一律呼叫 **Complete** 或 **Cancel** 方法，而不是依賴 JobInactivityTimeout 原則來清除您的工作。</span><span class="sxs-lookup"><span data-stu-id="c15b6-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="c15b6-121">如果達到 MaxJobsPerUser 或 MaxJobsPerMachine 原則限制，佇列中剩餘的作業可能會讓使用者無法建立其他作業。</span><span class="sxs-lookup"><span data-stu-id="c15b6-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




