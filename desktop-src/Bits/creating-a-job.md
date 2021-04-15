---
title: 建立作業
description: 若要建立傳送作業，請呼叫 IBackgroundCopyManager >batchclient.joboperations.createjob 方法。
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- 傳送工作 BITS
- 傳送工作 BITS，建立
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462085"
---
# <a name="creating-a-job"></a><span data-ttu-id="27532-105">建立作業</span><span class="sxs-lookup"><span data-stu-id="27532-105">Creating a Job</span></span>

<span data-ttu-id="27532-106">若要建立傳送作業，請呼叫 [**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) 方法。</span><span class="sxs-lookup"><span data-stu-id="27532-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="27532-107">在 BITS 建立作業之後，請 [將檔案新增至作業](adding-files-to-a-job.md) ，並視需要 [修改作業的屬性](setting-and-retrieving-the-properties-of-a-job.md) 以供您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="27532-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="27532-108">若要啟動佇列中的作業，請呼叫 [**IBackgroundCopyJob：： Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 方法。</span><span class="sxs-lookup"><span data-stu-id="27532-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="27532-109">[**>batchclient.joboperations.createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob)方法會建立可唯一識別作業的 GUID。</span><span class="sxs-lookup"><span data-stu-id="27532-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="27532-110">您可以使用 GUID [從傳送佇列中取出工作](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob)。</span><span class="sxs-lookup"><span data-stu-id="27532-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="27532-111">當您建立作業時所提供的顯示名稱不是唯一的;有一個以上的作業可以使用相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="27532-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="27532-112">BITS 會將佇列中的作業數目限制為300個工作，以及使用者可以建立至60作業的工作數目。</span><span class="sxs-lookup"><span data-stu-id="27532-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="27532-113">這些限制不適用於系統管理員或服務。</span><span class="sxs-lookup"><span data-stu-id="27532-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="27532-114">若要變更這些預設限制，請參閱 [群組原則](group-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="27532-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="27532-115">下列範例顯示如何建立下載工作。</span><span class="sxs-lookup"><span data-stu-id="27532-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="27532-116">此範例假設 g \_ pbcm 變數是有效的 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="27532-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="27532-117">如需有關如何建立 **IBackgroundCopyManager** 介面指標的詳細資訊，請參閱 [連接到 BITS 服務](connecting-to-the-bits-service.md)。</span><span class="sxs-lookup"><span data-stu-id="27532-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



<span data-ttu-id="27532-118">若要取得最新的 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面，請呼叫 **IBackgroundCopyJob：： QueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="27532-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="27532-119">下列範例顯示如何取得 [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) 介面。</span><span class="sxs-lookup"><span data-stu-id="27532-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




