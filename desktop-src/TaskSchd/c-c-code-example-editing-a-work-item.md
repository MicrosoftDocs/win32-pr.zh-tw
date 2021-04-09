---
title: 編輯工作專案的 c/c + + 程式碼範例
description: 這個範例會顯示已知工作的屬性頁，並允許使用者編輯工作專案的屬性。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: 526bc354-3585-43aa-a727-03c04e607a64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec02a7b7b12f350e7ed61220c9bdeebe920fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021460"
---
# <a name="cc-code-example-editing-a-work-item"></a><span data-ttu-id="70aab-104">C/c + + 程式碼範例：編輯工作專案</span><span class="sxs-lookup"><span data-stu-id="70aab-104">C/C++ Code Example: Editing a Work Item</span></span>

<span data-ttu-id="70aab-105">這個範例會顯示已知工作的屬性頁，並允許使用者編輯工作專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="70aab-105">This example displays the property pages for a known task and allows a user to edit the properties of the work item.</span></span> <span data-ttu-id="70aab-106">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="70aab-106">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  //Release ITaskScheduler interface
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate, ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::EditWorkItem. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HWND hParent = NULL;
  DWORD dwReserved = 0;
  
  hr = pITask->EditWorkItem(hParent,
                            dwReserved);
  // Release ITask interface
  pITask->Release();
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::EditWorkItem, ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="70aab-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="70aab-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70aab-108">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="70aab-108">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




