---
description: 可提供警示 i/o 是應用程式執行緒只會在處於可提供警示狀態時處理非同步 i/o 要求的方法。
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: 可提供警示 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971686"
---
# <a name="alertable-io"></a><span data-ttu-id="7c251-103">可提供警示 i/o</span><span class="sxs-lookup"><span data-stu-id="7c251-103">Alertable I/O</span></span>

<span data-ttu-id="7c251-104">可提供警示 i/o 是應用程式執行緒只會在處於可提供警示狀態時處理非同步 i/o 要求的方法。</span><span class="sxs-lookup"><span data-stu-id="7c251-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="7c251-105">若要瞭解執行緒處於可提供警示狀態的時間，請考慮下列案例：</span><span class="sxs-lookup"><span data-stu-id="7c251-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="7c251-106">執行緒藉由呼叫 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和回呼函式的指標，初始化非同步讀取要求。</span><span class="sxs-lookup"><span data-stu-id="7c251-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="7c251-107">執行緒藉由呼叫 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 和回呼函式的指標，來起始非同步寫入要求。</span><span class="sxs-lookup"><span data-stu-id="7c251-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="7c251-108">執行緒呼叫的函式會從遠端資料庫伺服器提取一列資料。</span><span class="sxs-lookup"><span data-stu-id="7c251-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="7c251-109">在此案例中， [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 的呼叫最可能會在步驟3中的函式呼叫之前傳回。</span><span class="sxs-lookup"><span data-stu-id="7c251-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="7c251-110">當他們這麼做時，核心會線上程的非同步程序呼叫上放置回呼函數的指標， (APC) 佇列。</span><span class="sxs-lookup"><span data-stu-id="7c251-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="7c251-111">核心會維護此佇列，專門用來保存傳回的 i/o 要求資料，直到對應的執行緒可以處理它為止。</span><span class="sxs-lookup"><span data-stu-id="7c251-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="7c251-112">當資料列提取完成且執行緒從函式傳回時，其最高優先順序是藉由呼叫回呼函式來處理佇列上傳回的 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="7c251-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="7c251-113">若要這樣做，它必須進入可提供警示狀態。</span><span class="sxs-lookup"><span data-stu-id="7c251-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="7c251-114">執行緒只能藉由使用適當的旗標來呼叫下列其中一個函式來執行此動作：</span><span class="sxs-lookup"><span data-stu-id="7c251-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="7c251-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="7c251-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="7c251-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="7c251-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="7c251-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="7c251-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="7c251-118">**SignalObjectAndWait**</span><span class="sxs-lookup"><span data-stu-id="7c251-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="7c251-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="7c251-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="7c251-120">當執行緒進入可提供警示狀態時，會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="7c251-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="7c251-121">核心會檢查執行緒的 APC 佇列。</span><span class="sxs-lookup"><span data-stu-id="7c251-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="7c251-122">如果佇列包含回呼函式指標，則核心會移除佇列中的指標，並將它傳送到執行緒。</span><span class="sxs-lookup"><span data-stu-id="7c251-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="7c251-123">執行緒執行回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7c251-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="7c251-124">佇列中剩餘的每個指標都會重複步驟1和2。</span><span class="sxs-lookup"><span data-stu-id="7c251-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="7c251-125">當佇列是空的時，執行緒會從將它置於可提供警示狀態的函式中返回。</span><span class="sxs-lookup"><span data-stu-id="7c251-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="7c251-126">在此案例中，一旦執行緒進入可提供警示狀態，它就會呼叫傳送至 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)的回呼函式，然後從放入可提供警示狀態的函式返回。</span><span class="sxs-lookup"><span data-stu-id="7c251-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="7c251-127">如果執行緒在其 APC 佇列是空的情況下進入可提供警示狀態，則在發生下列其中一種情況時，核心會暫停執行緒的執行：</span><span class="sxs-lookup"><span data-stu-id="7c251-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="7c251-128">正在等待的核心物件會收到信號。</span><span class="sxs-lookup"><span data-stu-id="7c251-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="7c251-129">在 APC 佇列中放置回呼函式指標。</span><span class="sxs-lookup"><span data-stu-id="7c251-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="7c251-130">使用可提供警示 i/o 來處理非同步 i/o [**要求的執行緒**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ，會比在設定重迭結構中的事件旗標時更有效率，而且可提供警示 i/o 機制的複雜度會比要使用的 [i/o 完成埠](i-o-completion-ports.md) 低。</span><span class="sxs-lookup"><span data-stu-id="7c251-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="7c251-131">不過，可提供警示 i/o 只會將 i/o 要求的結果傳回給起始它的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7c251-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="7c251-132">I/o 完成埠沒有這項限制。</span><span class="sxs-lookup"><span data-stu-id="7c251-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c251-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c251-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c251-134">非同步程序呼叫</span><span class="sxs-lookup"><span data-stu-id="7c251-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
