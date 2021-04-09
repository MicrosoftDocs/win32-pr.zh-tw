---
title: C/c + + 程式碼範例設定應用程式名稱
description: 此範例會設定與已知工作相關聯的應用程式名稱。 這個範例假設工作 \ 0034; test task \ 0034;已經存在於本機電腦上，且工作排程器服務正在執行中。
ms.assetid: 1d86f945-0f13-4a7f-8123-df7e63a02238
keywords:
- 設定工作屬性工作排程器，應用程式名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5ce664079217778e08dcd44ef8c646a4c4eaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021543"
---
# <a name="cc-code-example-setting-application-name"></a><span data-ttu-id="09a2f-105">C/c + + 程式碼範例：設定應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="09a2f-105">C/C++ Code Example: Setting Application Name</span></span>

<span data-ttu-id="09a2f-106">此範例會設定與已知工作相關聯的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="09a2f-106">This example sets the name of the application associated with a known task.</span></span> <span data-ttu-id="09a2f-107">此範例假設本機電腦上已有「測試工作」工作，且工作排程器服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="09a2f-107">This example assumes that the task "test task" already exists on the local computer and that the Task Scheduler service is running.</span></span>


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
  // Call ITask::SetApplicationName to specify the Application name
  // for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszApplicationName = L"C:\\Windows\\System32\\notepad.exe";
 
  hr = pITask->SetApplicationName(pwszApplicationName);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetApplicationName: ");
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
  
  wprintf(L"Set the application name for Test Task.\n");  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="09a2f-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="09a2f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a2f-109">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="09a2f-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




