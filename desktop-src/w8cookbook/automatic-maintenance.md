---
title: 適用于 Windows) 的自動維護 (相容性操作手冊
description: 自動維護
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463837"
---
# <a name="automatic-maintenance"></a>自動維護

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

Windows 取決於收件匣和協力廠商維護活動的許多價值新增，包括 Windows Update 和自動磁碟重組，以及防病毒軟體更新和掃描。 此外，企業經常使用維護活動（例如網路存取保護）來 (NAP) 掃描，以協助在所有企業工作站上強制執行安全性標準。

Windows 中的維護活動是設計成在背景中執行，使用者互動受限，而且對效能和能源效率的影響最小。 不過，在 Windows 7 及更早版本中，效能和能源效率仍會受到影響，因為 Windows 中的多個維護活動會有不具決定性且廣泛的不同排程。 當使用者主動使用電腦時，在維護活動執行時，會降低使用者的回應能力。 應用程式也經常要求使用者更新其軟體和執行背景維護，以及將使用者導向多種體驗，包括行動中心、主控台、Windows Update、工作排程器 MMC 嵌入式管理單元和協力廠商控制項。

自動維護的目標是要將 Windows 中的所有背景維護活動結合在一起，讓協力廠商開發人員將其維護活動新增至 Windows，而不會對效能和能源效率造成負面影響。 此外，自動維護可讓使用者和企業控制維護活動排程和設定。

**重要問題**

自動維護的設計目的是要解決 Windows 中維護活動的下列問題：

-   期限排程
-   資源使用率衝突
-   節能
-   使用者的透明度

## <a name="functionality"></a>功能

自動維護有助於提高空閒效率，並允許所有活動以及時且優先的方式執行。 它也有助於讓您一致地查看及控制維護活動，並讓協力廠商開發人員將其維護活動新增至 Windows，而不會對效能和能源效率造成負面影響。 若要這樣做，它會提供完全自動模式、使用者起始模式、自動停止、期限和通知，以及企業控制。 這些都是如下所述。

**完全自動模式**

此預設模式可讓您在電腦閒置時間和排程時間進行智慧型排程—執行和自動暫停維護活動，不需要使用者介入。 使用者可以設定每週或每日排程。 所有維護活動都是非互動式的，並且會以無訊息模式執行。

當系統不太可能在使用中時，電腦會自動從睡眠狀態恢復，並遵循電源管理原則（如果是膝上型電腦，則預設為只允許喚醒電源）。 高電源的完整系統資源可用來儘快完成維護活動。 如果系統從睡眠狀態恢復為自動維護，則會要求其返回睡眠狀態。

任何與活動（例如設定）相關的必要使用者互動都是在自動維護執行以外執行。

**使用者起始模式**

如果使用者需要準備旅遊、預期會有長時間的電池電力，或是想要優化效能和回應性，則可以選擇視需要起始自動維護。 使用者可以設定自動維護屬性，包括自動執行排程。 他們可以查看自動維護執行的目前狀態，也可以視需要停止自動維護。

**自動停止**

如果使用者開始與電腦互動，自動維護會自動停止目前正在執行的維護活動。 當系統復原閒置狀態時，維護活動將會繼續。

> [!Note]  
> 自動維護中的所有活動都必須支援在2秒或更短時間內停止。 使用者應該會收到活動已停止的通知。

 

**期限和通知**

重要維護活動必須在預先定義的時間範圍內執行。 如果重要工作無法在指定的時間內執行，自動維護將會在下一次可用的系統空閒機會時自動開始執行。 但是，如果工作狀態維持在期限之後，自動維護會通知使用者有關活動，並提供手動執行自動維護的選項。 所有排程進行維護的工作都會執行，雖然最耗盡的工作優先。 此活動可能會影響系統的回應性和效能;因此，自動維護會通知使用者正在執行重要的維護活動。

**企業控制**

企業 IT 專業人員應該能夠判斷何時自動維護在其 Windows 系統上執行、透過標準化的管理介面強制執行該排程，以及取得自動維護執行嘗試狀態的相關事件資料。 此外，IT 專業人員應該能夠透過標準管理介面從遠端叫用特定的自動維護活動。 每次自動維護執行時，狀態報表，包括無法執行自動維護的通知，因為使用者已手動暫停活動，所以會執行。 IT 專業人員應該考慮將登入腳本移至自動維護，讓使用者的登入體驗更快。

## <a name="creating-an-automatic-maintenance-task"></a>建立自動維護工作

本節將詳細說明開發人員如何使用 XML 或 C 語言的工作定義來建立工作。 請記住，維護活動不應該啟動任何需要使用者互動的使用者介面，因為自動維護完全無訊息，並且在使用者不存在時執行。 事實上，如果使用者在自動維護期間與電腦互動，則在下一個閒置的期間內，將會結束處理中的任何工作。

**使用 XML**

工作排程器包含內建的命令列工具，schtasks.exe，可匯入 XML 格式的工作定義。 工作定義的架構記載于 https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx 。 以下是在 XML 中定義自動維護工作的範例。


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



若要將工作儲存在 Windows 電腦上，請將上述 XML 儲存為文字檔，並使用此命令列：

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**使用 C**

也可以使用 C 程式碼建立自動維護工作。 以下是可用於設定工作自動維護設定的程式碼範例：


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
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
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a>驗證工作

驗證工作是否已成功建立，並在維護過程中執行。

**正在驗證工作建立**

使用這個命令列將工作定義匯出至檔案，並確定工作定義符合預期：

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**正在驗證工作執行**

執行此命令列以啟動工作，並驗證工作排程器 UI (taskschd.msc) 顯示工作已執行：

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>資源

-   [工作排程2。0](/previous-versions/bb756979(v=msdn.10))

 

 