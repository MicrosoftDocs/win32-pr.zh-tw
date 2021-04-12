---
description: 當有兩個或多個具有不同優先順序的執行緒在競爭中進行排程時，就會發生優先權反轉。
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: 優先權反轉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319159"
---
# <a name="priority-inversion"></a><span data-ttu-id="13c71-103">優先權反轉</span><span class="sxs-lookup"><span data-stu-id="13c71-103">Priority Inversion</span></span>

<span data-ttu-id="13c71-104">當有兩個或多個具有不同優先順序的執行緒在競爭中進行排程時，就會發生優先權反轉。</span><span class="sxs-lookup"><span data-stu-id="13c71-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="13c71-105">請考慮使用三個執行緒的簡單案例：執行緒1、執行緒2和執行緒3。</span><span class="sxs-lookup"><span data-stu-id="13c71-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="13c71-106">執行緒1是高優先順序，可做好排程。</span><span class="sxs-lookup"><span data-stu-id="13c71-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="13c71-107">執行緒2（低優先順序執行緒）正在執行重要區段中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="13c71-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="13c71-108">執行緒1（高優先順序執行緒）開始等待中的執行緒2的共用資源。</span><span class="sxs-lookup"><span data-stu-id="13c71-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="13c71-109">執行緒3有中優先順序。</span><span class="sxs-lookup"><span data-stu-id="13c71-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="13c71-110">執行緒3會收到所有處理器時間，因為高優先順序的執行緒 (執行緒 1) 正在等候低優先順序執行緒 (執行緒 2) 的共用資源。</span><span class="sxs-lookup"><span data-stu-id="13c71-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="13c71-111">執行緒2不會離開重要區段，因為它沒有最高的優先順序，因此不會進行排程。</span><span class="sxs-lookup"><span data-stu-id="13c71-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="13c71-112">排程器會藉由隨機提升就緒執行緒的優先順序來解決這個問題 (在此案例中，低優先順序鎖定持有人) 。</span><span class="sxs-lookup"><span data-stu-id="13c71-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="13c71-113">低優先順序執行緒執行的時間夠長，無法結束重要區段，而高優先順序執行緒可以進入重要區段。</span><span class="sxs-lookup"><span data-stu-id="13c71-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="13c71-114">如果低優先順序執行緒在第一次沒有足夠的 CPU 時間來結束重要區段，則會在下一次排程期間得到另一個機會。</span><span class="sxs-lookup"><span data-stu-id="13c71-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



