---
description: 事件物件是一種同步處理物件，其狀態可以明確設定為使用 SetEvent 函式來發出信號。 以下是兩種類型的事件物件。
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: " (同步處理的事件物件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ef4f5102df91cabb76529c9d4a9958859418aa
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102129"
---
# <a name="event-objects-synchronization"></a><span data-ttu-id="1055f-104"> (同步處理的事件物件) </span><span class="sxs-lookup"><span data-stu-id="1055f-104">Event Objects (Synchronization)</span></span>

<span data-ttu-id="1055f-105">*事件物件* 是一種同步處理物件，其狀態可以明確設定為使用 [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent)函式來發出信號。</span><span class="sxs-lookup"><span data-stu-id="1055f-105">An *event object* is a synchronization object whose state can be explicitly set to signaled by use of the [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) function.</span></span> <span data-ttu-id="1055f-106">以下是兩種類型的事件物件。</span><span class="sxs-lookup"><span data-stu-id="1055f-106">Following are the two types of event object.</span></span>



| <span data-ttu-id="1055f-107">Object</span><span class="sxs-lookup"><span data-stu-id="1055f-107">Object</span></span>             | <span data-ttu-id="1055f-108">描述</span><span class="sxs-lookup"><span data-stu-id="1055f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1055f-109">手動重設事件</span><span class="sxs-lookup"><span data-stu-id="1055f-109">Manual-reset event</span></span> | <span data-ttu-id="1055f-110">在 [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) 函式明確重設為未收到信號之前，其狀態會維持為信號的事件物件。</span><span class="sxs-lookup"><span data-stu-id="1055f-110">An event object whose state remains signaled until it is explicitly reset to nonsignaled by the [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="1055f-111">當其收到信號時，可以釋出任何數目的等候中線程，或後續在其中一個 [等候](wait-functions.md)函式中指定相同事件物件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1055f-111">While it is signaled, any number of waiting threads, or threads that subsequently specify the same event object in one of the [wait functions](wait-functions.md), can be released.</span></span>                                                                                                        |
| <span data-ttu-id="1055f-112">自動重設事件</span><span class="sxs-lookup"><span data-stu-id="1055f-112">Auto-reset event</span></span>   | <span data-ttu-id="1055f-113">事件物件，其狀態會保持為信號，直到釋放單一等候中的執行緒為止，此時系統會自動將狀態設定為未收到信號。</span><span class="sxs-lookup"><span data-stu-id="1055f-113">An event object whose state remains signaled until a single waiting thread is released, at which time the system automatically sets the state to nonsignaled.</span></span> <span data-ttu-id="1055f-114">如果沒有執行緒在等候，事件物件的狀態會維持已收到信號。</span><span class="sxs-lookup"><span data-stu-id="1055f-114">If no threads are waiting, the event object's state remains signaled.</span></span> <span data-ttu-id="1055f-115">如果有多個執行緒正在等候，則會選取等候中的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1055f-115">If more than one thread is waiting, a waiting thread is selected.</span></span> <span data-ttu-id="1055f-116">請勿採用先進先出 (FIFO) 順序。</span><span class="sxs-lookup"><span data-stu-id="1055f-116">Do not assume a first-in, first-out (FIFO) order.</span></span> <span data-ttu-id="1055f-117">外來事件（例如核心模式 Apc）可以變更等候順序。</span><span class="sxs-lookup"><span data-stu-id="1055f-117">External events such as kernel-mode APCs can change the wait order.</span></span><br/> |



 

<span data-ttu-id="1055f-118">事件物件適用于將信號傳送給指出發生特定事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1055f-118">The event object is useful in sending a signal to a thread indicating that a particular event has occurred.</span></span> <span data-ttu-id="1055f-119">例如，在重迭的輸入和輸出中，系統會在重迭的作業完成時，將指定的事件物件設定為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="1055f-119">For example, in overlapped input and output, the system sets a specified event object to the signaled state when the overlapped operation has been completed.</span></span> <span data-ttu-id="1055f-120">單一線程可以在數個同時重迭的作業中指定不同的事件物件，然後使用其中一個多物件 [等候](wait-functions.md) 函式來等候任何一個事件物件的狀態被發出信號。</span><span class="sxs-lookup"><span data-stu-id="1055f-120">A single thread can specify different event objects in several simultaneous overlapped operations, then use one of the multiple-object [wait functions](wait-functions.md) to wait for the state of any one of the event objects to be signaled.</span></span>

<span data-ttu-id="1055f-121">執行緒使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 或 [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) 函數來建立事件物件。</span><span class="sxs-lookup"><span data-stu-id="1055f-121">A thread uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) or [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) function to create an event object.</span></span> <span data-ttu-id="1055f-122">建立執行緒會指定物件的初始狀態，以及它是否為手動重設或自動重設事件物件。</span><span class="sxs-lookup"><span data-stu-id="1055f-122">The creating thread specifies the initial state of the object and whether it is a manual-reset or auto-reset event object.</span></span> <span data-ttu-id="1055f-123">建立執行緒也可以指定事件物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="1055f-123">The creating thread can also specify a name for the event object.</span></span> <span data-ttu-id="1055f-124">其他進程中的執行緒可以藉由在 [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) 函式的呼叫中指定其名稱，來開啟現有事件物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1055f-124">Threads in other processes can open a handle to an existing event object by specifying its name in a call to the [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) function.</span></span> <span data-ttu-id="1055f-125">如需 mutex、事件、信號和計時器物件之名稱的詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。</span><span class="sxs-lookup"><span data-stu-id="1055f-125">For additional information about names for mutex, event, semaphore, and timer objects, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1055f-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1055f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1055f-127">使用事件物件</span><span class="sxs-lookup"><span data-stu-id="1055f-127">Using Event Objects</span></span>](using-event-objects.md)
</dt> </dl>

 

 
