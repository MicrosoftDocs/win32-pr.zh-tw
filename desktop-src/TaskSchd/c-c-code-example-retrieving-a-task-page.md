---
title: C/c + + 程式碼範例-正在抓取工作頁面
description: 此範例會取出並顯示已知工作的工作頁面。 請注意，在此範例中，當不再需要所有介面時，就會釋放它們。
ms.assetid: f234f5b3-d668-44c3-8d03-c333cfe3acde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1db7bd6b472df53ff47629dbc1fcb9ecf13fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932130"
---
# <a name="cc-code-example-retrieving-a-task-page"></a><span data-ttu-id="5e926-104">C/c + + 程式碼範例：取出工作頁面</span><span class="sxs-lookup"><span data-stu-id="5e926-104">C/C++ Code Example: Retrieving a Task Page</span></span>

<span data-ttu-id="5e926-105">此範例會取出並顯示已知工作的工作頁面。</span><span class="sxs-lookup"><span data-stu-id="5e926-105">This example retrieves and displays the Task page of a known task.</span></span> <span data-ttu-id="5e926-106">請注意，在此範例中，當不再需要所有介面時，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="5e926-106">Note that in this example, all interfaces are released when they are no longer needed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5e926-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e926-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e926-108">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="5e926-108">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




