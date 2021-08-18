---
title: 搭配次要安裝程式使用重新開機管理員
description: 下列程式說明如何使用重新開機管理員與主要和次要安裝程式。
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aefb1f9658752677e7850e939fcb6a3c4c6047c5efc2dc0ceb06ec0f51900ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009986"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a>搭配次要安裝程式使用重新開機管理員

下列程式說明如何使用重新開機管理員與主要和次要安裝程式。

使用主要和次要安裝程式時，主要安裝程式會控制使用者介面。

**搭配使用重新開機管理員與主要和次要安裝程式**

1.  主要安裝程式會呼叫 [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) 函數來啟動重新開機管理員會話，並取得會話控制碼和金鑰。
2.  主要安裝程式會啟動或聯繫次要安裝程式，並提供在上一個步驟中取得的工作階段金鑰。
3.  次要安裝程式會使用工作階段金鑰呼叫 [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) 函式，以加入重新開機管理員會話。 只有當兩個安裝程式都在相同的使用者內容中執行時，次要安裝程式才可以加入主要安裝程式啟動的會話。
4.  主要和次要安裝程式會呼叫 [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) 函式來註冊資源。 重新開機管理員只能使用已註冊的資源來判斷哪些應用程式和服務必須關閉並重新啟動。 所有可能受安裝影響的資源都應該向會話註冊。 您可以依檔案名、服務簡短名稱或 [**RM 的 \_ 唯一 \_ 進程**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) 結構來識別資源。
5.  主要安裝程式會呼叫 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) 函式，以取得 [**RM \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) 結構的陣列，其中列出必須關閉和重新開機的所有應用程式和服務。

    如果 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)函數所傳回的 *lpdwRebootReason* 參數值為非零值，則重新開機管理員無法透過關閉應用程式或服務來釋放已註冊的資源。 在此情況下，需要系統關機並重新啟動，才能繼續安裝。 主要安裝程式應該會提示使用者輸入動作、停止程式或服務，或排程系統關機並重新啟動。

    如果 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)函數所傳回之 *lpdwRebootReason* 參數的值為零，則安裝程式應該呼叫 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)函數。 這會關閉使用已註冊資源的服務和應用程式。 主要和次要安裝程式接著應執行完成安裝所需的系統修改。 最後，主要安裝程式應該呼叫 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 函式，讓重新開機管理員可以重新開機已關閉的應用程式，並已註冊重新開機。

6.  主要和次要安裝程式會呼叫 [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) 函式來關閉重新開機管理員會話。

