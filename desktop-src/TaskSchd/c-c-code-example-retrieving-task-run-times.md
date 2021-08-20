---
title: C/c + + 程式碼範例正在抓取工作執行時間
description: 這個範例會抓取工作的執行時間，並將它們顯示在畫面上。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: ad9eb4a7-f42b-4f5a-86a3-05d02dc88f97
keywords:
- 工作排程器中取出工作執行時間
- 工作排程器工作執行時間，正在抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6159922aede5574f0371239d1e7985e745d93a290f04a1e5453a181660d96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943910"
---
# <a name="cc-code-example-retrieving-task-run-times"></a>C/c + + 程式碼範例：正在抓取工作執行時間

這個範例會抓取工作的執行時間，並將它們顯示在畫面上。 此範例假設本機電腦上已有工作和測試工作。


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
  
  // Release the ITaskScheduler interface.
  pITS->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetRunTimes and display the next five run times for 
  // this task.
  ///////////////////////////////////////////////////////////////////
  
  SYSTEMTIME stNow;
  LPSYSTEMTIME pstListOfTimes;
  LPSYSTEMTIME pstListBegin;
  WORD wCountOfRuns = 5;
  
  GetSystemTime(&stNow);
  hr = pITask->GetRunTimes(&stNow,
                           NULL,
                           &wCountOfRuns,
                           &pstListBegin);
  pstListOfTimes = pstListBegin;
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetRunTimes: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }
  
  wprintf(L"The next %u runtimes for this task are: \n",wCountOfRuns);
  
  for (WORD i = 0; i < wCountOfRuns; i++)
  {
    wprintf(L"\t%u - %u/%u/%u \t %u:%u\n", i+1, pstListOfTimes->wMonth,
                                                pstListOfTimes->wDay,
                                                pstListOfTimes->wYear,
                                                pstListOfTimes->wHour,
                                                pstListOfTimes->wMinute);
    pstListOfTimes++;
  }

  CoTaskMemFree(pstListBegin);
  CoTaskMemFree(pstListOfTimes);
  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




