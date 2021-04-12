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
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="a3b94-109">列舉傳送佇列中的作業</span><span class="sxs-lookup"><span data-stu-id="a3b94-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="a3b94-110">若要列舉傳送佇列中的作業，請呼叫 [**IBackgroundCopyManager：： EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法。</span><span class="sxs-lookup"><span data-stu-id="a3b94-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="a3b94-111">方法會傳回 [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) 介面指標，您可以用它來列舉佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="a3b94-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="a3b94-112">若要取得使用者的作業，請將 [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法的第一個參數設定為0。</span><span class="sxs-lookup"><span data-stu-id="a3b94-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="a3b94-113">若要取出佇列中的所有作業，請將 **EnumJobs** 方法的第一個參數設定為 BG \_ JOB \_ ENUM \_ all \_ USERS。</span><span class="sxs-lookup"><span data-stu-id="a3b94-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="a3b94-114">只有具備系統管理員許可權的使用者可以取出傳送佇列中的所有作業。</span><span class="sxs-lookup"><span data-stu-id="a3b94-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="a3b94-115">請注意，列舉清單是在您呼叫 [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) 方法時，傳送佇列中的作業快照。</span><span class="sxs-lookup"><span data-stu-id="a3b94-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="a3b94-116">不過，這些作業的屬性值會反映作業目前的值。</span><span class="sxs-lookup"><span data-stu-id="a3b94-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="a3b94-117">如果您想要取出個別的傳送作業，請呼叫 [**IBackgroundCopyManager：： GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) 方法。</span><span class="sxs-lookup"><span data-stu-id="a3b94-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="a3b94-118">若要列舉作業中的檔案，請參閱 [列舉作業中](enumerating-files-in-a-job.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="a3b94-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="a3b94-119">下列範例顯示如何列舉傳送佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="a3b94-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="a3b94-120">\_範例中的 g XferManager 變數是 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)介面指標。</span><span class="sxs-lookup"><span data-stu-id="a3b94-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="a3b94-121">如需有關如何建立 **IBackgroundCopyManager** 介面指標的詳細資訊，請參閱 [連接到 BITS 服務](connecting-to-the-bits-service.md)。</span><span class="sxs-lookup"><span data-stu-id="a3b94-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


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



 

 




