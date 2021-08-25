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
ms.openlocfilehash: 01a986b8a8869008db34e97c1cc7e0cd733c301f5cdc57ce4ef6e313ff382479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801458"
---
# <a name="enumerating-files-in-a-job"></a>列舉作業中的檔案

若要列舉作業中的檔案，請呼叫 [**IBackgroundCopyJob：： EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) 方法。 方法會傳回用來列舉檔案的 [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) 介面指標。

請注意，在您呼叫 [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) 方法時，列舉清單是作業中檔案的快照集。 不過，這些檔案物件的屬性值會反映檔案目前的值。

下列範例將示範如何列舉作業中的檔案，並取得其屬性。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。


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



 

 




