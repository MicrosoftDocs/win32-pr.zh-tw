---
title: 設定和取出作業的屬性
description: 作業的擁有者或具有系統管理員許可權的使用者可以隨時設定和取出作業的屬性。
ms.assetid: 5d0ab96b-b818-4b41-8317-cf50ad17c12d
keywords:
- 傳送作業位，屬性
- 設定作業屬性位
- 正在抓取作業屬性位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ded532d3c99c8f8063a5c372c60086f35320d321860b056b60f2cb5a9a4003
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004828"
---
# <a name="setting-and-retrieving-the-properties-of-a-job"></a>設定和取出作業的屬性

作業的擁有者或具有系統管理員許可權的使用者可以隨時設定和取出作業的屬性。 如需可設定和取出的完整屬性清單，請參閱 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)、 [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)、 [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)和 [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) 介面。

檔案也會包含屬性。 如需如何從作業中取出檔案和其屬性的詳細資訊，請參閱 [列舉作業中](enumerating-files-in-a-job.md)的檔案。

若要傳送檔案，您不需要變更作業屬性的預設值，BITS 會使用適用于一般應用程式的預設值。

## <a name="setting-the-properties-of-a-job"></a>設定作業的屬性

下列範例顯示如何設定您的應用程式最有可能變更的屬性： [優先順序](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)、 [通知介面](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)、 [通知旗標](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)和 [回復檔案名](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename)。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 是有效的。


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob4* pJob4 = NULL;
CNotifyInterface *pNotify = new CNotifyInterface();

hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob4), (void**)&pJob4);
pJob->Release();

//The default priority level for a job is BG_JOB_PRIORITY_NORMAL. 
hr = pJob4->SetPriority(BG_JOB_PRIORITY_HIGH);
if (FAILED(hr))
{
  //Handle error
}

//By default, an application must poll BITS for the status of a job.
//To specify an IBackgroundCopyCallback interface pointer that receives event 
//notification based on the value of the notify flags property, set the notify 
//interface property. For details on the CNotifyInterface example class, see the 
//IBackgroundCopyCallback interface in the reference section.
hr = pJob4->SetNotifyInterface(pNotify);
if (SUCCEEDED(hr))
{
  hr = pJob4->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                            BG_NOTIFY_JOB_ERROR);
}
pNotify->Release();
if (FAILED(hr))
{
  //Handle error - failed to setup notification callbacks
}

//Only set the reply file name if the job's type is BG_JOB_TYPE_UPLOAD_REPLY.
//If you do not set the file name before calling the IBackgroundCopyJob::Resume 
//method, BITS generates a file name for you; the directory is the same as that
//specified for the local file name (the file being uploaded). To retrieve the 
//file name, call the IBackgroundCopyJob2::GetReplyFileName method.
hr = pJob4->SetReplyFileName(L"<REPLYPATHGOESHERE>");
if (FAILED(hr))
{
  //Handle error
}
pJob4->Release();
```



根據預設，BITS 會從源伺服器下載內容。 若要從對等下載內容，電腦和作業都必須啟用對等快取。 若要在電腦上啟用對等快取，請設定 EnablePeerCaching 群組原則設定。 您也可以呼叫 [**IBitsPeerCacheAdministration：： SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) 方法，在電腦上啟用對等快取;不過，原則會覆寫喜好設定（如果設定的話）。 若要啟用作業的對等快取，您必須呼叫 [**IBackgroundCopyJob4：： SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) 方法。

若要指定自訂標頭、用戶端驗證的用戶端憑證，以及重新導向原則、CRL 檢查，以及指定要忽略哪些憑證錯誤的 HTTP 選項，請使用 [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) 介面。 若要取得 **IBackgroundCopyJobHttpOptions** 介面，請查詢任何 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面。

## <a name="retrieving-the-properties-of-a-job"></a>正在抓取作業的屬性

下列範例示範如何取出作業的 [顯示名稱](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)、 [擁有](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)者、 [進度](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)和 [狀態](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) 屬性值。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標 pJob 是有效的。


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR* pszJobName = NULL;
WCHAR* pszOwnerSid = NULL;
BOOL bResult;
DWORD dwNameSize = 0;
DWORD dwDomainSize = 0;
WCHAR* pszName = NULL;
WCHAR* pszDomain = NULL;
WCHAR* pszFullOwnerName = NULL;
PSID pSid = NULL;
SID_NAME_USE eNameUse;
BG_JOB_PROGRESS Progress;
int PercentOfFiles = 0;
BG_JOB_PRIORITY Priority;
BG_JOB_STATE State;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

//Name of the job to use in the user interface. The name is set when you 
//create the job. You can use the SetDisplayName method to change the name. 
hr = pJob->GetDisplayName(&pszJobName);
if (SUCCEEDED(hr))
{
  //Use the name in a user interface or output.
  CoTaskMemFree(pszJobName);       
}

//The owner property contains the SID of the job's owner. The following code
//shows how to get the domain and user names associated with the SID.
hr = pJob->GetOwner(&pszOwnerSID);
if (SUCCEEDED(hr))
{
  bResult = ConvertStringSidToSid(pszOwnerSid, &pSid);
  CoTaskMemFree(pszOwnerSid);
  if (bResult)
  {
    //Call LookupAccountSid twice. The first call retrieves the buffer size 
    //for name and domain and the second call retrieves the actual name and domain.
    LookupAccountSid(NULL, pSid, NULL, &cbNameSize, 
                               NULL, &cbDomainSize, &eNameUse);
    LastError = GetLastError();
    if (ERROR_INSUFFICIENT_BUFFER == LastError)
    {
      pszName = (WCHAR*)malloc(sizeof(WCHAR) * cbNameSize);
      pszDomain = (WCHAR*)malloc(sizeof(WCHAR) * cbDomainSize);
      if (pszName && pszDomain)
      {
        bResult = LookupAccountSid(NULL, pSid, pszName, &cbNameSize, 
                                   pszDomain, &cbDomainSize, &eNameUse);
        if (bResult)
        {
          pszFullName = (WCHAR*)malloc(sizeof(WCHAR)*(cbDomainSize+1+cbNameSize+1));
          if (pszFullName)
          {
            StringCchPrintf(pszFullName, cbDomainSize+1+cbNameSize+1, L"%s\\%s", pszDomain, pszName);
            //Do something with pszFullName. 
            free(pszFullName);
          }
        }
      }
      if (pszDomain)
        free(pszDomain);
      if(pszName)
        free(pszName);
    }
    else
    {
      //Handle error - most likely ERROR_NONE_MAPPED, could not find the SID.
    }
    LocalFree(pSid);
  }
}

//The state property identifies the current state of the job. For example, the 
//state of the job is BG_JOB_STATE_TRANSFERRING or BG_JOB_STATE_ERROR. 
hr = pJob->GetState(&State);
if (SUCCEEDED(hr))
{
  //Use JobStates[State] to set the text representation of the job's 
  //state in a user interface.
}

//Use the information contained in the BG_JOB_PROGRESS structure to determine the 
//overall progress of the job. The structure contains information on the number of 
//bytes and files transferred. 
hr = pJob->GetProgress(&Progress);
if (SUCCEEDED(hr))
{
  //Determine the progress of the job based on the number of files transferred.
  if (Progress.FilesTotal > 0)
  {
    PercentOfFiles = 100*Progress.FilesTransferred/Progress.FilesTotal
  }
  //For an example that shows determining the progress of the job based on the 
  //number of bytes transferred, see the topic Determing the Progress of a Job.
}
```



 

 




