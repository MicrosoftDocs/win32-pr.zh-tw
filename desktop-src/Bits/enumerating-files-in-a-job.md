---
title: 列舉作業中的檔案
description: 若要列舉作業中的檔案，請呼叫 IBackgroundCopyJob EnumFiles 方法。 方法會傳回用來列舉檔案的 IEnumBackgroundCopyFiles 介面指標。
ms.assetid: 0e1fa024-4576-434c-bc5f-518d246b5faa
keywords:
- 傳送工作 BITS，列舉檔
- 列舉檔位
- 列舉位，檔案
- 檔案傳輸位，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0db704e47a0e075801de2434ed30ba6fb8d8c91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671624"
---
# <a name="enumerating-files-in-a-job"></a><span data-ttu-id="cda97-108">列舉作業中的檔案</span><span class="sxs-lookup"><span data-stu-id="cda97-108">Enumerating Files in a Job</span></span>

<span data-ttu-id="cda97-109">若要列舉作業中的檔案，請呼叫 [**IBackgroundCopyJob：： EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) 方法。</span><span class="sxs-lookup"><span data-stu-id="cda97-109">To enumerate files in a job, call the [**IBackgroundCopyJob::EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="cda97-110">方法會傳回用來列舉檔案的 [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cda97-110">The method returns an [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) interface pointer that you use to enumerate the files.</span></span>

<span data-ttu-id="cda97-111">請注意，在您呼叫 [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) 方法時，列舉清單是作業中檔案的快照集。</span><span class="sxs-lookup"><span data-stu-id="cda97-111">Note that the enumerated list is a snapshot of the files in the job at the time you call the [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="cda97-112">不過，這些檔案物件的屬性值會反映檔案目前的值。</span><span class="sxs-lookup"><span data-stu-id="cda97-112">However, the property values of those file objects reflect the current values of the file.</span></span>

<span data-ttu-id="cda97-113">下列範例將示範如何列舉作業中的檔案，並取得其屬性。</span><span class="sxs-lookup"><span data-stu-id="cda97-113">The following example shows how to enumerate files in a job and retrieve their properties.</span></span> <span data-ttu-id="cda97-114">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。</span><span class="sxs-lookup"><span data-stu-id="cda97-114">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
IBackgroundCopyJob* pJob;
IEnumBackgroundCopyFiles* pFiles = NULL;
IBackgroundCopyFile* pFile = NULL;
IBackgroundCopyFile3* pFile3 = NULL;
WCHAR* pLocalFileName = NULL;
ULONG cFileCount = 0;
ULONG idx = 0;

hr = pJob->EnumFiles(&pFiles);
if (SUCCEEDED(hr))
{
  //Get the count of files in the job. 
  pFiles->GetCount(&cFileCount);

  //Enumerate the files in the job.
  for (idx=0; idx<cFileCount; idx++)
  {
    hr = pFiles->Next(1, &pFile, NULL);
    if (S_OK == hr)
    {
      // Query for the latest file interface.
      hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
      pFile->Release();
      if (FAILED(hr))
      {
        wprintf(L"pFile->QueryInterface failed with 0x%x.\n", hr);
        goto cleanup;
      }

      // You can use the interface to retrieve the local and remote file
      // names, get the ranges to download if only part of the file content
      // is requested, determine the progress of the transfer, change the remote file
      // name, get the name of the temporary file that BITS uses to download
      // the file, determine if the file is downloaded from a peer, and set
      // the validation state of the file so it can be shared with peers.

      //Get the local name of the file.
      hr = pFile3->GetLocalName(&pLocalFileName);
      if (SUCCEEDED(hr))
      {
        //Do something with the file information.
      }

      CoTaskMemFree(pLocalFileName); 
      pFile3->Release();
      pFile3 = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pFiles->Release();
  pFiles = NULL;
}
```



 

 




