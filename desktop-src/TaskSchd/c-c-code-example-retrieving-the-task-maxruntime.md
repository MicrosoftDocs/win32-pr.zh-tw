---
title: MaxRunTime 的 c/c + + 程式碼範例
description: 此範例會抓取工作可執行檔最大時間量（以毫秒為單位） () ，並在畫面上顯示該數位。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 33873fef-1b67-4010-8bda-b75e1dfa80d5
keywords:
- 正在抓取工作 MaxRunTime 工作排程器
- 正在工作排程器中抓取工作屬性，MaxRunTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fcf442e2936de48a11aea4d81de6e0bac18f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371920"
---
# <a name="cc-code-example-retrieving-the-task-maxruntime"></a><span data-ttu-id="3645e-106">C/c + + 程式碼範例：正在抓取工作 MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="3645e-106">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>

<span data-ttu-id="3645e-107">此範例會抓取工作可執行檔最大時間量（以毫秒為單位） () ，並在畫面上顯示該數位。</span><span class="sxs-lookup"><span data-stu-id="3645e-107">This example retrieves the maximum amount of time the task can run (in milliseconds) and displays that number on the screen.</span></span> <span data-ttu-id="3645e-108">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="3645e-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate;\n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetMaxRunTime to display the maximum time Test Task
  // is allowed to run.
  ///////////////////////////////////////////////////////////////////
  
  DWORD pdwRunTime;
  hr = pITask->GetMaxRunTime(&pdwRunTime);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetMaxRunTime: \n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  wprintf(L"Test Task can run for %d milliseconds\n", pdwRunTime);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="3645e-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="3645e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3645e-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="3645e-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




