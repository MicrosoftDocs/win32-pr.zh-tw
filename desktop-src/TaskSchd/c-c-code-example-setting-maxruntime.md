---
title: C/c + + 程式碼範例設定 MaxRunTime
description: 此範例會設定已知工作的執行時間上限，以毫秒為單位)  (設定。 此範例假設本機電腦上已有工作和測試工作。
ms.assetid: ccfa3c01-870b-4b44-a493-9934ca1e51e4
keywords:
- 設定工作屬性工作排程器，執行時間上限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d75470a19a7b2a142a99c5f0c307404fc1bc1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672432"
---
# <a name="cc-code-example-setting-maxruntime"></a><span data-ttu-id="fe42f-105">C/c + + 程式碼範例：設定 MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="fe42f-105">C/C++ Code Example: Setting MaxRunTime</span></span>

<span data-ttu-id="fe42f-106">此範例會設定已知工作的執行時間上限，以毫秒為單位)  (設定。</span><span class="sxs-lookup"><span data-stu-id="fe42f-106">This example sets the maximum run time (set in milliseconds) of a known task.</span></span> <span data-ttu-id="fe42f-107">此範例假設本機電腦上已有工作和測試工作。</span><span class="sxs-lookup"><span data-stu-id="fe42f-107">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::SetMaxRunTime to specify the maximum amount
  // of time the task will run.
  ///////////////////////////////////////////////////////////////////
  DWORD dwMaxRunTime = (1000*60*5);
  
  hr = pITask->SetMaxRunTime(dwMaxRunTime);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetMaxRunTime: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }
  
  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"The maximum run time is set to 5 minutes.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="fe42f-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe42f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe42f-109">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="fe42f-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




