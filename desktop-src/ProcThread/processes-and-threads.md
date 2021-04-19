---
description: 執行多工處理、排程優先順序，以及處理處理常式、執行緒、執行緒集區、工作物件和纖維。 使用使用者模式排程來排程執行緒。
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: 處理序和執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982419"
---
# <a name="processes-and-threads"></a><span data-ttu-id="d7d87-104">處理序和執行緒</span><span class="sxs-lookup"><span data-stu-id="d7d87-104">Processes and Threads</span></span>

<span data-ttu-id="d7d87-105">應用程式是由一或多個進程所組成。</span><span class="sxs-lookup"><span data-stu-id="d7d87-105">An application consists of one or more processes.</span></span> <span data-ttu-id="d7d87-106">以最簡單的程式 *來說，程式* 是執行中的程式。</span><span class="sxs-lookup"><span data-stu-id="d7d87-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="d7d87-107">一或多個執行緒會在進程的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="d7d87-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="d7d87-108">*執行緒* 是作業系統配置處理器時間的基本單位。</span><span class="sxs-lookup"><span data-stu-id="d7d87-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="d7d87-109">執行緒可以執行程式碼的任何部分，包括目前正在由另一個執行緒執行的元件。</span><span class="sxs-lookup"><span data-stu-id="d7d87-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="d7d87-110">*工作物件* 允許將進程群組作為一個單位來管理。</span><span class="sxs-lookup"><span data-stu-id="d7d87-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="d7d87-111">工作物件是 namable、安全實體、可共用的物件，可控制與其相關聯之進程的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d87-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="d7d87-112">在工作物件上執行的作業會影響與工作物件相關聯的所有進程。</span><span class="sxs-lookup"><span data-stu-id="d7d87-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="d7d87-113">*執行緒* 集區是工作者執行緒的集合，可代表應用程式有效率地執行非同步回呼。</span><span class="sxs-lookup"><span data-stu-id="d7d87-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="d7d87-114">執行緒集區主要是用來減少應用程式執行緒的數目，並提供工作者執行緒的管理。</span><span class="sxs-lookup"><span data-stu-id="d7d87-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="d7d87-115">*光纖* 是必須由應用程式手動排程的執行單位。</span><span class="sxs-lookup"><span data-stu-id="d7d87-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="d7d87-116">在排程執行緒的執行緒內容中執行纖程。</span><span class="sxs-lookup"><span data-stu-id="d7d87-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="d7d87-117">*使用者模式排程* (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。</span><span class="sxs-lookup"><span data-stu-id="d7d87-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="d7d87-118">UMS 執行緒與 [纖維](fibers.md) 不同之處在于，每個 ums 執行緒都有自己的執行緒內容，而不是共用單一執行緒的執行緒內容。</span><span class="sxs-lookup"><span data-stu-id="d7d87-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="d7d87-119">進程和執行緒的新功能</span><span class="sxs-lookup"><span data-stu-id="d7d87-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="d7d87-120">關於處理序和執行緒</span><span class="sxs-lookup"><span data-stu-id="d7d87-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="d7d87-121">使用進程和執行緒</span><span class="sxs-lookup"><span data-stu-id="d7d87-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="d7d87-122">進程和執行緒參考</span><span class="sxs-lookup"><span data-stu-id="d7d87-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