下列程式碼片段顯示啟動和使用重新開機管理員會話的主要安裝程式範例。 此範例需要 Windows 7 或 Windows Server 2008 R2。 在 Windows Vista 或 Windows Server 2008 上，計算機應用程式會關閉，但不會重新開機。 此範例顯示主要安裝程式如何使用重新開機管理員來關閉和重新開機進程。 此範例假設計算機已在執行，然後再啟動重新開機管理員會話。


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the  
    // Text-Encoded session key,defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of calc files to be registered.
    DWORD dwFiles           = 2;   

    //
    // NOTE:We register two calc executable files. 
    // The second one is for the redirection of 32 bit calc on 
    // 64 bit machines. Even if you are using a 32 bit machine,  
    // you don't need to comment out the second line. 
    //
    LPCWSTR rgsFiles[]      = 
     {L"C:\\Windows\\System32\\calc.exe",
      L"C:\\Windows\\SysWow64\\calc.exe"};

    UINT nRetry             = 0; 
    UINT nAffectedApps      = 0;
    UINT nProcInfoNeeded    = 0;
    RM_REBOOT_REASON dwRebootReasons    = RmRebootReasonNone;
    RM_PROCESS_INFO *rgAffectedApps     = NULL;
    
    //
    // Start a Restart Manager Session
    //
    dwErrCode = RmStartSession(&dwSessionHandle, 0, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: we only register two calc executable files 
    // in this sample. You can register files, processes 
    // (in the form of process ID), and services (in the   
    // form of service short names) with Restart Manager.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,       // Files
                                    0,  
                                    NULL,           // Processes
                                    0, 
                                    NULL);          // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Obtain the list of affected applications/services.
    //
    // NOTE: Restart Manager returns the results into the  
    // buffer allocated by the caller. The first call to 
    // RmGetList() will return the size of the buffer  
    // (i.e. nProcInfoNeeded) the caller needs to allocate. 
    // The caller then needs to allocate the buffer  
    // (i.e. rgAffectedApps) and make another RmGetList() 
    // call to ask Restart Manager to write the results 
    // into the buffer. However, since Restart Manager 
    // refreshes the list every time RmGetList()is called, 
    // it is possible that the size returned by the first 
    // RmGetList()call is not sufficient to hold the results  
    // discovered by the second RmGetList() call. Therefore, 
    // it is recommended that the caller follows the 
    // following practice to handle this race condition:
    //   
    //    Use a loop to call RmGetList() in case the buffer 
    //    allocated according to the size returned in previous 
    //    call is not enough.      
    // 
    // In this example, we use a do-while loop trying to make 
    // 3 RmGetList() calls (including the first attempt to get 
    // buffer size) and if we still cannot succeed, we give up. 
    //
    do
    {
        dwErrCode = RmGetList(dwSessionHandle,
                              &nProcInfoNeeded,
                              &nAffectedApps, 
                              rgAffectedApps, 
                              (LPDWORD) &dwRebootReasons);
        if (ERROR_SUCCESS == dwErrCode)
        {
            //
            // RmGetList() succeeded
            //
            break;
        }

        if (ERROR_MORE_DATA != dwErrCode)
        {
            //
            // RmGetList() failed, with errors 
            // other than ERROR_MORE_DATA
            //
            goto RM_CLEANUP;
        }

        //
        // RmGetList() is asking for more data
        //
        nAffectedApps = nProcInfoNeeded;
        
        if (NULL != rgAffectedApps)
        {
            delete []rgAffectedApps;
            rgAffectedApps = NULL;
        }

        rgAffectedApps = new RM_PROCESS_INFO[nAffectedApps];
    } while ((ERROR_MORE_DATA == dwErrCode) && (nRetry ++ < 3));

    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    if (RmRebootReasonNone != dwRebootReasons)
    {
        //
        // Restart Manager cannot mitigate a reboot. 
        // We goes to the clean up. The caller may want   
        // to add additional code to handle this scenario.
        //
        goto RM_CLEANUP;
    }
    
    //
    // Now rgAffectedApps contains the affected applications 
    // and services. The number of applications and services
    // returned is nAffectedApps. The result of RmGetList can 
    // be interpreted by the user to determine subsequent  
    // action (e.g. ask user's permission to shutdown).
    //
    // CALLER CODE GOES HERE...
     
    //
    // Shut down all running instances of affected 
    // applications and services.
    //
    dwErrCode = RmShutdown(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // An installer can now replace or update
    // the calc executable file.
    //
    // CALLER CODE GOES HERE...


    //
    // Restart applications and services, after the 
    // files have been replaced or updated.
    //
    dwErrCode = RmRestart(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:
    
    if (NULL != rgAffectedApps)
    {
        delete [] rgAffectedApps;
        rgAffectedApps = NULL;
    }

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // Clean up the Restart Manager session.
        //
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}
```



下列程式碼片段顯示將次要安裝程式加入現有重新開機管理員會話的範例。 此範例需要 Windows Vista 或 Windows Server 2008。 次要安裝程式會從主要安裝程式取得工作階段金鑰，並使用此金鑰來加入會話。


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the 
    // Text-Encoded session key, defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of files to be registered.
    DWORD dwFiles           = 1;   
    //
    // We register oleaut32.dll with Restart Manager.
    //
    LPCWSTR rgsFiles[]      = 
        {L"C:\\Windows\\System32\\oleaut32.dll"};

    //    
    // Secondary installer needs to obtain the session key from  
    // the primary installer and uses it to join the session.
    //
    // CALLER CODE GOES HERE ...
    //

    // We assume the session key obtained is stored in sessKey
    dwErrCode = RmJoinSession(&dwSessionHandle, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: In Vista, the subordinate is only allowed to 
    // register resources and cannot perform any other 
    // getlist, shutdown, restart or filter operations.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,     // Files
                                    0,  
                                    NULL,         // Processes
                                    0, 
                                    NULL);        // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // The subordinate leaves the conductor's session 
        // by calling RmEndSession(). The session itself 
        // won't be destroyed until the primary installer 
        // calls RmEndSession()
        //          
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}

```



 

 




