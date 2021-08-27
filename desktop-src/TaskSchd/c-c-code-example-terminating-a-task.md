---
title: 終止工作的 c/c + + 程式碼範例
description: 此範例會驗證已知工作的狀態，並在工作正在執行時終止該工作。
ms.assetid: 2131b966-6179-4a80-a3f1-ebb8967a7a90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65b470d2fdeb3ec308d57dbc108851eb59f99f63b00dd446be4f80744e17f5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100488"
---
# <a name="cc-code-example-terminating-a-task"></a>C/c + + 程式碼範例：終止工作

此範例會驗證已知工作的狀態，並在工作正在執行時終止該工作。


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
  // Call ITask::GetStatus. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HRESULT phrStatus;
  
  hr = pITask->GetStatus(&phrStatus);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Terminate if the status is SCHED_S_TASK_RUNNING.
  ///////////////////////////////////////////////////////////////////
  
  if(phrStatus==SCHED_S_TASK_RUNNING)
  {
    hr = pITask->Terminate();
    if (FAILED(hr))
    {
      wprintf(L"Failed calling ITask::Terminate: ");
      wprintf(L"error = 0x%x\n",hr);
      pITask->Release();
      CoUninitialize();
      return 1;
    }
  wprintf(L"Test Task is terminated.\n");
  }
  else
  {
    wprintf(L"Test Task is not running.\n");
  }

  // Release the ITask interface.
  pITask->Release();
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




