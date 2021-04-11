---
title: 啟動工作的 c/c + + 程式碼範例
description: 這個範例會嘗試執行現有的工作。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: e4f38f8a-3488-4802-913b-f627ecca8bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9fa9ba112b642aa5e14abc3b408c1536c527d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372013"
---
# <a name="cc-code-example-starting-a-task"></a><span data-ttu-id="865f8-104">C/c + + 程式碼範例：啟動工作</span><span class="sxs-lookup"><span data-stu-id="865f8-104">C/C++ Code Example: Starting a Task</span></span>

<span data-ttu-id="865f8-105">這個範例會嘗試執行現有的工作。</span><span class="sxs-lookup"><span data-stu-id="865f8-105">This example attempts to run an existing task.</span></span> <span data-ttu-id="865f8-106">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="865f8-106">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>
#include<stdio.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
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
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Run to start the execution of "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  hr = pITask->Run();
  pITask->Release();

  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::Run, error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }

  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="865f8-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="865f8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="865f8-108">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="865f8-108">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




