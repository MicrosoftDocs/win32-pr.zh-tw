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
# <a name="registering-to-execute-a-program"></a><span data-ttu-id="10c02-106">註冊以執行程式</span><span class="sxs-lookup"><span data-stu-id="10c02-106">Registering to Execute a Program</span></span>

<span data-ttu-id="10c02-107">您可以註冊，讓 BITS 根據已傳送的作業和錯誤事件來執行程式，而不是作業修改事件。</span><span class="sxs-lookup"><span data-stu-id="10c02-107">You can register to have BITS execute a program based on job transferred and error events, but not job modified events.</span></span> <span data-ttu-id="10c02-108">BITS 會在使用者的內容中執行程式。</span><span class="sxs-lookup"><span data-stu-id="10c02-108">BITS executes the program in the user's context.</span></span>

<span data-ttu-id="10c02-109">**註冊以執行程式**</span><span class="sxs-lookup"><span data-stu-id="10c02-109">**To register to execute a program**</span></span>

1.  <span data-ttu-id="10c02-110">呼叫 **IBackgroundCopyJob：： QueryInterface** 方法以取出 [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="10c02-110">Call the **IBackgroundCopyJob::QueryInterface** method to retrieve an [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface pointer.</span></span> <span data-ttu-id="10c02-111">指定 \_ \_ Uuidof (IBackgroundCopyJob2) 作為介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="10c02-111">Specify \_\_uuidof(IBackgroundCopyJob2) as the interface identifier.</span></span>
2.  <span data-ttu-id="10c02-112">呼叫 [**IBackgroundCopyJob2：： SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) 方法來指定要執行的程式，以及程式所需的任何引數，例如作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="10c02-112">Call the [**IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) method to specify the program to execute and any arguments required by the program, such as the job identifier.</span></span>

3.  <span data-ttu-id="10c02-113">呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) 方法，以指定命令列執行的時間。</span><span class="sxs-lookup"><span data-stu-id="10c02-113">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to specify when the command line executes.</span></span>

    <span data-ttu-id="10c02-114">您只能指定已傳送的 BG \_ 通知 \_ 作業 \_ 和 bg \_ 通知 \_ 作業 \_ 錯誤事件旗標。</span><span class="sxs-lookup"><span data-stu-id="10c02-114">You can only specify the BG\_NOTIFY\_JOB\_TRANSFERRED and BG\_NOTIFY\_JOB\_ERROR event flags.</span></span> <span data-ttu-id="10c02-115">\_ \_ 已忽略 BG 通知作業 \_ 修改旗標。</span><span class="sxs-lookup"><span data-stu-id="10c02-115">The BG\_NOTIFY\_JOB\_MODIFICATION flag is ignored.</span></span>

<span data-ttu-id="10c02-116">請注意，如果您也 [註冊接收 COM 回呼](registering-a-com-callback.md) ，而回呼介面指標有效，或 bits 呼叫的通知方法傳回成功碼，則 bits 不會執行程式。</span><span class="sxs-lookup"><span data-stu-id="10c02-116">Note that BITS will not execute the program if you also [registered to receive COM callbacks](registering-a-com-callback.md) and the callback interface pointer is valid or the notification method that BITS calls returns a success code.</span></span> <span data-ttu-id="10c02-117">但是，如果通知方法傳回失敗碼，例如 E \_ 失敗，BITS 將會執行命令列。</span><span class="sxs-lookup"><span data-stu-id="10c02-117">However, if the notification method returns a failure code, such as E\_FAIL, BITS will execute the command line.</span></span>

<span data-ttu-id="10c02-118">BITS 會呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式來啟動程式。</span><span class="sxs-lookup"><span data-stu-id="10c02-118">BITS calls the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to launch the program.</span></span> <span data-ttu-id="10c02-119">如果您指定參數字串，則第一個參數必須是程式名稱。</span><span class="sxs-lookup"><span data-stu-id="10c02-119">If you specify a parameter string, the first parameter must be the program name.</span></span>

<span data-ttu-id="10c02-120">下列範例示範如何註冊，以在發生作業傳送事件時執行程式。</span><span class="sxs-lookup"><span data-stu-id="10c02-120">The following example shows how to register to execute a program when the job-transferred event occurs.</span></span> <span data-ttu-id="10c02-121">此範例假設 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 介面指標有效。</span><span class="sxs-lookup"><span data-stu-id="10c02-121">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


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



<span data-ttu-id="10c02-122">當作業的狀態變成「BG \_ 工作」 \_ 狀態時 \_ ，BITS 會執行 pProgram 中指定的程式。</span><span class="sxs-lookup"><span data-stu-id="10c02-122">When the state of the job becomes BG\_JOB\_STATE\_TRANSFERRED, BITS executes the program specified in pProgram.</span></span> <span data-ttu-id="10c02-123">下列範例是一個簡單的程式，可接受工作識別碼作為引數。</span><span class="sxs-lookup"><span data-stu-id="10c02-123">The following example is a simple implementation of a program that takes a job identifier as an argument.</span></span> <span data-ttu-id="10c02-124">程式會假設傳遞的引數數目是正確的。</span><span class="sxs-lookup"><span data-stu-id="10c02-124">The program assumes the correct number of arguments are passed to it.</span></span>


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



 

 