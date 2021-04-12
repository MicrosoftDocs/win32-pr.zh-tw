---
title: 列舉傳送佇列中的作業
description: 若要列舉傳送佇列中的作業，請呼叫 IBackgroundCopyManager EnumJobs 方法。 方法會傳回 IEnumBackgroundCopyJobs 介面指標，您可以用它來列舉佇列中的作業。
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- 傳送作業位，列舉
- 列舉傳送佇列位中的作業
- 傳送佇列位，列舉
- 列舉位
- 列舉 BITS，作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300156"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a>列舉傳送佇列中的作業

若要列舉傳送佇列中的作業，請呼叫 [**IBackgroundCopyManager：： EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法。 方法會傳回 [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) 介面指標，您可以用它來列舉佇列中的作業。

若要取得使用者的作業，請將 [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法的第一個參數設定為0。 若要取出佇列中的所有作業，請將 **EnumJobs** 方法的第一個參數設定為 BG \_ JOB \_ ENUM \_ all \_ USERS。 只有具備系統管理員許可權的使用者可以取出傳送佇列中的所有作業。

請注意，列舉清單是在您呼叫 [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法時，傳送佇列中的作業快照。 不過，這些作業的屬性值會反映作業目前的值。

如果您想要取出個別的傳送作業，請呼叫 [**IBackgroundCopyManager：： GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) 方法。

若要列舉作業中的檔案，請參閱 [列舉作業中](enumerating-files-in-a-job.md)的檔案。

下列範例顯示如何列舉傳送佇列中的作業。 \_範例中的 g XferManager 變數是 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)介面指標。 如需有關如何建立 **IBackgroundCopyManager** 介面指標的詳細資訊，請參閱 [連接到 BITS 服務](connecting-to-the-bits-service.md)。


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




