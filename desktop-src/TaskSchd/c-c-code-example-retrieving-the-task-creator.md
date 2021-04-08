---
title: C/c + + 程式碼範例，以抓取工作建立者
description: 這個範例會抓取工作建立者的名稱，並將它顯示在螢幕上。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 02554ce1-2d52-48e9-95f1-d5d480519035
keywords:
- 正在抓取工作建立者工作排程器
- 工作排程器，工作建立者正在抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546d676a5f1ac4b99595e47f2514b84e38f4c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021348"
---
# <a name="cc-code-example-retrieving-the-task-creator"></a><span data-ttu-id="c7d35-106">C/c + + 程式碼範例：正在抓取工作建立者</span><span class="sxs-lookup"><span data-stu-id="c7d35-106">C/C++ Code Example: Retrieving the Task Creator</span></span>

<span data-ttu-id="c7d35-107">這個範例會抓取工作建立者的名稱，並將它顯示在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="c7d35-107">This example retrieves the name of the creator of the task and displays it on the screen.</span></span> <span data-ttu-id="c7d35-108">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="c7d35-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::GetCreator. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR ppwszCreator;
  
  hr = pITask->GetCreator(&ppwszCreator);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetCreator: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The creator of Test Task is: ");
  wprintf(L"  %s\n",ppwszCreator);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free the string.
  ///////////////////////////////////////////////////////////////////
  CoTaskMemFree(ppwszCreator);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="c7d35-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7d35-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7d35-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="c7d35-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




