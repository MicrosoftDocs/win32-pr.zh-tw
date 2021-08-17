---
description: CreateProcess 函式會建立新的進程，它會與建立的進程分開執行。 不過，為了簡單起見，關聯性稱為父子式關聯性。
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: 建立處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8e5e4340f5c956e964b74ab134a7618a4c4bf0fa44eee1989a0457741d7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143101"
---
# <a name="creating-processes"></a>建立處理常式

[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式會建立新的進程，它會與建立的進程分開執行。 不過，為了簡單起見，關聯性稱為父子式關聯性。

下列程式碼示範如何建立進程。


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



如果 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 成功，它會傳回 [**進程 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) 結構，其中包含新進程及其主要執行緒的控制碼和識別碼。 系統會以完整存取權限建立執行緒和進程控制碼，不過如果您指定安全描述項，就可以限制存取。 當您不再需要這些控制碼時，請使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數來關閉它們。

您也可以使用 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) 函數建立進程。 這可讓您指定進程將在其中執行的使用者帳戶的安全性內容。

 

 
