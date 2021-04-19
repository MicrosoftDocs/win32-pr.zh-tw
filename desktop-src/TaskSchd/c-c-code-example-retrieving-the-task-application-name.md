---
title: C/c + + 程式碼範例，以抓取工作應用程式名稱
description: 此範例會取得與指定工作相關聯的應用程式名稱，並在畫面上顯示該名稱。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 7cf20a14-fee3-4507-83a9-4a081a9783fc
keywords:
- 工作排程器中取出應用程式名稱
- 正在工作排程器應用程式名稱中抓取工作屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb590900cf7b4c6d8821560e91e2f05c21c0f73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996149"
---
# <a name="cc-code-example-retrieving-the-task-application-name"></a>C/c + + 程式碼範例：正在抓取工作應用程式名稱

此範例會取得與指定工作相關聯的應用程式名稱，並在畫面上顯示該名稱。 此範例假設本機電腦上已有工作和測試工作。


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
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetApplicationName to display the name of the 
  // application associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszApplicationName;
  hr = pITask->GetApplicationName(&lpwszApplicationName);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetApplicationName\n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process the returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with: %s\n", lpwszApplicationName);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszApplicationName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




