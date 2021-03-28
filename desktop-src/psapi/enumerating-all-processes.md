---
title: 列舉所有進程
description: 下列範例程式碼使用 EnumProcesses 函式來列舉系統中目前的進程。
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64e127014910974b881a7ae21e807be9ac19452
ms.sourcegitcommit: d581811a577e00821667dad731710909979dc72d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2021
ms.locfileid: "104514272"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="26e4b-103">列舉所有進程</span><span class="sxs-lookup"><span data-stu-id="26e4b-103">Enumerating All Processes</span></span>

<span data-ttu-id="26e4b-104">下列範例程式碼會使用 [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) 函式來取得系統中每個處理常式物件的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="26e4b-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="26e4b-105">接著會呼叫[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules)來取得每個處理常式名稱，並加以列印。</span><span class="sxs-lookup"><span data-stu-id="26e4b-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="26e4b-106">若為64位程式，請使用 [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) 函數。</span><span class="sxs-lookup"><span data-stu-id="26e4b-106">For 64 bit proceses, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="26e4b-107">Main 函式會使用 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) 函數取得處理常式清單。</span><span class="sxs-lookup"><span data-stu-id="26e4b-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="26e4b-108">Main 會針對每個進程呼叫 **PrintProcessNameAndID** 函式，並將處理序識別碼傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="26e4b-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="26e4b-109">接著， **PrintProcessNameAndID** 會呼叫 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)函式，以取得處理控制碼。</span><span class="sxs-lookup"><span data-stu-id="26e4b-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="26e4b-110">如果 **OpenProcess** 失敗，輸出會將進程名稱顯示為 <unknown> 。</span><span class="sxs-lookup"><span data-stu-id="26e4b-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="26e4b-111">例如，閒置和 CSRSS 程式的 **OpenProcess** 會失敗，因為其存取限制會防止使用者層級的程式碼開啟這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="26e4b-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="26e4b-112">接下來， **PrintProcessNameAndID** 會呼叫 [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) 函數來取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="26e4b-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="26e4b-113">最後， **PrintProcessNameAndID** 會呼叫 [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) 函式以取得可執行檔的名稱，並顯示名稱和處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="26e4b-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
