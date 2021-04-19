---
title: C/c + + 程式碼範例，此範例會取出工作 MostRecentRun 時間
description: 此範例會抓取工作上次執行的時間，並顯示在畫面上。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 683ff1e1-1cb0-4ef7-bca2-9c3a2b4d1bd0
keywords:
- 正在將工作最新的執行時間抓取工作排程器
- 工作排程器、工作最新的執行時間，正在抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cae40de306d79628fa10230091c571e776c5e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967828"
---
# <a name="cc-code-example-retrieving-the-task-mostrecentrun-time"></a><span data-ttu-id="160a3-106">C/c + + 程式碼範例：取出工作 MostRecentRun 時間</span><span class="sxs-lookup"><span data-stu-id="160a3-106">C/C++ Code Example: Retrieving the Task MostRecentRun Time</span></span>

<span data-ttu-id="160a3-107">此範例會抓取工作上次執行的時間，並顯示在畫面上。</span><span class="sxs-lookup"><span data-stu-id="160a3-107">This example retrieves the time the task was last run and displays it on the screen.</span></span> <span data-ttu-id="160a3-108">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="160a3-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <wchar.h>
#include <stdio.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>


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
  LPCWSTR lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release ITaskScheduler interface.
  pITS->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetMostRecentRunTime and display the most recent 
  // run time of this task.
  ///////////////////////////////////////////////////////////////////

  SYSTEMTIME pstLastRun;
    
  hr = pITask->GetMostRecentRunTime(&pstLastRun);
  
  // Release the ITask interface.
  pITask->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetMostRecentRunTime: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }

  wprintf(L"The most recent run time for this task was: \n");
  wprintf(L"  %u/%u/%u \t %u:%02u\n", pstLastRun.wMonth,
                                      pstLastRun.wDay,
                                      pstLastRun.wYear,
                                      pstLastRun.wHour,
                                      pstLastRun.wMinute);
 

  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="160a3-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="160a3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="160a3-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="160a3-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




