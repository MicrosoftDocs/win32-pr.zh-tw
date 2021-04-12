---
description: 每個進程都會提供執行程式所需的資源。
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: 關於處理序和執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650eab4421971bdc08e71c031aec433ed84471bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192765"
---
# <a name="about-processes-and-threads"></a><span data-ttu-id="9664f-103">關於處理序和執行緒</span><span class="sxs-lookup"><span data-stu-id="9664f-103">About Processes and Threads</span></span>

<span data-ttu-id="9664f-104">每個 *進程* 都會提供執行程式所需的資源。</span><span class="sxs-lookup"><span data-stu-id="9664f-104">Each *process* provides the resources needed to execute a program.</span></span> <span data-ttu-id="9664f-105">進程具有虛擬位址空間、可執行程式碼、對系統物件的開啟控制碼、安全性內容、唯一的處理序識別碼、環境變數、優先順序類別、最小和最大工作集大小，以及至少一個執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="9664f-105">A process has a virtual address space, executable code, open handles to system objects, a security context, a unique process identifier, environment variables, a priority class, minimum and maximum working set sizes, and at least one thread of execution.</span></span> <span data-ttu-id="9664f-106">每個進程都是使用單一執行緒啟動，通常稱為 *主要執行緒*，但可以從其任何執行緒建立額外的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9664f-106">Each process is started with a single thread, often called the *primary thread*, but can create additional threads from any of its threads.</span></span>

<span data-ttu-id="9664f-107">*執行緒* 是可排程執行之進程內的實體。</span><span class="sxs-lookup"><span data-stu-id="9664f-107">A *thread* is the entity within a process that can be scheduled for execution.</span></span> <span data-ttu-id="9664f-108">進程的所有線程都會共用其虛擬位址空間和系統資源。</span><span class="sxs-lookup"><span data-stu-id="9664f-108">All threads of a process share its virtual address space and system resources.</span></span> <span data-ttu-id="9664f-109">此外，每個執行緒都會維護例外狀況處理常式、排程優先權、執行緒區域儲存區、唯一的執行緒識別碼，以及系統將用來儲存執行緒內容的一組結構，直到排程為止。</span><span class="sxs-lookup"><span data-stu-id="9664f-109">In addition, each thread maintains exception handlers, a scheduling priority, thread local storage, a unique thread identifier, and a set of structures the system will use to save the thread context until it is scheduled.</span></span> <span data-ttu-id="9664f-110">*執行緒內容* 包括執行緒的電腦暫存器集合、核心堆疊、執行緒環境區塊，以及執行緒進程的位址空間中的使用者堆疊。</span><span class="sxs-lookup"><span data-stu-id="9664f-110">The *thread context* includes the thread's set of machine registers, the kernel stack, a thread environment block, and a user stack in the address space of the thread's process.</span></span> <span data-ttu-id="9664f-111">執行緒也可以有自己的安全性內容，可用來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="9664f-111">Threads can also have their own security context, which can be used for impersonating clients.</span></span>

<span data-ttu-id="9664f-112">Microsoft Windows 支援先占多 *任務*，這會造成同時執行多個進程之多個執行緒的效果。</span><span class="sxs-lookup"><span data-stu-id="9664f-112">Microsoft Windows supports *preemptive multitasking*, which creates the effect of simultaneous execution of multiple threads from multiple processes.</span></span> <span data-ttu-id="9664f-113">在多處理器的電腦上，系統可以同時執行與電腦上的處理器一樣多的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9664f-113">On a multiprocessor computer, the system can simultaneously execute as many threads as there are processors on the computer.</span></span>

<span data-ttu-id="9664f-114">*工作物件* 允許將進程群組作為一個單位來管理。</span><span class="sxs-lookup"><span data-stu-id="9664f-114">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="9664f-115">工作物件是 namable、安全實體、可共用的物件，可控制與其相關聯之進程的屬性。</span><span class="sxs-lookup"><span data-stu-id="9664f-115">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="9664f-116">在工作物件上執行的作業會影響與工作物件相關聯的所有進程。</span><span class="sxs-lookup"><span data-stu-id="9664f-116">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="9664f-117">應用程式可以使用 *執行緒集* 區來減少應用程式執行緒的數目，並提供工作者執行緒的管理。</span><span class="sxs-lookup"><span data-stu-id="9664f-117">An application can use the *thread pool* to reduce the number of application threads and provide management of the worker threads.</span></span> <span data-ttu-id="9664f-118">應用程式可以將工作專案排入佇列、建立工作與可等候控制碼的關聯、根據計時器自動排入佇列，以及使用 i/o 系結。</span><span class="sxs-lookup"><span data-stu-id="9664f-118">Applications can queue work items, associate work with waitable handles, automatically queue based on a timer, and bind with I/O.</span></span>

