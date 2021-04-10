---
description: CreateProcess 函式會建立新的進程，它會與建立的進程分開執行。 不過，為了簡單起見，關聯性稱為父子式關聯性。
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: 建立處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944226"
---
# <a name="creating-processes"></a><span data-ttu-id="6d512-104">建立處理常式</span><span class="sxs-lookup"><span data-stu-id="6d512-104">Creating Processes</span></span>

<span data-ttu-id="6d512-105">[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式會建立新的進程，它會與建立的進程分開執行。</span><span class="sxs-lookup"><span data-stu-id="6d512-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="6d512-106">不過，為了簡單起見，關聯性稱為父子式關聯性。</span><span class="sxs-lookup"><span data-stu-id="6d512-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="6d512-107">下列程式碼示範如何建立進程。</span><span class="sxs-lookup"><span data-stu-id="6d512-107">The following code demonstrates how to create a process.</span></span>


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



<span data-ttu-id="6d512-108">如果 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 成功，它會傳回 [**進程 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) 結構，其中包含新進程及其主要執行緒的控制碼和識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d512-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="6d512-109">系統會以完整存取權限建立執行緒和進程控制碼，不過如果您指定安全描述項，就可以限制存取。</span><span class="sxs-lookup"><span data-stu-id="6d512-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="6d512-110">當您不再需要這些控制碼時，請使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數來關閉它們。</span><span class="sxs-lookup"><span data-stu-id="6d512-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="6d512-111">您也可以使用 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) 函數建立進程。</span><span class="sxs-lookup"><span data-stu-id="6d512-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="6d512-112">這可讓您指定進程將在其中執行的使用者帳戶的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="6d512-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
