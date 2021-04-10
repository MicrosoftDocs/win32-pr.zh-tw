---
title: " (c + +) 的登入觸發程式範例"
description: 這個 c + + 範例會示範如何建立排定在使用者登入時執行「記事本」的工作。
ms.assetid: 15647234-8d1f-4d75-b215-92927b300c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137155a28a84a981b6013b6651f327a8c6bb4474
ms.sourcegitcommit: f19e3b30abea739d83178cdc8f2478eb4905f1d0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/04/2020
ms.locfileid: "104316693"
---
# <a name="logon-trigger-example-c"></a><span data-ttu-id="d96a1-103"> (c + +) 的登入觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="d96a1-103">Logon Trigger Example (C++)</span></span>

<span data-ttu-id="d96a1-104">這個 c + + 範例會示範如何建立排定在使用者登入時執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="d96a1-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="d96a1-105">此工作包含登入觸發程式，可指定開始工作的開始界限，以及指定使用者的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="d96a1-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="d96a1-106">此工作會使用 Administrators 群組作為安全性內容來執行工作，以進行註冊。</span><span class="sxs-lookup"><span data-stu-id="d96a1-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="d96a1-107">下列程式描述如何排程工作，以在使用者登入時啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d96a1-107">The following procedure describes how to schedule a task to start an executable when a user logs on.</span></span>

<span data-ttu-id="d96a1-108">**排定在使用者登入時啟動 [記事本]**</span><span class="sxs-lookup"><span data-stu-id="d96a1-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="d96a1-109">初始化 COM 並設定一般 COM 安全性。</span><span class="sxs-lookup"><span data-stu-id="d96a1-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="d96a1-110">建立 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 物件。</span><span class="sxs-lookup"><span data-stu-id="d96a1-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="d96a1-111">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="d96a1-111">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="d96a1-112">取得要在其中建立工作的工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="d96a1-112">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="d96a1-113">您可以使用 [**ITaskService：： GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) 方法來取得資料夾，並使用 [**ITaskService：： NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) 方法來建立 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 物件。</span><span class="sxs-lookup"><span data-stu-id="d96a1-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="d96a1-114">使用 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 物件定義工作的相關資訊，例如工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d96a1-114">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="d96a1-115">使用 [**ITaskDefinition 的 RegistrationInfo 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) 和 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) 介面的其他屬性來定義工作資訊。</span><span class="sxs-lookup"><span data-stu-id="d96a1-115">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="d96a1-116">使用 [**ITaskDefinition 的 trigger 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) 來建立登入觸發程式，以存取工作的 [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) 介面。</span><span class="sxs-lookup"><span data-stu-id="d96a1-116">Create a logon trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) interface for the task.</span></span>

    <span data-ttu-id="d96a1-117">您可以使用 [**ITriggerCollection：： Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) 方法來指定要建立登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d96a1-117">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a logon trigger.</span></span> <span data-ttu-id="d96a1-118">您可以設定觸發程式的開始界限和 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) 屬性，如此一來，當使用者在開始界限之後登入時，就會排定工作的動作執行。</span><span class="sxs-lookup"><span data-stu-id="d96a1-118">You can set the start boundary and the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the user logs on after the start boundary.</span></span>

6.  <span data-ttu-id="d96a1-119">使用 ITaskDefinition 的 [ [**動作] 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) 來存取工作的 [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) 介面，以建立工作要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="d96a1-119">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="d96a1-120">使用 [**IActionCollection：： Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) 方法可指定您想要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="d96a1-120">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="d96a1-121">這個範例會使用 [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) 物件，代表執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="d96a1-121">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="d96a1-122">使用 [**ITaskFolder：： RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="d96a1-122">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="d96a1-123">下列 c + + 範例顯示如何排程工作，以在使用者登入時執行 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="d96a1-123">The following C++ example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```C++
/**********************************************************************
 This sample schedules a task to start notepad.exe when a user logs on. 
**********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")

using namespace std;


int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Logon Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to create an instance of ITaskService: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to create a task definition: %x", hr);
        pRootFolder->Release();
        CoUninitialize();
        return 1;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author(L"Author Name");
    pRegInfo->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task. 
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);
    pSettings->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the logon trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the logon trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_LOGON, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    ILogonTrigger *pLogonTrigger = NULL;       
    hr = pTrigger->QueryInterface( 
            IID_ILogonTrigger, (void**) &pLogonTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for ILogonTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pLogonTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pLogonTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
    
    hr = pLogonTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);    
    
    //  Define the user.  The task will execute when the user logs on.
    //  The specified user must be a user on this computer.  
    hr = pLogonTrigger->put_UserId( _bstr_t( L"DOMAIN\\UserName" ) );  
    pLogonTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot add user ID to logon trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
        
    //  Create the action, specifying that it is an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot set path of executable: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(L"S-1-5-32-544"),
            _variant_t(), 
            TASK_LOGON_GROUP,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    // Clean up
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d96a1-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="d96a1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d96a1-125">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="d96a1-125">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




