---
title: C/c + + 程式碼範例-正在抓取工作頁面
description: 此範例會取出並顯示已知工作的工作頁面。 請注意，在此範例中，當不再需要所有介面時，就會釋放它們。
ms.assetid: f234f5b3-d668-44c3-8d03-c333cfe3acde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894ea88289203ea35e85005b4aa30f22bad7a2cd07150ac5a5ee83f1c9f8a22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139671"
---
# <a name="cc-code-example-retrieving-a-task-page"></a>C/c + + 程式碼範例：取出工作頁面

此範例會取出並顯示已知工作的工作頁面。 請注意，在此範例中，當不再需要所有介面時，就會釋放它們。


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
  // Call ITask::QueryInterface to retrieve the IProvideTaskPage 
  // interface, and call IProvideTaskPage::GetPage to retrieve the 
  // task page.
  ///////////////////////////////////////////////////////////////////
  TASKPAGE tpType = TASKPAGE_TASK;
  BOOL fPersistChanges = TRUE;
  HPROPSHEETPAGE phPage; 
  
  IProvideTaskPage *pIProvTaskPage;
  hr = pITask->QueryInterface(IID_IProvideTaskPage,
                              (void **)&pIProvTaskPage);
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::QueryInterface: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  hr = pIProvTaskPage->GetPage(tpType,
                               fPersistChanges,
                               &phPage);
  
  // Release the IProvideTaskPage interface.
  pIProvTaskPage->Release();
  
  if (FAILED(hr))
  {
     wprintf(L"Failed calling IProvideTaskPage::GetPage: ");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  //////////////////////////////////////////////////////////////////
  // Display the page using additional code.
  //////////////////////////////////////////////////////////////////
  
  PROPSHEETHEADER psh;
  ZeroMemory(&psh, sizeof(PROPSHEETHEADER));
  psh.dwSize = sizeof(PROPSHEETHEADER);
  psh.dwFlags = PSH_DEFAULT | PSH_NOAPPLYNOW;
  psh.phpage = &phPage;
  psh.nPages = 1;

  int psResult = PropertySheet(&psh);
  if (psResult <= 0)
  {
    wprintf(L"Failed to create the property page: ");
    wprintf(L"0x%x\n", GetLastError());
  }
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




