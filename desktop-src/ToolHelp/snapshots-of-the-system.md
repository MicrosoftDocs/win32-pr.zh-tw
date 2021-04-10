---
title: 系統的快照集
description: 快照集是工具說明功能的核心。 快照集是一或多個位於系統記憶體進程、執行緒、模組和堆積中的下列一或多個清單之目前狀態的唯讀複本。
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842484"
---
# <a name="snapshots-of-the-system"></a><span data-ttu-id="27b73-104">系統的快照集</span><span class="sxs-lookup"><span data-stu-id="27b73-104">Snapshots of the System</span></span>

<span data-ttu-id="27b73-105">快照集是工具說明功能的核心。</span><span class="sxs-lookup"><span data-stu-id="27b73-105">Snapshots are at the core of the tool help functions.</span></span> <span data-ttu-id="27b73-106">快照集是一或多個位於系統記憶體：進程、執行緒、模組和堆積之下列清單的目前狀態的唯讀複本。</span><span class="sxs-lookup"><span data-stu-id="27b73-106">A snapshot is a read-only copy of the current state of one or more of the following lists that reside in system memory: processes, threads, modules, and heaps.</span></span>

<span data-ttu-id="27b73-107">使用工具說明函式的進程會從快照集（而不是直接從作業系統）存取這些清單。</span><span class="sxs-lookup"><span data-stu-id="27b73-107">Processes that use tool help functions access these lists from snapshots instead of directly from the operating system.</span></span> <span data-ttu-id="27b73-108">當處理常式啟動和結束時，系統記憶體中的清單會變更、建立和終結執行緒、從系統記憶體載入和卸載可執行模組，以及建立和終結堆積。</span><span class="sxs-lookup"><span data-stu-id="27b73-108">The lists in system memory change when processes are started and ended, threads are created and destroyed, executable modules are loaded and unloaded from system memory, and heaps are created and destroyed.</span></span> <span data-ttu-id="27b73-109">從快照集使用資訊可防止不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="27b73-109">The use of information from a snapshot prevents inconsistencies.</span></span> <span data-ttu-id="27b73-110">否則，對清單所做的變更可能會導致執行緒不正確地進行清單或造成 (GP 錯誤) 的存取違規。</span><span class="sxs-lookup"><span data-stu-id="27b73-110">Otherwise, changes to a list could possibly cause a thread to incorrectly traverse the list or cause an access violation (a GP fault).</span></span> <span data-ttu-id="27b73-111">例如，如果應用程式在建立或終止其他執行緒時，會線上程清單中進行，則應用程式用來跨越執行緒清單的資訊可能會變成過時，而且可能會導致應用程式發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="27b73-111">For example, if an application traverses the thread list while other threads are created or terminated, information that the application is using to traverse the thread list might become outdated and could cause an error for the application traversing the list.</span></span>

<span data-ttu-id="27b73-112">若要取得系統記憶體的快照，請使用 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) 函數。</span><span class="sxs-lookup"><span data-stu-id="27b73-112">To take a snapshot of the system memory, use the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function.</span></span> <span data-ttu-id="27b73-113">您可以在呼叫此函式時指定下列一或多個值，以控制快照集的內容：</span><span class="sxs-lookup"><span data-stu-id="27b73-113">You can control the content of a snapshot by specifying one or more of the following values when calling this function:</span></span>

-   <span data-ttu-id="27b73-114">**TH32CS \_ SNAPHEAPLIST**</span><span class="sxs-lookup"><span data-stu-id="27b73-114">**TH32CS\_SNAPHEAPLIST**</span></span>
-   <span data-ttu-id="27b73-115">**TH32CS \_ SNAPMODULE**</span><span class="sxs-lookup"><span data-stu-id="27b73-115">**TH32CS\_SNAPMODULE**</span></span>
-   <span data-ttu-id="27b73-116">**TH32CS \_ SNAPPROCESS**</span><span class="sxs-lookup"><span data-stu-id="27b73-116">**TH32CS\_SNAPPROCESS**</span></span>
-   <span data-ttu-id="27b73-117">**TH32CS \_ SNAPTHREAD**</span><span class="sxs-lookup"><span data-stu-id="27b73-117">**TH32CS\_SNAPTHREAD**</span></span>

