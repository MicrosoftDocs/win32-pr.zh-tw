---
title: C/c + + 程式碼範例設定工作帳戶資訊
description: 此範例會設定已知工作的帳戶資訊。 這個範例假設工作 \ 0034; test task \ 0034;已經存在於本機電腦上，且工作排程器服務正在執行中。
ms.assetid: ab865f70-f8d1-411e-b637-b1b1028ccf62
keywords:
- 設定帳戶資訊工作排程器
- 設定工作專案屬性工作排程器、帳戶資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5673653fa5dfe4875fb57a00535b30ae384e91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021160"
---
# <a name="cc-code-example-setting-task-account-information"></a><span data-ttu-id="62a7b-106">C/c + + 程式碼範例：設定工作帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="62a7b-106">C/C++ Code Example: Setting Task Account Information</span></span>

<span data-ttu-id="62a7b-107">此範例會設定已知工作的帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="62a7b-107">This example sets the account information for a known task.</span></span> <span data-ttu-id="62a7b-108">此範例假設本機電腦上已有「測試工作」工作，且工作排程器服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="62a7b-108">This example assumes that the task "test task" already exists on the local computer and that the Task Scheduler service is running.</span></span>


```C++
#define _WIN32_DCOM
#include <windows.h>
#include <initguid.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

#pragma comment(lib, "comsupp.lib")
#pragma comment(lib, "credui.lib")


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  
  hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      wprintf(L"Failed calling CoCreateInstance. ");
      CoUninitialize();
      return 1;
    }
  }
  else
  {
    wprintf(L"Failed calling CoInitializeEx. ");
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
  
    //  ------------------------------------------------------
    //  Securely get the user name and password. 
    CREDUI_INFO cui;
    TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH] = "";
    TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH] = "";
    BOOL fSave;
    DWORD dwErr;

    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    //  Ensure that MessageText and CaptionText identify
    //  what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Account information for task registration:");
    cui.pszCaptionText = TEXT("Enter Account Information for Task Registration");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    //  Create the UI asking for the credentials.
    dwErr = CredUIPromptForCredentials(
        &cui,                             //  CREDUI_INFO structure
        TEXT(""),                         //  Target for credentials
        NULL,                             //  Reserved
        0,                                //  Reason
        pszName,                          //  User name
        CREDUI_MAX_USERNAME_LENGTH,       //  Max number for user name
        pszPwd,                           //  Password
        CREDUI_MAX_PASSWORD_LENGTH,       //  Max number for password
        &fSave,                           //  State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |  //  Flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr)
    {
        wprintf(L"Failed calling ITask::SetAccountInformation: ");
        wprintf(L"error = 0x%x\n",dwErr);
        pITask->Release();    
        CoUninitialize();
        return 1;      
    }

  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetAccountInformation to specify the account name
  // and the account password for Test Task.
  ///////////////////////////////////////////////////////////////////
  hr = pITask->SetAccountInformation((LPCWSTR)pszName, 
            (LPCWSTR)pszPwd);

  SecureZeroMemory(pszName, sizeof(pszName));
  SecureZeroMemory(pszPwd, sizeof(pszPwd));
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetAccountInformation: ");
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
  
  wprintf(L"Set the account name and password.");  
  CoUninitialize();
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="62a7b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="62a7b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62a7b-110">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="62a7b-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




