---
description: 有兩種方式可執行多工處理：作為多個執行緒或多個進程的單一進程，每個進程都有一個或多個執行緒。
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: 使用多工的時機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980319"
---
# <a name="when-to-use-multitasking"></a><span data-ttu-id="a87e0-103">使用多工的時機</span><span class="sxs-lookup"><span data-stu-id="a87e0-103">When to Use Multitasking</span></span>

<span data-ttu-id="a87e0-104">有兩種方式可執行多工處理：作為多個執行緒或多個進程的單一進程，每個進程都有一個或多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="a87e0-104">There are two ways to implement multitasking: as a single process with multiple threads or as multiple processes, each with one or more threads.</span></span> <span data-ttu-id="a87e0-105">應用程式可以將需要私人位址空間和私用資源的每個執行緒放入自己的進程，以保護它免于其他進程執行緒的活動。</span><span class="sxs-lookup"><span data-stu-id="a87e0-105">An application can put each thread that requires a private address space and private resources into its own process, to protect it from the activities of other process threads.</span></span>

<span data-ttu-id="a87e0-106">多執行緒進程可以使用執行緒管理互斥的工作，例如提供使用者介面和執行背景計算。</span><span class="sxs-lookup"><span data-stu-id="a87e0-106">A multithreaded process can manage mutually exclusive tasks with threads, such as providing a user interface and performing background calculations.</span></span> <span data-ttu-id="a87e0-107">建立多執行緒程式也是一種方便的方式，可讓您以同時執行數個類似或相同工作的程式為結構。</span><span class="sxs-lookup"><span data-stu-id="a87e0-107">Creating a multithreaded process can also be a convenient way to structure a program that performs several similar or identical tasks concurrently.</span></span> <span data-ttu-id="a87e0-108">例如，具名管道伺服器可以針對附加至管道的每個用戶端進程建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="a87e0-108">For example, a named pipe server can create a thread for each client process that attaches to the pipe.</span></span> <span data-ttu-id="a87e0-109">此執行緒會管理伺服器與用戶端之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="a87e0-109">This thread manages the communication between the server and the client.</span></span> <span data-ttu-id="a87e0-110">您的進程可能會使用多個執行緒來完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="a87e0-110">Your process could use multiple threads to accomplish the following tasks:</span></span>

-   <span data-ttu-id="a87e0-111">管理多個視窗的輸入。</span><span class="sxs-lookup"><span data-stu-id="a87e0-111">Manage input for multiple windows.</span></span>
-   <span data-ttu-id="a87e0-112">從數個通訊裝置管理輸入。</span><span class="sxs-lookup"><span data-stu-id="a87e0-112">Manage input from several communications devices.</span></span>
-   <span data-ttu-id="a87e0-113">區分不同優先順序的工作。</span><span class="sxs-lookup"><span data-stu-id="a87e0-113">Distinguish tasks of varying priority.</span></span> <span data-ttu-id="a87e0-114">例如，高優先順序執行緒會應付緊急工作，而低優先順序執行緒則執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="a87e0-114">For example, a high-priority thread manages time-critical tasks, and a low-priority thread performs other tasks.</span></span>
-   <span data-ttu-id="a87e0-115">讓使用者介面保持回應，同時又配置時間給背景工作。</span><span class="sxs-lookup"><span data-stu-id="a87e0-115">Allow the user interface to remain responsive, while allocating time to background tasks.</span></span>

<span data-ttu-id="a87e0-116">藉由建立單一、多執行緒進程，而不是建立多個進程，讓應用程式更有效率地執行多工處理，原因如下：</span><span class="sxs-lookup"><span data-stu-id="a87e0-116">It is typically more efficient for an application to implement multitasking by creating a single, multithreaded process, rather than creating multiple processes, for the following reasons:</span></span>

-   <span data-ttu-id="a87e0-117">系統可以更快速地對執行緒執行內容切換，而不是處理常式，因為進程的額外負荷比執行緒 (進程內容大於執行緒內容) 。</span><span class="sxs-lookup"><span data-stu-id="a87e0-117">The system can perform a context switch more quickly for threads than processes, because a process has more overhead than a thread does (the process context is larger than the thread context).</span></span>
-   <span data-ttu-id="a87e0-118">進程的所有線程都共用相同的位址空間，而且可以存取進程的全域變數，這可簡化執行緒之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="a87e0-118">All threads of a process share the same address space and can access the process's global variables, which can simplify communication between threads.</span></span>
-   <span data-ttu-id="a87e0-119">進程的所有線程都可以共用開啟的控制碼給資源，例如檔案和管道。</span><span class="sxs-lookup"><span data-stu-id="a87e0-119">All threads of a process can share open handles to resources, such as files and pipes.</span></span>

<span data-ttu-id="a87e0-120">您可以使用其他技巧來取代多執行緒。</span><span class="sxs-lookup"><span data-stu-id="a87e0-120">There are other techniques you can use in the place of multithreading.</span></span> <span data-ttu-id="a87e0-121">最重要的是：非同步輸入和輸出 (i/o) 、i/o 完成埠、非同步程序呼叫 (APC) ，以及等待多個事件的能力。</span><span class="sxs-lookup"><span data-stu-id="a87e0-121">The most significant of these are as follows: asynchronous input and output (I/O), I/O completion ports, asynchronous procedure calls (APC), and the ability to wait for multiple events.</span></span>

<span data-ttu-id="a87e0-122">單一線程可以起始多個耗時的 i/o 要求，這些要求可以使用非同步 i/o 並存執行。</span><span class="sxs-lookup"><span data-stu-id="a87e0-122">A single thread can initiate multiple time-consuming I/O requests that can run concurrently using asynchronous I/O.</span></span> <span data-ttu-id="a87e0-123">非同步 i/o 可以在檔案、管道和序列通訊裝置上執行。</span><span class="sxs-lookup"><span data-stu-id="a87e0-123">Asynchronous I/O can be performed on files, pipes, and serial communication devices.</span></span> <span data-ttu-id="a87e0-124">如需詳細資訊，請參閱 [同步處理和重迭的輸入和輸出](../sync/synchronization-and-overlapped-input-and-output.md)。</span><span class="sxs-lookup"><span data-stu-id="a87e0-124">For more information, see [Synchronization and Overlapped Input and Output](../sync/synchronization-and-overlapped-input-and-output.md).</span></span>

<span data-ttu-id="a87e0-125">單一線程可以封鎖其本身的執行，同時等候數個或所有的事件發生。</span><span class="sxs-lookup"><span data-stu-id="a87e0-125">A single thread can block its own execution while waiting for any one or all of several events to occur.</span></span> <span data-ttu-id="a87e0-126">這比使用多個執行緒，每個執行緒都在等候單一事件時更有效率，而且比使用單一執行緒來取用處理器時間更有效率，因為持續檢查事件是否發生。</span><span class="sxs-lookup"><span data-stu-id="a87e0-126">This is more efficient than using multiple threads, each waiting for a single event, and more efficient than using a single thread that consumes processor time by continually checking for events to occur.</span></span> <span data-ttu-id="a87e0-127">如需詳細資訊，請參閱 [Wait 函數](../sync/wait-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="a87e0-127">For more information, see [Wait Functions](../sync/wait-functions.md).</span></span>

 

 