<span data-ttu-id="9664f-119">*使用者模式排程* (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9664f-119">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="9664f-120">應用程式可以在使用者模式中的 UMS 執行緒之間切換，而不需要涉及 [系統](scheduling.md) 排程器，而且如果核心中的 ums 執行緒區塊，則會重新取得處理器的控制權。</span><span class="sxs-lookup"><span data-stu-id="9664f-120">An application can switch between UMS threads in user mode without involving the [system scheduler](scheduling.md) and regain control of the processor if a UMS thread blocks in the kernel.</span></span> <span data-ttu-id="9664f-121">每個 UMS 執行緒都有自己的執行緒內容，而不是共用單一執行緒的執行緒內容。</span><span class="sxs-lookup"><span data-stu-id="9664f-121">Each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span> <span data-ttu-id="9664f-122">在使用者模式中切換執行緒的能力，讓 UMS 比需要少數系統呼叫的短時間工作專案的執行緒集區更有效率。</span><span class="sxs-lookup"><span data-stu-id="9664f-122">The ability to switch between threads in user mode makes UMS more efficient than thread pools for short-duration work items that require few system calls.</span></span>

<span data-ttu-id="9664f-123">*光纖* 是必須由應用程式手動排程的執行單位。</span><span class="sxs-lookup"><span data-stu-id="9664f-123">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="9664f-124">在排程執行緒的執行緒內容中執行纖程。</span><span class="sxs-lookup"><span data-stu-id="9664f-124">Fibers run in the context of the threads that schedule them.</span></span> <span data-ttu-id="9664f-125">每個執行緒都可以排程多個纖維。</span><span class="sxs-lookup"><span data-stu-id="9664f-125">Each thread can schedule multiple fibers.</span></span> <span data-ttu-id="9664f-126">一般而言，在設計完善的多執行緒應用程式上，纖維並不提供任何優點。</span><span class="sxs-lookup"><span data-stu-id="9664f-126">In general, fibers do not provide advantages over a well-designed multithreaded application.</span></span> <span data-ttu-id="9664f-127">不過，使用纖維可讓您更輕鬆地移植設計來排程其自有線程的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9664f-127">However, using fibers can make it easier to port applications that were designed to schedule their own threads.</span></span>

<span data-ttu-id="9664f-128">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9664f-128">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9664f-129">多工</span><span class="sxs-lookup"><span data-stu-id="9664f-129">Multitasking</span></span>](multitasking.md)
-   [<span data-ttu-id="9664f-130">排程</span><span class="sxs-lookup"><span data-stu-id="9664f-130">Scheduling</span></span>](scheduling.md)
-   [<span data-ttu-id="9664f-131">多個執行緒</span><span class="sxs-lookup"><span data-stu-id="9664f-131">Multiple Threads</span></span>](multiple-threads.md)
-   [<span data-ttu-id="9664f-132">子進程</span><span class="sxs-lookup"><span data-stu-id="9664f-132">Child Processes</span></span>](child-processes.md)
-   [<span data-ttu-id="9664f-133">執行緒集區</span><span class="sxs-lookup"><span data-stu-id="9664f-133">Thread Pools</span></span>](thread-pools.md)
-   [<span data-ttu-id="9664f-134">工作物件</span><span class="sxs-lookup"><span data-stu-id="9664f-134">Job Objects</span></span>](job-objects.md)
-   [<span data-ttu-id="9664f-135">使用者模式排程</span><span class="sxs-lookup"><span data-stu-id="9664f-135">User-Mode Scheduling</span></span>](user-mode-scheduling.md)
-   [<span data-ttu-id="9664f-136">纖維</span><span class="sxs-lookup"><span data-stu-id="9664f-136">Fibers</span></span>](fibers.md)

 

 



