---
title: 註冊應用程式重新開機
description: 若要註冊要重新開機的應用程式，請呼叫 RegisterApplicationRestart 函數。
ms.assetid: 4dfbced7-77db-4042-823f-b4b81b2b27a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717f8984f26570284a70b40eef70a9d6f753d66a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186085"
---
# <a name="registering-for-application-restart"></a><span data-ttu-id="87a15-103">註冊應用程式重新開機</span><span class="sxs-lookup"><span data-stu-id="87a15-103">Registering for Application Restart</span></span>

<span data-ttu-id="87a15-104">若要註冊要重新開機的應用程式，請呼叫 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函數。</span><span class="sxs-lookup"><span data-stu-id="87a15-104">To register your application to be restarted, call the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="87a15-105">如果您的應用程式在沒有回應或遇到未處理的例外狀況之前，已執行至少60秒，則[Windows 錯誤報告 (WER) ](/windows/desktop/wer/windows-error-reporting)會重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="87a15-105">[Windows Error Reporting (WER)](/windows/desktop/wer/windows-error-reporting) will restart your application if it has been running for at least 60 seconds before becoming unresponsive or encountering an unhandled exception.</span></span>

<span data-ttu-id="87a15-106">您也應該考慮 [註冊](registering-for-application-recovery.md)復原，如此可讓您儲存在 WER 重新開機應用程式時，可能會有説明的資料和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="87a15-106">You should consider also [registering for recovery](registering-for-application-recovery.md), which lets you save data and state information that may be helpful when WER restarts your application.</span></span> <span data-ttu-id="87a15-107">如果您也註冊進行復原，則在復原程式完成之後，WER 將會重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="87a15-107">WER will restart the application after the recovery process completes, if you also register for recovery.</span></span>

<span data-ttu-id="87a15-108">復原程式完成之後，WER 會終止應用程式，然後重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="87a15-108">After the recovery process completes, WER terminates the application and then restarts it.</span></span> <span data-ttu-id="87a15-109">若為主控台應用程式，應用程式會在應用程式結束時關閉的另一個主控台視窗中啟動。</span><span class="sxs-lookup"><span data-stu-id="87a15-109">For console applications, the application is started in a separate console window that closes when the application exits.</span></span>

<span data-ttu-id="87a15-110">**請注意應用程式安裝程式的作者：** 註冊應用程式重新開機也會導致 Windows 在電腦重新開機後，在電腦因軟體更新而重新開機的情況下自動重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="87a15-110">**Note for application installer authors:** Registering for application restart will also cause Windows to automatically restart the application after the computer is restarted in cases where the computer is restarted due to a software update.</span></span> <span data-ttu-id="87a15-111">若要這樣做，應用程式的安裝程式必須使用 EWX [](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) \_ RESTARTAPPS 旗標集或 [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna)函式（已設定 SHUTDOWN RESTARTAPPS 旗標）來呼叫 ExitWindowsEx 函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="87a15-111">For this to work, the installer of the application must call the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function with the EWX\_RESTARTAPPS flag set or the [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) function with the SHUTDOWN\_RESTARTAPPS flag set.</span></span>

<span data-ttu-id="87a15-112">下列範例示範如何註冊，讓 WER 重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="87a15-112">The following example shows how to register to have WER restart your application.</span></span> <span data-ttu-id="87a15-113">在註冊應用程式重新開機之後，此範例會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="87a15-113">The example causes an access violation after registering for application restart.</span></span> <span data-ttu-id="87a15-114">Windows 錯誤報告會挑選存取違規，並示範錯誤報表使用者體驗，包括應用程式重新開機。</span><span class="sxs-lookup"><span data-stu-id="87a15-114">The access violation will be picked up by Windows Error Reporting and will demonstrate the error reporting user experience, including application restart.</span></span> <span data-ttu-id="87a15-115">它應該從沒有命令列引數的主控台視窗中執行。</span><span class="sxs-lookup"><span data-stu-id="87a15-115">It should be run from a console window with no command line arguments.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#define RESTART_SWITCH L"/restart"

void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId); 
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId); 
BOOL WINAPI CtrlHandler(DWORD dwControlType);
DWORD WINAPI Recover(PVOID pContext);

