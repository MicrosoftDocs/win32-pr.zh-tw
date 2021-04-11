---
description: 此範例說明如何使用 GetProcessHeaps 函式來抓取預設進程堆積的控制碼，以及目前進程使用中的任何私用堆積。
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: 取得進程堆積
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caffc8dcc69b02ab671b379dbb5e133e65f8d448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944164"
---
# <a name="getting-process-heaps"></a><span data-ttu-id="6ce08-103">取得進程堆積</span><span class="sxs-lookup"><span data-stu-id="6ce08-103">Getting Process Heaps</span></span>

<span data-ttu-id="6ce08-104">此範例說明如何使用 [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) 函式來抓取預設進程堆積的控制碼，以及目前進程使用中的任何私用堆積。</span><span class="sxs-lookup"><span data-stu-id="6ce08-104">This example illustrates the use of the [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) function to retrieve handles to the default process heap and any private heaps that are active for the current process.</span></span>

<span data-ttu-id="6ce08-105">此範例會呼叫 [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) 兩次，先計算所需的緩衝區大小，然後再重新取得緩衝區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ce08-105">The example calls [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) twice, first to calculate the size of the buffer needed and again to retrieve handles into the buffer.</span></span> <span data-ttu-id="6ce08-106">緩衝區是使用 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)所傳回的控制碼，從預設進程堆積進行配置。</span><span class="sxs-lookup"><span data-stu-id="6ce08-106">The buffer is allocated from the default process heap, using the handle returned by [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap).</span></span> <span data-ttu-id="6ce08-107">此範例會將每個堆積的起始位址列印到主控台。</span><span class="sxs-lookup"><span data-stu-id="6ce08-107">The example prints the starting address of each heap to the console.</span></span> <span data-ttu-id="6ce08-108">然後，它會使用 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) 函式來釋放為緩衝區配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6ce08-108">It then uses the [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) function to free memory allocated for the buffer.</span></span>

<span data-ttu-id="6ce08-109">進程中的堆積數目可能會不同。</span><span class="sxs-lookup"><span data-stu-id="6ce08-109">The number of heaps in a process may vary.</span></span> <span data-ttu-id="6ce08-110">進程一律至少有一個堆積（預設進程堆積），而且可能會有一個或多個由應用程式建立的私用堆積，或是載入至進程位址空間的 Dll。</span><span class="sxs-lookup"><span data-stu-id="6ce08-110">A process always has at least one heap—the default process heap—and it may have one or more private heaps created by the application or by DLLs that are loaded into the address space of the process.</span></span>

<span data-ttu-id="6ce08-111">請注意，應用程式應該只對其預設進程堆積或應用程式所建立的私用堆積呼叫堆積函數;呼叫另一個元件所擁有之私用堆積上的堆積函式可能會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="6ce08-111">Note that an application should call heap functions only on its default process heap or on private heaps that the application has created; calling heap functions on a private heap owned by another component may cause undefined behavior.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