<span data-ttu-id="27b73-118">**TH32CS \_ SNAPHEAPLIST** 和 **TH32CS \_ SNAPMODULE** 值是進程特定的。</span><span class="sxs-lookup"><span data-stu-id="27b73-118">The **TH32CS\_SNAPHEAPLIST** and **TH32CS\_SNAPMODULE** values are process specific.</span></span> <span data-ttu-id="27b73-119">當指定這些值時，快照集會包含指定進程的堆積和模組清單。</span><span class="sxs-lookup"><span data-stu-id="27b73-119">When these values are specified, the heap and module lists of the specified process are included in the snapshot.</span></span> <span data-ttu-id="27b73-120">如果您指定零做為處理常式識別碼，則會使用目前的進程。</span><span class="sxs-lookup"><span data-stu-id="27b73-120">If you specify zero as the process identifier, the current process is used.</span></span> <span data-ttu-id="27b73-121">即使將進程識別碼傳遞給 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)， **TH32CS \_ SNAPTHREAD** 值一律會建立全系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="27b73-121">The **TH32CS\_SNAPTHREAD** value always creates a system-wide snapshot even if a process identifier is passed to [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).</span></span>

<span data-ttu-id="27b73-122">若要列舉所有進程的堆積或模組狀態，請指定 **TH32CS \_ SNAPALL** 值和目前進程的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="27b73-122">To enumerate the heap or module state for all processes, specify the **TH32CS\_SNAPALL** value and the process identifier of the current process.</span></span> <span data-ttu-id="27b73-123">然後，針對快照中的每個額外進程，再次呼叫 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) ，指定其處理序識別碼和 **TH32CS \_ SNAPHEAPLIST** 或 **TH32CS \_ SNAPMODULE** 值。</span><span class="sxs-lookup"><span data-stu-id="27b73-123">Then, for each additional process in the snapshot, call [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) again, specifying its process identifier and the **TH32CS\_SNAPHEAPLIST** or **TH32CS\_SNAPMODULE** value.</span></span>

<span data-ttu-id="27b73-124">您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)的擴充錯誤狀態碼。</span><span class="sxs-lookup"><span data-stu-id="27b73-124">You can retrieve an extended error status code for [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="27b73-125">當您的進程使用快照集完成時，請使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式將它終結。</span><span class="sxs-lookup"><span data-stu-id="27b73-125">When your process finishes using a snapshot, destroy it using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="27b73-126">如果您沒有終結快照集，進程將會流失記憶體，直到它結束為止，此時系統會回收記憶體。</span><span class="sxs-lookup"><span data-stu-id="27b73-126">If you do not destroy a snapshot, the process will leak memory until the it exits, at which time the system reclaims the memory.</span></span>

> [!Note]  
> <span data-ttu-id="27b73-127">快照集控制碼的運作方式就像是檔案控制代碼，並且受限於可使用它之進程和執行緒的相同規則。</span><span class="sxs-lookup"><span data-stu-id="27b73-127">The snapshot handle acts like a file handle and is subject to the same rules regarding the processes and threads in which it can be used.</span></span> <span data-ttu-id="27b73-128">若要指定控制碼是可繼承的，請使用 **TH32CS \_ INHERIT** 值來建立快照集。</span><span class="sxs-lookup"><span data-stu-id="27b73-128">To specify that the handle is inheritable, create the snapshot using the **TH32CS\_INHERIT** value.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="27b73-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="27b73-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b73-130">拍攝快照集和觀看進程</span><span class="sxs-lookup"><span data-stu-id="27b73-130">Taking a Snapshot and Viewing Processes</span></span>](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 