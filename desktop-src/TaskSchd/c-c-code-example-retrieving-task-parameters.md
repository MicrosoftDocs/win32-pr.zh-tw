---
title: C/c + + 程式碼範例正在抓取工作參數
description: 這個範例會抓取執行工作時所執行的參數字串，並在畫面上顯示該字串。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: fefa668e-803f-4e05-8097-b75231ee8f72
keywords:
- 正在工作排程器中抓取工作參數
- 工作排程器的參數中抓取工作屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6adff7baeb4d4151c06ab192e336712716fb9d80
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372200"
---
# <a name="cc-code-example-retrieving-task-parameters"></a><span data-ttu-id="87542-106">C/c + + 程式碼範例：正在抓取工作參數</span><span class="sxs-lookup"><span data-stu-id="87542-106">C/C++ Code Example: Retrieving Task Parameters</span></span>

<span data-ttu-id="87542-107">這個範例會抓取執行工作時所執行的參數字串，並在畫面上顯示該字串。</span><span class="sxs-lookup"><span data-stu-id="87542-107">This example retrieves the parameter string that is executed when the task is run and displays that string on the screen.</span></span> <span data-ttu-id="87542-108">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="87542-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::GetParameters to display the parameters string 
  // associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszParameters;
  hr = pITask->GetParameters(&lpwszParameters);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetApplicationName\n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process returned parameter string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with the following parameters:\n");
  wprintf(L"  %s\n", lpwszParameters);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszParameters);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="87542-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="87542-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87542-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="87542-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




