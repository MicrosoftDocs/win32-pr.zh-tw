---
title: 輪詢作業的狀態
description: 根據預設，應用程式必須輪詢作業狀態中的變更。
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- 傳送工作 BITS，輪詢
- 輪詢作業狀態位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f1f47a891968e686ae1ffc083bfa9b00d79c8bdc22e2c78ea523ef7ec707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701718"
---
# <a name="polling-for-the-status-of-the-job"></a>輪詢作業的狀態

根據預設，應用程式必須輪詢作業狀態中的變更。 若要在作業的狀態中捕捉變更，請呼叫 [**IBackgroundCopyJob：： >getstate**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) 方法。 若要捕捉傳送的位元組和檔案數目變更，請呼叫 [**IBackgroundCopyJob：： GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) 方法。 若要在上傳-回復作業的回復部分取得進度資訊，請呼叫 [**IBackgroundCopyJob2：： GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) 方法。 如需使用進度資訊的範例，請參閱 [判斷工作的進度](determining-the-progress-of-a-job.md)。

[**Bg \_ 作業 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state)列舉會定義工作的狀態，而 [**bg \_ 工作 \_ 進度**](/windows/desktop/api/Bits/ns-bits-bg_job_progress)結構包含所傳輸的位元組數目和檔案的資訊。

若要使用輪詢，您需要建立可起始輪詢的機制。 例如，建立計時器或使用使用者介面上的 [更新] 按鈕。 不過，在狀態或進度變更時，註冊事件通知和接收事件可能比較容易。 如需事件通知的詳細資訊，請參閱 [註冊 COM 回呼](registering-a-com-callback.md)。

下列範例會使用計時器來輪詢作業的狀態。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。


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



 

 




