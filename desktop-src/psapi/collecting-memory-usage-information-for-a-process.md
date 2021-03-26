---
title: 收集處理常式的記憶體使用量資訊
description: 若要判斷應用程式的效率，您可能會想要檢查其記憶體使用量。 下列範例程式碼會使用 GetProcessMemoryInfo 函數來取得進程記憶體使用量的相關資訊。
ms.assetid: 23641bf8-3653-4cb9-8008-cd99137ca268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead17b8308424be8b959c4043eec606b18292708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375664"
---
# <a name="collecting-memory-usage-information-for-a-process"></a><span data-ttu-id="a8a01-104">收集處理常式的記憶體使用量資訊</span><span class="sxs-lookup"><span data-stu-id="a8a01-104">Collecting Memory Usage Information For a Process</span></span>

<span data-ttu-id="a8a01-105">若要判斷應用程式的效率，您可能會想要檢查其記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="a8a01-105">To determine the efficiency of your application, you may want to examine its memory usage.</span></span> <span data-ttu-id="a8a01-106">下列範例程式碼會使用 [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) 函數來取得進程記憶體使用量的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a8a01-106">The following sample code uses the [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function to obtain information about the memory usage of a process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintMemoryInfo( DWORD processID )
{
    HANDLE hProcess;
    PROCESS_MEMORY_COUNTERS pmc;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Print information about the memory usage of the process.

    hProcess = OpenProcess(  PROCESS_QUERY_INFORMATION |
                                    PROCESS_VM_READ,
                                    FALSE, processID );
    if (NULL == hProcess)
        return;

    if ( GetProcessMemoryInfo( hProcess, &pmc, sizeof(pmc)) )
    {
        printf( "\tPageFaultCount: 0x%08X\n", pmc.PageFaultCount );
        printf( "\tPeakWorkingSetSize: 0x%08X\n", 
                  pmc.PeakWorkingSetSize );
        printf( "\tWorkingSetSize: 0x%08X\n", pmc.WorkingSetSize );
        printf( "\tQuotaPeakPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakPagedPoolUsage );
        printf( "\tQuotaPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPagedPoolUsage );
        printf( "\tQuotaPeakNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakNonPagedPoolUsage );
        printf( "\tQuotaNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaNonPagedPoolUsage );
        printf( "\tPagefileUsage: 0x%08X\n", pmc.PagefileUsage ); 
        printf( "\tPeakPagefileUsage: 0x%08X\n", 
                  pmc.PeakPagefileUsage );
    }

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

    // Print the memory usage for each process

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintMemoryInfo( aProcesses[i] );
    }

    return 0;
}
```



<span data-ttu-id="a8a01-107">Main 函式會使用 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) 函數取得處理常式清單。</span><span class="sxs-lookup"><span data-stu-id="a8a01-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="a8a01-108">Main 會針對每個進程呼叫 PrintMemoryInfo 函式，並傳遞處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8a01-108">For each process, main calls the PrintMemoryInfo function, passing the process identifier.</span></span> <span data-ttu-id="a8a01-109">接著，PrintMemoryInfo 會呼叫 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) 函式，以取得處理控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8a01-109">PrintMemoryInfo in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="a8a01-110">如果 **OpenProcess** 失敗，輸出只會顯示處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8a01-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="a8a01-111">例如，閒置和 CSRSS 程式的 **OpenProcess** 會失敗，因為其存取限制會防止使用者層級的程式碼開啟這些處理常式。</span><span class="sxs-lookup"><span data-stu-id="a8a01-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="a8a01-112">最後，PrintMemoryInfo 會呼叫 [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) 函數來取得記憶體使用量資訊。</span><span class="sxs-lookup"><span data-stu-id="a8a01-112">Finally, PrintMemoryInfo calls the [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function to obtain the memory usage information.</span></span>

 

 