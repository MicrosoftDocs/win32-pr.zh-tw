---
title: '處理 (BITS 的錯誤) '
description: 您的應用程式中有兩種類型的錯誤需要處理。
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- 處理錯誤位
- 傳輸作業位，錯誤
- 錯誤位
- 錯誤位，處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024411"
---
# <a name="handling-errors-bits"></a>處理 (BITS 的錯誤) 

您的應用程式中有兩種類型的錯誤需要處理。 第一個錯誤是方法呼叫失敗。 每個方法都會傳回 **HRESULT** 值。 每個方法的參考頁面都會識別最可能產生的傳回值。 如需其他傳回值，請參閱 [BITS 傳回值](bits-return-values.md)。 若要取得與傳回值相關聯的郵件內文，請呼叫 [**IBackgroundCopyManager：： GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) 方法。

第二種要處理的錯誤類型是其 [狀態](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) 轉換為 [bg \_ 工作 \_ 狀態 \_ 錯誤](/windows/desktop/api/Bits/ne-bits-bg_job_state) 或 **BG \_ 工作 \_ 狀態 \_ 暫時性 \_ 錯誤** 的作業。 若要取得與這些類型的錯誤相關的資訊，請呼叫作業的 [**IBackgroundCopyJob：： GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) 方法。 方法會傳回 [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) 介面指標，其中包含您用來判斷錯誤原因的資訊。 您也可以註冊接收事件通知，以接收錯誤通知。 如需詳細資訊，請參閱 [註冊 COM 回呼](registering-a-com-callback.md)。

BITS 會將每個工作視為不可部分完成。 如果作業中的其中一個檔案產生錯誤，作業會維持在錯誤狀態，直到錯誤解決為止。 因此，您無法刪除導致作業發生錯誤的檔案。 但是，如果錯誤是因為伺服器無法使用或遠端檔案無效所造成，您可以呼叫 [**IBackgroundCopyJob3：： ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) 或 [**IBackgroundCopyFile2：： SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) 方法來識別新的伺服器或檔案名。

判斷錯誤的原因之後，請執行下列其中一個選項：

-   藉由呼叫 [**IBackgroundCopyJob：： cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法來取消作業。
-   若為下載作業，請呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法，以儲存在錯誤發生之前成功傳輸的檔案。
-   請修正錯誤並呼叫 [**IBackgroundCopyJob：： Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 方法以完成工作。

若為上傳-回復作業，請檢查 [**BG \_ 作業 \_ 回復 \_ 進度**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress)結構的 **BytesTotal** 成員值，以判斷此錯誤是否發生在作業的上傳或回復部分。 如果值是 BG 大小未知，就會在上傳時發生錯誤 \_ \_ 。

下列範例顯示如何取出 [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) 介面指標。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




