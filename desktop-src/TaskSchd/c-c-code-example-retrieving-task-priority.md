---
title: C/c + + 程式碼範例正在抓取工作優先順序
description: 此範例會抓取工作的優先權層級，並顯示幕幕上工作目錄的路徑。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 6e7eccce-406a-4827-8fe2-abe93251668a
keywords:
- 正在抓取工作優先權工作排程器
- 正在抓取工作屬性工作排程器，優先權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9b32b5b4a6e66539ce1a65ab41488f96418d29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969454"
---
# <a name="cc-code-example-retrieving-task-priority"></a>C/c + + 程式碼範例：正在抓取工作優先順序

此範例會抓取工作的優先權層級，並顯示幕幕上工作目錄的路徑。 此範例假設本機電腦上已有工作和測試工作。


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
     wprintf(L"Failed calling ITaskScheduler::Activate: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetPriority to retrieve the priority level 
  // of Test Task.
  ///////////////////////////////////////////////////////////////////
  
  DWORD pdwPriority;
  hr = pITask->GetPriority(&pdwPriority);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetPriority: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  if(pdwPriority == HIGH_PRIORITY_CLASS)
  {
     wprintf(L"Test Task is a high priority task.\n");
  }
  else
  {
     wprintf(L"Test Task is not a high priority task.\n");
  }
  
  CoUninitialize();
  return 0;
  
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




