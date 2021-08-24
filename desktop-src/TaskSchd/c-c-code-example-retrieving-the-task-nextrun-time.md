---
title: C/c + + 程式碼範例，此範例會取出工作 NextRun 時間
description: 此範例會在下一次排程執行工作時抓取，並在畫面上顯示該時間。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 2134a188-2fd4-4b55-bd9e-3363772080c0
keywords:
- 在下次執行時間工作排程器中取出工作
- 工作排程器中的工作專案屬性，工作下一次執行時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0472f867aea83457bbb4cb77a5a092b8c302f793b0df052e4addb0422adedb5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738498"
---
# <a name="cc-code-example-retrieving-the-task-nextrun-time"></a>C/c + + 程式碼範例：取出工作 NextRun 時間

此範例會在下一次排程執行工作時抓取，並在畫面上顯示該時間。 此範例假設本機電腦上已有工作和測試工作。


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
  // Call ITaskScheduler::Activate to get the task object.
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
  // Call ITask::GetNextRunTime and display next run time of 
  // this task.
  ///////////////////////////////////////////////////////////////////

  SYSTEMTIME pstNextRun;
    
  hr = pITask->GetNextRunTime(&pstNextRun);
  
  // Release the ITask interface.
  pITask->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetNextRunTime: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }

  wprintf(L"The next runtime for this task is: \n");
  wprintf(L"  %u/%u/%u \t %u:%02u\n", pstNextRun.wMonth,
                                      pstNextRun.wDay,
                                      pstNextRun.wYear,
                                      pstNextRun.wHour,
                                      pstNextRun.wMinute);
 

  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




