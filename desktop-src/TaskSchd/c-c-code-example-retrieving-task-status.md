---
title: C/c + + 程式碼範例正在抓取工作狀態
description: 這個範例會抓取工作的目前狀態，並將它顯示在螢幕上。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 7ad40ac7-2363-481a-87fa-18dcf2d749b3
keywords:
- 正在抓取工作狀態工作排程器
- 工作排程器的工作狀態中，正在抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068e2be84750ac8fead97eac146400139dee85fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932181"
---
# <a name="cc-code-example-retrieving-task-status"></a><span data-ttu-id="84d3d-106">C/c + + 程式碼範例：正在抓取工作狀態</span><span class="sxs-lookup"><span data-stu-id="84d3d-106">C/C++ Code Example: Retrieving Task Status</span></span>

<span data-ttu-id="84d3d-107">這個範例會抓取工作的目前狀態，並將它顯示在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="84d3d-107">This example retrieves the current status of the task and displays it on the screen.</span></span> <span data-ttu-id="84d3d-108">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="84d3d-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::GetStatus. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HRESULT phrStatus;
  
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The status of Test Task is: ");
  
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;
  case SCHED_S_TASK_DISABLED:
       wprintf(L"  SCHED_S_TASK_DISABLED\n");
       break;
  case SCHED_S_TASK_HAS_NOT_RUN:
       wprintf(L"  SCHED_S_TASK_HAS_NOT_RUN\n");
       break;
  case SCHED_S_TASK_NOT_SCHEDULED:
       wprintf(L"  SCHED_S_TASK_NOT_SCHEDULED\n");
       break;
  case SCHED_S_TASK_NO_MORE_RUNS:
       wprintf(L"  SCHED_S_TASK_NO_MORE_RUNS\n");
       break;
  case SCHED_S_TASK_NO_VALID_TRIGGERS:
       wprintf(L"  SCHED_S_TASK_NO_VALID_TRIGGERS\n");
       break;
  default:
       wprintf(L"  unknown status flag!\n"); 
  }
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="84d3d-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="84d3d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84d3d-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="84d3d-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