// A simple example to show how to use application recovery. For simplicity,
// the state information (record ID) is passed as part of the command line. 
void wmain(int argc, wchar_t* argv[])
{
    HRESULT hr = S_OK;
    DWORD dwRecordId = 0;
    BOOL fIsRestart = FALSE;

    GetRestartInfo(argc, argv, &fIsRestart, &dwRecordId);

    if (FAILED(hr = InitApplication(fIsRestart, &dwRecordId)))
    {
        wprintf(L"Failed to initialize the application.\n");
        goto cleanup;
    }

    // Do work. If you have a lot of state information, you should
    // periodically persist the state information to save time
    // in the recovery process.

    // The application must exist for at least 60 seconds for the
    // application to be restarted. Use Sleep() to mimic 60 seconds
    // worth of work.
    wprintf(L"Sleeping...\n");
    Sleep(62 * 1000);

    // Set the record ID to verify restart value.
    dwRecordId = 10;

    // Generate an access violation to force a restart. If we've already
    // restarted just exit because the example already demonstrated
    // the restart feature.
    if (FALSE == fIsRestart)
    {
        wprintf(L"Causing access violation...\n");
        int* p = NULL;
        *p = 5;
    }

cleanup:

    wprintf(L"Exiting...\n");
}


// Get the restart info from the command line. The command line is 
// of the form, /restart -r <RecordId>. The application 
// is being restarted if the first argument is /restart.
void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId) 
{
    if (argc > 1)
    {
        if (!wcsncmp(RESTART_SWITCH, argv[1], sizeof(RESTART_SWITCH)))
        {
            *pfIsRestart = TRUE;
            *pdwRecordId = _wtoi(argv[3]);
        }
    }

}

// Initialize the application. If this is a restart, use the state 
// information to reset the state of the application. This example 
// does not fail the initialization process if the process of 
// registering for application recovery and restart failed.
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId)
{
    DWORD status = ERROR_SUCCESS;  // Set only if the initializing the application fails,
    HRESULT hr = S_OK;             // not if registering for recovery and restart fails.
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering InitApplication...\n");

    if (fIsRestart)
    {
        // TODO: Use the record ID to initialize the application.
        wprintf(L"Restart record ID is %lu\n", *pdwRecordId);
    }
    else
    {
        // This is not a restart, so initialize the application accordingly.
    }

    // Register for restart. The command line is updated in the recovery callback.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", *pdwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
        goto cleanup;
    }

    // Register the callback that handles the control event notifications.
    // Used for recovery when an installer is updating a component of the
    // application.
    if (!SetConsoleCtrlHandler(CtrlHandler, TRUE))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"SetConsoleCtrlHandler failed.\n");
        goto cleanup;
    }

    // Register the callback that handles recovery when the application
    // encounters an unhandled exception or becomes unresponsive.
    hr = RegisterApplicationRecoveryCallback(Recover, pdwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
    if (FAILED(hr))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"RegisterApplicationRecoveryCallback failed with ox%x.\n", hr);
        goto cleanup;
    }

cleanup:

    return hr;
}


// Implement the callback for handling control character events.
// You'd implement this callback if an installer could update a
// component of your application. The system sends a CTRL_C_EVENT
// notification when an installer needs to shutdown your application
// or restart the computer in order to complete the installation.
// You can use the CTRL_C_EVENT to save final state information or
// data before exiting.
BOOL WINAPI CtrlHandler(DWORD dwControlType)
{
    wprintf(L"Entering CtrlHandler...\n");

    switch (dwControlType)
    {
        case CTRL_C_EVENT:
            wprintf(L"Handling CTRL_C_EVENT\n");
            return FALSE;

        // Other cases go here.

        default: 
            wprintf(L"Other, %ul\n", dwControlType);
            return FALSE;
    }
}


// Implement the recovery callback. This callback lets the application
// save state information or data in the event that the application
// encounters an unhandled exception or becomes unresponsive.
DWORD WINAPI Recover(PVOID pContext)
{
    HRESULT hr = S_OK;
    BOOL bCanceled = FALSE;
    DWORD dwRecordId = *(DWORD*)pContext;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering Recover callback...\n");

    // Do recovery work. 

    // Update the restart command line.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", dwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
    }

    // You must call the ApplicationRecoveryInProgress function within
    // the specified ping interval or the recovery callback exits.
    // Typically, you would do a block of work, call the function, and repeat.
    hr = ApplicationRecoveryInProgress(&bCanceled);
    if (bCanceled)  
    {
        wprintf(L"Recovery was canceled by the user.\n");
        goto cleanup;
    }

    // Do more recovery work. 
    
    // You could also call the RegisterApplicationRestart function to
    // update the command line used for the restart.

cleanup:

    // Save the state file.

    wprintf(L"Leaving Recover callback...\n");
    ApplicationRecoveryFinished((bCanceled) ? FALSE: TRUE);

    return 0;
}
```



 

 