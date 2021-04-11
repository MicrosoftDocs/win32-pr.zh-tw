---
description: 建議的指導方針是盡可能使用較少的執行緒，因此可將系統資源的使用降至最低。
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: 多工考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115553"
---
# <a name="multitasking-considerations"></a><span data-ttu-id="b02b6-103">多工考慮</span><span class="sxs-lookup"><span data-stu-id="b02b6-103">Multitasking Considerations</span></span>

<span data-ttu-id="b02b6-104">建議的指導方針是盡可能使用較少的執行緒，因此可將系統資源的使用降至最低。</span><span class="sxs-lookup"><span data-stu-id="b02b6-104">The recommended guideline is to use as few threads as possible, thereby minimizing the use of system resources.</span></span> <span data-ttu-id="b02b6-105">這樣可以提高執行效能。</span><span class="sxs-lookup"><span data-stu-id="b02b6-105">This improves performance.</span></span> <span data-ttu-id="b02b6-106">當您設計應用程式時，多工具有資源需求和潛在衝突。</span><span class="sxs-lookup"><span data-stu-id="b02b6-106">Multitasking has resource requirements and potential conflicts to be considered when designing your application.</span></span> <span data-ttu-id="b02b6-107">資源需求如下：</span><span class="sxs-lookup"><span data-stu-id="b02b6-107">The resource requirements are as follows:</span></span>

-   <span data-ttu-id="b02b6-108">系統會耗用記憶體給進程和執行緒所需的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b02b6-108">The system consumes memory for the context information required by both processes and threads.</span></span> <span data-ttu-id="b02b6-109">因此，可建立的進程和執行緒數目會受到可用記憶體的限制。</span><span class="sxs-lookup"><span data-stu-id="b02b6-109">Therefore, the number of processes and threads that can be created is limited by available memory.</span></span>
-   <span data-ttu-id="b02b6-110">追蹤大量執行緒會耗用大量的處理器時間。</span><span class="sxs-lookup"><span data-stu-id="b02b6-110">Keeping track of a large number of threads consumes significant processor time.</span></span> <span data-ttu-id="b02b6-111">如果有太多執行緒，大部分的執行緒將無法進行大幅的進展。</span><span class="sxs-lookup"><span data-stu-id="b02b6-111">If there are too many threads, most of them will not be able to make significant progress.</span></span> <span data-ttu-id="b02b6-112">如果大多數目前的執行緒都在一個處理序中，其他處理序中的執行緒排程頻率就會較低。</span><span class="sxs-lookup"><span data-stu-id="b02b6-112">If most of the current threads are in one process, threads in other processes are scheduled less frequently.</span></span>

<span data-ttu-id="b02b6-113">提供對資源的共用存取權可能會造成衝突。</span><span class="sxs-lookup"><span data-stu-id="b02b6-113">Providing shared access to resources can create conflicts.</span></span> <span data-ttu-id="b02b6-114">若要避免這些問題，您必須同步處理對共用資源的存取。</span><span class="sxs-lookup"><span data-stu-id="b02b6-114">To avoid them, you must synchronize access to shared resources.</span></span> <span data-ttu-id="b02b6-115">這適用于系統資源 (例如通訊埠) 、多個進程所共用的資源 (例如) 的檔案控制代碼，或單一進程的資源 (例如由多個執行緒存取的全域變數) 。</span><span class="sxs-lookup"><span data-stu-id="b02b6-115">This is true for system resources (such as communications ports), resources shared by multiple processes (such as file handles), or the resources of a single process (such as global variables) accessed by multiple threads.</span></span> <span data-ttu-id="b02b6-116">如果無法在相同或不同的進程中正確地同步存取 (，) 可能會導致像是鎖死和競爭情況等問題。</span><span class="sxs-lookup"><span data-stu-id="b02b6-116">Failure to synchronize access properly (in the same or in different processes) can lead to problems such as deadlock and race conditions.</span></span> <span data-ttu-id="b02b6-117">您可以用來在多個執行緒之間協調資源分享的同步處理物件和函式。</span><span class="sxs-lookup"><span data-stu-id="b02b6-117">The synchronization objects and functions you can use to coordinate resource sharing among multiple threads.</span></span> <span data-ttu-id="b02b6-118">如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="b02b6-118">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span> <span data-ttu-id="b02b6-119">減少執行緒數目可讓您更輕鬆且更有效率地同步處理資源。</span><span class="sxs-lookup"><span data-stu-id="b02b6-119">Reducing the number of threads makes it easier and more effective to synchronize resources.</span></span>

<span data-ttu-id="b02b6-120">多執行緒應用程式的良好設計是管線伺服器。</span><span class="sxs-lookup"><span data-stu-id="b02b6-120">A good design for a multithreaded application is the pipeline server.</span></span> <span data-ttu-id="b02b6-121">在這個設計中，您會為每個處理器建立一個執行緒，並建立應用程式維護內容資訊的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="b02b6-121">In this design, you create one thread per processor and build queues of requests for which the application maintains the context information.</span></span> <span data-ttu-id="b02b6-122">執行緒會處理佇列中的所有要求，然後才處理下一個佇列中的要求。</span><span class="sxs-lookup"><span data-stu-id="b02b6-122">A thread would process all requests in a queue before processing requests in the next queue.</span></span>

 

 



