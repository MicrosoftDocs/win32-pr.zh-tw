---
title: 轉散發設定的範例程式碼
description: 轉散發設定的範例程式碼
ms.assetid: 480f0da7-68c1-4144-a623-47578ae54acb
keywords:
- Windows媒體格式 SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows媒體格式 SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，範例程式碼
- 軟體轉散發，程式碼範例
- 轉散發，範例程式碼
- 轉散發，程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a845f6c4ec66f2858756071a3e0260cb812c665a2b5b4effa063369bc894abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586068"
---
# <a name="example-code-for-redistribution-setup"></a>轉散發設定的範例程式碼

當您在應用程式中包含轉散發套件時，當您在安裝程式常式中叫用轉散發套件時，可以使用/Q： A 旗標。 這會隱藏使用者介面 (UI) 。

下列範例程式碼可以在您的安裝程式常式中用來以無訊息模式執行轉散發套件，並在電腦必須重新開機時通知您的設定常式。


```C++
#include <windows.h>
#include <shlwapi.h>
#include <TCHAR.H>

// Link to shlwapi.lib.
#pragma comment(lib, "shlwapi")

#define MAX_TIMEOUT_MS 30 * 60 * 1000
#define TIME_INCREMENT 250

// Prototypes
BOOL InstallWMRedist( BOOL );
BOOL SystemNeedsReboot( void );

void main( void )
{
    InstallWMRedist( TRUE );

    printf("Setup is complete.\n");

    if( SystemNeedsReboot() )
    {
        // Write some code here to ensure that your application will 
        // restart the computer, delay dll registrations, and so on 
        // until after the restart, where possible. For example, 
        // set a global flag for use by the application.
        printf("A reboot IS required.");
    }
    else
    {
        printf("A reboot IS NOT required...");
    }
    
}

///////////////////////////////////////////////////////////////////////
// 
// InstallWMRedist
//
// fWaitForCompletion: If TRUE the function waits for completion.
//
///////////////////////////////////////////////////////////////////////
BOOL InstallWMRedist( BOOL fWaitForCompletion )
{
    STARTUPINFO StartUpInfo;
    PROCESS_INFORMATION ProcessInfo;

    StartUpInfo.cb = sizeof( StartUpInfo );
    StartUpInfo.lpReserved = NULL;
    StartUpInfo.dwFlags = 0;
    StartUpInfo.cbReserved2 = 0;
    StartUpInfo.lpReserved2 = NULL; 
    StartUpInfo.lpDesktop = NULL;
    StartUpInfo.lpTitle = NULL;
    StartUpInfo.dwX = 0;
    StartUpInfo.dwY = 0;
    StartUpInfo.dwXSize = 0;
    StartUpInfo.dwYSize = 0;
    StartUpInfo.dwXCountChars = 0;
    StartUpInfo.dwYCountChars = 0;
    StartUpInfo.dwFillAttribute = 0;
    StartUpInfo.dwFlags = 0;
    StartUpInfo.wShowWindow = 0;
    StartUpInfo.hStdInput = NULL;
    StartUpInfo.hStdOutput = NULL;
    StartUpInfo.hStdError = NULL;

    // Run the installer with the Quiet for All dialogs and Reboot:Never 
    // flags. The installation should be silent, and the setup routine  
    // will be notified about whether the computer must be restarted.

    if( !CreateProcess( _T("c:\\temp\\WMFDist.exe"), 
                        _T("c:\\temp\\WMFDist.exe /Q:A"), 
                        NULL, NULL, FALSE, 0, NULL, NULL, 
                        &StartUpInfo, &ProcessInfo ) )
    {
        DWORD myError = GetLastError();
        return( FALSE );
    }

    CloseHandle( ProcessInfo.hThread );

    if( fWaitForCompletion )
    {
        DWORD dwTimePassed = 0;
        while( TRUE )
        {
            if( WAIT_TIMEOUT != WaitForMultipleObjects( 1, 
                                       &ProcessInfo.hProcess, 
                                       FALSE, TIME_INCREMENT ) )
                break;

            if( dwTimePassed > MAX_TIMEOUT_MS )
            {
                TerminateProcess( ProcessInfo.hProcess, E_FAIL );
                break;
            }
            dwTimePassed += TIME_INCREMENT;
        }
    }
    CloseHandle( ProcessInfo.hProcess);

    return( TRUE );
}

///////////////////////////////////////////////////////////////////////
//
// Used to determine whether the system should be restarted.
//
///////////////////////////////////////////////////////////////////////
BOOL SystemNeedsReboot( void )
{
    BOOL fNeedExists = FALSE;
    OSVERSIONINFO osvi;

    osvi.dwOSVersionInfoSize = sizeof( OSVERSIONINFO );
    GetVersionEx( &osvi );

    if( VER_PLATFORM_WIN32_NT != osvi.dwPlatformId )
    {
        TCHAR szIniPath[MAX_PATH];

        GetWindowsDirectory(szIniPath, sizeof(szIniPath)/sizeof(TCHAR));

        // PathAppend automatically inserts a backslash if needed.
        PathAppend( szIniPath, _T("wininit.ini") );

        if( 0xFFFFFFFF != GetFileAttributes( szIniPath ) )
        {
            HANDLE hFile = INVALID_HANDLE_VALUE;

            hFile = CreateFile(
                szIniPath, 
                GENERIC_READ, 
                FILE_SHARE_READ | FILE_SHARE_WRITE, 
                NULL,
                OPEN_EXISTING,
                0, NULL
                );

            if (hFile != INVALID_HANDLE_VALUE)
            {
                DWORD cbFileSize = GetFileSize(hFile, NULL);

                if ((cbFileSize > 0) && (cbFileSize != INVALID_FILE_SIZE))
                {
                    fNeedExists = TRUE;
                }
                CloseHandle(hFile);
            }
        }
    }
    else
    {
        HKEY hKey = NULL;

        if( ERROR_SUCCESS == RegOpenKeyEx( HKEY_LOCAL_MACHINE, 
                _T("System\\CurrentControlSet\\Control\\Session Manager"), 
                 0, KEY_READ, &hKey ) )
        {
            if( ERROR_SUCCESS == RegQueryValueEx( hKey, 
                _T("PendingFileRenameOperations"), 
                 NULL, NULL, NULL, NULL))
            {
                fNeedExists = TRUE;
            }

            RegCloseKey( hKey );
        }
    }

    return( fNeedExists );
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**軟體轉散發**](software-redistribution.md)
</dt> </dl>

 

 




