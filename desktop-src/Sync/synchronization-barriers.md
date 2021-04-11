---
description: 同步處理屏障可讓多個執行緒等候，直到所有線程都已到達特定的執行點，然後再繼續任何執行緒。
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: 同步處理阻礙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194728"
---
# <a name="synchronization-barriers"></a><span data-ttu-id="1defa-103">同步處理阻礙</span><span class="sxs-lookup"><span data-stu-id="1defa-103">Synchronization Barriers</span></span>

<span data-ttu-id="1defa-104">同步處理屏障可讓多個執行緒等候，直到所有線程都已到達特定的執行點，然後再繼續任何執行緒。</span><span class="sxs-lookup"><span data-stu-id="1defa-104">A synchronization barrier enables multiple threads to wait until all threads have all reached a particular point of execution before any thread continues.</span></span> <span data-ttu-id="1defa-105">無法跨進程共用同步處理阻礙。</span><span class="sxs-lookup"><span data-stu-id="1defa-105">Synchronization barriers cannot be shared across processes.</span></span>

<span data-ttu-id="1defa-106">同步處理屏障適用于階段式計算，其中平行執行相同程式碼的執行緒必須全都完成一個階段，然後才繼續進行下一個階段。</span><span class="sxs-lookup"><span data-stu-id="1defa-106">Synchronization barriers are useful for phased computations, in which threads executing the same code in parallel must all complete one phase before moving on to the next.</span></span>

<span data-ttu-id="1defa-107">若要建立同步處理屏障，請呼叫 [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) 函式，並指定執行緒的最大數目，以及執行緒在封鎖之前應該旋轉多少次。</span><span class="sxs-lookup"><span data-stu-id="1defa-107">To create a synchronization barrier, call the [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) function and specify a maximum number of threads and how many times a thread should spin before it blocks.</span></span> <span data-ttu-id="1defa-108">然後啟動將使用屏障的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1defa-108">Then launch the threads that will use the barrier.</span></span> <span data-ttu-id="1defa-109">在每個執行緒完成其工作之後，它會呼叫 [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) 來等候關卡。</span><span class="sxs-lookup"><span data-stu-id="1defa-109">After each thread finishes its work, it calls [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) to wait at the barrier.</span></span> <span data-ttu-id="1defa-110">**EnterSynchronizationBarrier** 函式會封鎖每個執行緒，直到關卡中封鎖的執行緒數目達到屏障的執行緒計數上限為止，此時 **EnterSynchronizationBarrier** 會解除封鎖所有線程。</span><span class="sxs-lookup"><span data-stu-id="1defa-110">The **EnterSynchronizationBarrier** function blocks each thread until the number of threads blocked in the barrier reaches the maximum thread count for the barrier, at which point **EnterSynchronizationBarrier** unblocks all the threads.</span></span> <span data-ttu-id="1defa-111">**EnterSynchronizationBarrier** 函式只會針對其中一個進入屏障的執行緒傳回 **TRUE** ，並針對所有其他執行緒傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1defa-111">The **EnterSynchronizationBarrier** function returns **TRUE** for exactly one of the threads that entered the barrier, and returns **FALSE** for all other threads.</span></span>

<span data-ttu-id="1defa-112">若要釋放不再需要的同步處理屏障，請呼叫 [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)。</span><span class="sxs-lookup"><span data-stu-id="1defa-112">To release a synchronization barrier when it is no longer needed, call [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier).</span></span> <span data-ttu-id="1defa-113">呼叫 [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) 後立即呼叫此函式是安全的，因為該函式可確保所有線程在釋放之前都已完成使用屏障。</span><span class="sxs-lookup"><span data-stu-id="1defa-113">It is safe to call this function immediately after calling [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) because that function ensures that all threads have finished using the barrier before it is released.</span></span>

<span data-ttu-id="1defa-114">如果不會刪除同步處理屏障，執行緒可以在進入屏障時，指定 **同步處理 \_ 屏障 \_ 旗標 \_ 無 \_ 刪除旗標** 。</span><span class="sxs-lookup"><span data-stu-id="1defa-114">If a synchronization barrier will never be deleted, threads can specify the **SYNCHRONIZATION\_BARRIER\_FLAGS\_NO\_DELETE** flag when they enter the barrier.</span></span> <span data-ttu-id="1defa-115">使用屏障的所有線程都必須指定此旗標;如果有任何執行緒沒有，則會忽略旗標。</span><span class="sxs-lookup"><span data-stu-id="1defa-115">All threads using the barrier must specify this flag; if any thread does not, the flag is ignored.</span></span> <span data-ttu-id="1defa-116">此旗標會導致函式略過刪除安全所需的額外工作，這可改善效能。</span><span class="sxs-lookup"><span data-stu-id="1defa-116">This flag causes the function to skip the extra work required for deletion safety, which can improve performance.</span></span> <span data-ttu-id="1defa-117">請注意，在此旗標生效時刪除關卡可能會導致不正確控制碼存取，以及一或多個永久封鎖的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1defa-117">Note that deleting a barrier while this flag is in effect may result in an invalid handle access and one or more permanently blocked threads.</span></span>

 

 



