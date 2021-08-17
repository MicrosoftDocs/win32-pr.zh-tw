---
title: 遍歷堆積清單
description: 範例顯示如何取得目前進程的堆積清單。
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 868526c76ee85095f5b52cc9238e9e16015bfb3a81c9888da148f1d5ecc644aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419248"
---
# <a name="traversing-the-heap-list"></a>遍歷堆積清單

下列範例會取得目前進程的堆積清單。 它會使用 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) 函式來建立堆積的快照集，然後使用 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) 和 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) 函式逐步執行清單。 針對每個堆積，它會使用 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函數來引導堆積區塊。

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 效率不佳，尤其是針對大型堆積。 不過，它們很適合用來查詢其他進程，您通常必須將執行緒插入另一個進程來收集資訊， (這些 Api 為您) 。

請參閱第二個範例，以取得相等、更有效率的替代方案，其使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) ，而不是 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)。 請注意， [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 只能用於相同的進程。

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

下列程式碼片段會使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式來逐步解說進程堆積，並產生與前一個範例相同的輸出，但更有效率：

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

使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式進行堆積的方式大約是堆積大小的線性，而 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函式的堆積在堆積的大小大約是二到二。
即使是具有10000配置的適度堆積， [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 執行10000倍的速度比 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 快，同時提供更詳細的資訊。 隨著堆積大小的增加，效能的差異變得更顯著。

如需使用 [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) 函式來逐步堆積的詳細範例，請參閱 [列舉堆積](/windows/win32/memory/enumerating-a-heap)。
