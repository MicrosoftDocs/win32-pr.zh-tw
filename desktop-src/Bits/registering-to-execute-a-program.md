---
title: 註冊以執行程式
description: 您可以註冊，讓 BITS 根據已傳送的作業和錯誤事件來執行程式，而不是作業修改事件。 BITS 會在使用者的內容中執行程式。
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- 事件通知位，命令列
- 註冊命令列通知位
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682569"
---
# <a name="registering-to-execute-a-program"></a>註冊以執行程式

您可以註冊，讓 BITS 根據已傳送的作業和錯誤事件來執行程式，而不是作業修改事件。 BITS 會在使用者的內容中執行程式。

**註冊以執行程式**

1.  呼叫 **IBackgroundCopyJob：： QueryInterface** 方法以取出 [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面指標。 指定 \_ \_ Uuidof (IBackgroundCopyJob2) 作為介面識別碼。
2.  呼叫 [**IBackgroundCopyJob2：： SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) 方法來指定要執行的程式，以及程式所需的任何引數，例如作業識別碼。

3.  呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法，以指定命令列執行的時間。

    您只能指定已傳送的 BG \_ 通知 \_ 作業 \_ 和 bg \_ 通知 \_ 作業 \_ 錯誤事件旗標。 \_ \_ 已忽略 BG 通知作業 \_ 修改旗標。

請注意，如果您也 [註冊接收 COM 回呼](registering-a-com-callback.md) ，而回呼介面指標有效，或 bits 呼叫的通知方法傳回成功碼，則 bits 不會執行程式。 但是，如果通知方法傳回失敗碼，例如 E \_ 失敗，BITS 將會執行命令列。

BITS 會呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式來啟動程式。 如果您指定參數字串，則第一個參數必須是程式名稱。

下列範例示範如何註冊，以在發生作業傳送事件時執行程式。 此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



當作業的狀態變成「BG \_ 工作」 \_ 狀態時 \_ ，BITS 會執行 pProgram 中指定的程式。 下列範例是一個簡單的程式，可接受工作識別碼作為引數。 程式會假設傳遞的引數數目是正確的。


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 