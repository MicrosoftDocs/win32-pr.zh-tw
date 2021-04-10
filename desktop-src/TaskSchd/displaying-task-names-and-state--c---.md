---
title: '顯示工作名稱和狀態 (c + +) '
description: 這兩個 c + + 範例示範如何列舉工作。 其中一個範例示範如何在工作資料夾中顯示工作的資訊，而其他範例則顯示如何顯示所有執行中工作的資訊。
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6189960ef5b6e4ad78e75f156a482481f347b4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675723"
---
# <a name="displaying-task-names-and-states-c"></a>顯示工作名稱和狀態 (c + +) 

這兩個 c + + 範例示範如何列舉工作。 其中一個範例示範如何在工作資料夾中顯示工作的資訊，而其他範例則顯示如何顯示所有執行中工作的資訊。

下列程式說明如何顯示工作資料夾中所有工作的工作名稱和狀態。

**顯示工作資料夾中所有工作的工作名稱和狀態**

1.  初始化 COM 並設定一般 COM 安全性。
2.  建立 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 物件。

    此物件可讓您連接到工作排程器服務，並存取特定的工作資料夾。

3.  取得工作資料夾，其中包含您想要的相關資訊。

    使用 [**ITaskService：： GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) 方法來取得資料夾。

4.  從資料夾中取得工作的集合。

    您可以使用 [**ITaskFolder：： GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) 方法，取得工作 ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)) 的集合。

5.  取得集合中的工作數目，並列舉集合中的每個工作。

    使用 [**IRegisteredTaskCollection 的 Item 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) 來取得 [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) 實例。 每個實例都會包含集合中的工作。 然後，您可以從每個已註冊的工作中，顯示 (屬性值) 的資訊。

下列 c + + 範例顯示如何顯示根工作資料夾中所有工作的名稱和狀態。


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
********************************************************************/

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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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
    //  Get the pointer to the root task folder.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



下列程式說明如何顯示所有正在執行之工作的工作名稱和狀態。

**顯示所有正在執行之工作的工作名稱和狀態**

1.  初始化 COM 並設定一般 COM 安全性。
2.  建立 [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) 物件。

    此物件可讓您連接到工作排程器服務，並存取特定的工作資料夾。

3.  您可以使用 [**ITaskService：： GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) 方法，取得所有執行中工作的集合 ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)) 。 您可以指定以取得執行中工作的實例，包括或排除隱藏的工作。
4.  取得集合中的工作數目，並列舉集合中的每個工作。

    使用 [**IRunningTaskCollection 的 Item 屬性**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) 來取得 [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) 實例。 每個實例都會包含集合中的工作。 然後，您可以從每個已註冊的工作中，顯示 (屬性值) 的資訊。

下列 c + + 範例顯示如何顯示所有執行中工作的名稱和狀態，包括隱藏的工作。


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
********************************************************************/

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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




