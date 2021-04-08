---
title: 堆積清單和堆積行走
description: 包含指定進程之堆積清單的快照集包含每個與指定進程相關聯之堆積的識別資訊，以及每個堆積的詳細資訊。
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5a9b8d30e2de1bf5ab37de03fdcb3fde663417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682525"
---
# <a name="heap-lists-and-heap-walking"></a><span data-ttu-id="a74bd-103">堆積清單和堆積行走</span><span class="sxs-lookup"><span data-stu-id="a74bd-103">Heap Lists and Heap Walking</span></span>

<span data-ttu-id="a74bd-104">包含指定進程之堆積清單的快照集包含每個與指定進程相關聯之堆積的識別資訊，以及每個堆積的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a74bd-104">A snapshot that includes the heap list for a specified process contains identification information for each heap associated with the specified process and detailed information about each heap.</span></span> <span data-ttu-id="a74bd-105">您可以使用 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) 函式，來抓取堆積清單的第一個堆積的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a74bd-105">You can retrieve an identifier for the first heap of the heap list by using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) function.</span></span> <span data-ttu-id="a74bd-106">在抓取清單中的第一個堆積之後，您可以使用 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) 函式，針對與進程相關聯的後續堆積來進行堆積清單。</span><span class="sxs-lookup"><span data-stu-id="a74bd-106">After retrieving the first heap in the list, you can traverse the heap list for subsequent heaps associated with the process by using the [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) function.</span></span> <span data-ttu-id="a74bd-107">**Heap32ListFirst** 和 **Heap32ListNext** 會以處理常式識別碼、堆積識別碼和描述堆積的旗標來填滿 [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) 結構。</span><span class="sxs-lookup"><span data-stu-id="a74bd-107">**Heap32ListFirst** and **Heap32ListNext** fill a [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) structure with the process identifier, the heap identifier, and flags describing the heap.</span></span>

<span data-ttu-id="a74bd-108">您可以使用 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 函數來取得堆積第一個區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a74bd-108">You can retrieve information about the first block of a heap by using the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) function.</span></span> <span data-ttu-id="a74bd-109">在抓取堆積的第一個區塊之後，您可以使用 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函數來取得相同堆積之後續區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a74bd-109">After retrieving the first block of a heap, you can retrieve information about subsequent blocks of the same heap by using the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function.</span></span> <span data-ttu-id="a74bd-110">**Heap32First** 和 **Heap32Next** 會在 [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) 結構中填入適當堆積區塊的資訊。</span><span class="sxs-lookup"><span data-stu-id="a74bd-110">**Heap32First** and **Heap32Next** fill a [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) structure with information for the appropriate block of a heap.</span></span>

<span data-ttu-id="a74bd-111">您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)、 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)、 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)的擴充錯誤狀態碼。</span><span class="sxs-lookup"><span data-stu-id="a74bd-111">You can retrieve an extended error status code for [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first), and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="a74bd-112">在 [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32)結構的 **th32HeapID** 成員中指定的堆積識別碼，只有工具說明函式的意義。</span><span class="sxs-lookup"><span data-stu-id="a74bd-112">The heap identifier, which is specified in the **th32HeapID** member of the [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) structure, has meaning only to the tool help functions.</span></span> <span data-ttu-id="a74bd-113">它不是控制碼，也不能供其他函式使用。</span><span class="sxs-lookup"><span data-stu-id="a74bd-113">It is not a handle, nor is it usable by other functions.</span></span>

 

 

 