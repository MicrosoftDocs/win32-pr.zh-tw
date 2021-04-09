---
title: C/c + + 程式碼範例，正在抓取工作帳戶資訊
description: 這個程式碼範例會取出已知工作的帳戶資訊，並在畫面上顯示帳戶名稱。 此範例假設本機電腦上已有工作和測試工作，且工作排程器正在執行。
ms.assetid: ef330276-a063-42c6-a837-fddb4723091b
keywords:
- 正在抓取工作帳戶資訊工作排程器
- 工作排程器的帳戶資訊中，正在抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1102ce0c2a2a98e66c1ac943eeab0593fe75e189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932293"
---
# <a name="cc-code-example-retrieving-task-account-information"></a><span data-ttu-id="7640e-106">C/c + + 程式碼範例：正在抓取工作帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="7640e-106">C/C++ Code Example: Retrieving Task Account Information</span></span>

<span data-ttu-id="7640e-107">這個程式碼範例會取出已知工作的帳戶資訊，並在畫面上顯示帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7640e-107">This code example retrieves the account information of a known task and displays the account name on the screen.</span></span> <span data-ttu-id="7640e-108">此範例假設本機電腦上已有工作和測試工作，且工作排程器正在執行。</span><span class="sxs-lookup"><span data-stu-id="7640e-108">This example assumes that the task and the test task already exist on the local computer and that the Task Scheduler is running.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  //Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetAccountInformation. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR pwszAccountName;
  
  hr = pITask->GetAccountInformation(&pwszAccountName);
  
  // Release the ITask interface.
  pITask->Release();

  if(hr == SCHED_E_NO_SECURITY_SERVICES)
  {
    wprintf(L"Error: SCHED_E_NO_SECURITY_SERVICES");
    wprintf(L"Security services are available only on Windows Server 2003");
    wprintf(L", Windows XP, and Windows 2000.");
    CoUninitialize();
    return 1;

  }
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetAccountInformation: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The account name for Test Task is: ");
  wprintf(L"  %s\n",pwszAccountName);
  
  CoTaskMemFree(pwszAccountName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="7640e-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7640e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7640e-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="7640e-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




