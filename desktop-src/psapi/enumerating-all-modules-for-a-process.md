---
title: 列舉進程的所有模組
description: 若要判斷哪些進程已載入特定 DLL，您必須列舉每個進程的模組。 下列範例程式碼使用 EnumProcessModules 函式來列舉系統中目前進程的模組。
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315154"
---
# <a name="enumerating-all-modules-for-a-process"></a><span data-ttu-id="28415-104">列舉進程的所有模組</span><span class="sxs-lookup"><span data-stu-id="28415-104">Enumerating All Modules For a Process</span></span>

<span data-ttu-id="28415-105">若要判斷哪些進程已載入特定 DLL，您必須列舉每個進程的模組。</span><span class="sxs-lookup"><span data-stu-id="28415-105">To determine which processes have loaded a particular DLL, you must enumerate the modules for each process.</span></span> <span data-ttu-id="28415-106">下列範例程式碼使用 [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) 函式來列舉系統中目前進程的模組。</span><span class="sxs-lookup"><span data-stu-id="28415-106">The following sample code uses the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to enumerate the modules of current processes in the system.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



<span data-ttu-id="28415-107">Main 函式會使用 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) 函數取得處理常式清單。</span><span class="sxs-lookup"><span data-stu-id="28415-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="28415-108">在每個進程中，main 函式會呼叫 PrintModules 函式，並將處理序識別碼傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="28415-108">For each process, the main function calls the PrintModules function, passing it the process identifier.</span></span> <span data-ttu-id="28415-109">接著，PrintModules 會呼叫 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) 函式，以取得處理控制碼。</span><span class="sxs-lookup"><span data-stu-id="28415-109">PrintModules in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="28415-110">如果 **OpenProcess** 失敗，輸出只會顯示處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="28415-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="28415-111">例如，閒置和 CSRSS 程式的 **OpenProcess** 會失敗，因為其存取限制會防止使用者層級的程式碼開啟這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="28415-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="28415-112">接下來，PrintModules 會呼叫 [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) 函式，以取得模組控制碼函數。</span><span class="sxs-lookup"><span data-stu-id="28415-112">Next, PrintModules calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles function.</span></span> <span data-ttu-id="28415-113">最後，PrintModules 會呼叫 [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) 函式，每個模組一次，以取得模組名稱。</span><span class="sxs-lookup"><span data-stu-id="28415-113">Finally, PrintModules calls the [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) function, once for each module, to obtain the module names.</span></span>

 

 