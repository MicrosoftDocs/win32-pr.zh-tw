---
title: 遍歷堆積清單
description: 範例顯示如何取得目前進程的堆積清單。
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/30/2021
ms.locfileid: "106991070"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="db62b-103">遍歷堆積清單</span><span class="sxs-lookup"><span data-stu-id="db62b-103">Traversing the Heap List</span></span>

<span data-ttu-id="db62b-104">下列範例會取得目前進程的堆積清單。</span><span class="sxs-lookup"><span data-stu-id="db62b-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="db62b-105">它會使用 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) 函式來建立堆積的快照集，然後使用 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) 和 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) 函式逐步執行清單。</span><span class="sxs-lookup"><span data-stu-id="db62b-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="db62b-106">針對每個堆積，它會使用 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函數來引導堆積區塊。</span><span class="sxs-lookup"><span data-stu-id="db62b-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="db62b-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 效率不佳，尤其是針對大型堆積。</span><span class="sxs-lookup"><span data-stu-id="db62b-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="db62b-108">不過，它們很適合用來查詢其他進程，您通常必須將執行緒插入另一個進程來收集資訊， (這些 Api 為您) 。</span><span class="sxs-lookup"><span data-stu-id="db62b-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="db62b-109">請參閱第二個範例，以取得相等、更有效率的替代方案，其使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) ，而不是 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)。</span><span class="sxs-lookup"><span data-stu-id="db62b-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="db62b-110">請注意， [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 只能用於相同的進程。</span><span class="sxs-lookup"><span data-stu-id="db62b-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

<span data-ttu-id="db62b-111">下列程式碼片段會使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式來逐步解說進程堆積，並產生與前一個範例相同的輸出，但更有效率：</span><span class="sxs-lookup"><span data-stu-id="db62b-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="db62b-112">使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式進行堆積的方式大約是堆積大小的線性，而 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函式的堆積在堆積的大小大約是二到二。</span><span class="sxs-lookup"><span data-stu-id="db62b-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="db62b-113">即使是具有10000配置的適度堆積， [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 執行10000倍的速度比 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 快，同時提供更詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="db62b-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="db62b-114">隨著堆積大小的增加，效能的差異變得更顯著。</span><span class="sxs-lookup"><span data-stu-id="db62b-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="db62b-115">如需使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式來逐步堆積的詳細範例，請參閱 [列舉堆積](/windows/win32/memory/enumerating-a-heap)。</span><span class="sxs-lookup"><span data-stu-id="db62b-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
