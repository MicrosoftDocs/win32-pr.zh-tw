---
title: 輪詢作業的狀態
description: 根據預設，應用程式必須輪詢作業狀態中的變更。
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- 傳送工作 BITS，輪詢
- 輪詢作業狀態位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839415"
---
# <a name="polling-for-the-status-of-the-job"></a><span data-ttu-id="5a27a-105">輪詢作業的狀態</span><span class="sxs-lookup"><span data-stu-id="5a27a-105">Polling for the Status of the Job</span></span>

<span data-ttu-id="5a27a-106">根據預設，應用程式必須輪詢作業狀態中的變更。</span><span class="sxs-lookup"><span data-stu-id="5a27a-106">By default, an application must poll for changes in the status of a job.</span></span> <span data-ttu-id="5a27a-107">若要在作業的狀態中捕捉變更，請呼叫 [**IBackgroundCopyJob：： >getstate**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a27a-107">To capture changes in the job's state, call the [**IBackgroundCopyJob::GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) method.</span></span> <span data-ttu-id="5a27a-108">若要捕捉傳送的位元組和檔案數目變更，請呼叫 [**IBackgroundCopyJob：： GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a27a-108">To capture changes in the number of bytes and files transferred, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method.</span></span> <span data-ttu-id="5a27a-109">若要在上傳-回復作業的回復部分取得進度資訊，請呼叫 [**IBackgroundCopyJob2：： GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a27a-109">To retrieve progress information on the reply portion of an upload-reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method.</span></span> <span data-ttu-id="5a27a-110">如需使用進度資訊的範例，請參閱 [判斷工作的進度](determining-the-progress-of-a-job.md)。</span><span class="sxs-lookup"><span data-stu-id="5a27a-110">For an example that uses the progress information, see [Determining the Progress of a Job](determining-the-progress-of-a-job.md).</span></span>

<span data-ttu-id="5a27a-111">[**Bg \_ 作業 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state)列舉會定義工作的狀態，而 [**bg \_ 工作 \_ 進度**](/windows/desktop/api/Bits/ns-bits-bg_job_progress)結構包含所傳輸的位元組數目和檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="5a27a-111">The [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration defines the states of a job, and the [**BG\_JOB\_PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) structure contains information on the number of bytes and files transferred.</span></span>

<span data-ttu-id="5a27a-112">若要使用輪詢，您需要建立可起始輪詢的機制。</span><span class="sxs-lookup"><span data-stu-id="5a27a-112">To use polling, you need to create a mechanism to initiate polling.</span></span> <span data-ttu-id="5a27a-113">例如，建立計時器或使用使用者介面上的 [更新] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="5a27a-113">For example, create a timer or use an "Update" button on the user interface.</span></span> <span data-ttu-id="5a27a-114">不過，在狀態或進度變更時，註冊事件通知和接收事件可能比較容易。</span><span class="sxs-lookup"><span data-stu-id="5a27a-114">However, it might be easier to register for event notification and receive events when the state or progress changes.</span></span> <span data-ttu-id="5a27a-115">如需事件通知的詳細資訊，請參閱 [註冊 COM 回呼](registering-a-com-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="5a27a-115">For information on event notification, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="5a27a-116">下列範例會使用計時器來輪詢作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a27a-116">The following example uses a timer to poll for the state of a job.</span></span> <span data-ttu-id="5a27a-117">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。</span><span class="sxs-lookup"><span data-stu-id="5a27a-117">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




