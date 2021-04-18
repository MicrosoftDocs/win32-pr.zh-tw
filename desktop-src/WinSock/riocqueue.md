---
description: 針對使用 Winsock 註冊的 i/o 擴充功能的傳送和接收要求，指定用於 i/o 完成通知的完成佇列描述項。
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983435"
---
# <a name="rio_cq"></a><span data-ttu-id="36df0-103">RIO \_ CQ</span><span class="sxs-lookup"><span data-stu-id="36df0-103">RIO\_CQ</span></span>

<span data-ttu-id="36df0-104">**RIO \_ CQ** Typedef 會以 Winsock 註冊的 i/o 擴充功能，指定用於傳送和接收要求之 i/o 完成通知的完成佇列描述項。</span><span class="sxs-lookup"><span data-stu-id="36df0-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="36df0-105">**RIO \_ CQ**</span><span class="sxs-lookup"><span data-stu-id="36df0-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="36df0-106">一種資料類型，可指定傳送和接收要求用於 i/o 完成通知的完成佇列描述項。</span><span class="sxs-lookup"><span data-stu-id="36df0-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36df0-107">備註</span><span class="sxs-lookup"><span data-stu-id="36df0-107">Remarks</span></span>

<span data-ttu-id="36df0-108">**RIO \_ CQ** 物件是用來進行傳送和接收網路要求的 i/o 完成通知（由 Winsock 註冊的 i/o 擴充功能）。</span><span class="sxs-lookup"><span data-stu-id="36df0-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="36df0-109">當 **RIO \_ CQ** 完成佇列不是空的時，應用程式可以使用 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)函數來要求通知。</span><span class="sxs-lookup"><span data-stu-id="36df0-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="36df0-110">應用程式也可以使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)函式，以非封鎖方式，在 **RIO \_ CQ** 完成佇列的任何時間輪詢狀態。</span><span class="sxs-lookup"><span data-stu-id="36df0-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="36df0-111">**RIO \_ CQ** 物件是使用 [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)函數所建立。</span><span class="sxs-lookup"><span data-stu-id="36df0-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="36df0-112">在建立時，應用程式必須指定佇列的大小，以決定可以保留多少完成專案。</span><span class="sxs-lookup"><span data-stu-id="36df0-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="36df0-113">當應用程式呼叫 [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) 函式來取得 [**RIO \_ RQ**](riorqueue.md) 控制碼時，應用程式必須指定傳送完成的 **RIO \_ CQ** 控制碼，以及接收完成的 **RIO \_ CQ** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="36df0-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="36df0-114">當相同的佇列應該用於傳送和接收完成時，這些控制碼可能會完全相同。</span><span class="sxs-lookup"><span data-stu-id="36df0-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="36df0-115">**RIOCreateRequestQueue** 函式也需要最大未處理的傳送和接收作業數目，這些作業是針對相關聯的完成佇列或佇列的容量收費。</span><span class="sxs-lookup"><span data-stu-id="36df0-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="36df0-116">如果佇列沒有足夠的容量， **RIOCreateRequestQueue** 呼叫會失敗並出現 [WSAENOBUFS](windows-sockets-error-codes-2.md)。</span><span class="sxs-lookup"><span data-stu-id="36df0-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="36df0-117">建立 **RIO \_ CQ** 時，會設定完成佇列的通知行為。</span><span class="sxs-lookup"><span data-stu-id="36df0-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="36df0-118">如果是使用事件的完成佇列， [**RIO \_ 通知 \_ 完成**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)結構的 **類型** 成員會設定為 **RIO \_ 事件 \_ 完成**。</span><span class="sxs-lookup"><span data-stu-id="36df0-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="36df0-119">**EventHandle** 成員應該包含 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)或 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)函數所建立事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36df0-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="36df0-120">若要接收 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) 完成，應用程式應該使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 或類似的等候常式來等候指定的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36df0-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="36df0-121">如果應用程式計畫要重設並重複使用事件，則應用程式可以將 **NotifyReset** 成員設定為非零值，以降低額外負荷。</span><span class="sxs-lookup"><span data-stu-id="36df0-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="36df0-122">這會導致 **RIONotify** 函式在通知發生時自動重設事件。</span><span class="sxs-lookup"><span data-stu-id="36df0-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="36df0-123">這樣可減少呼叫 [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) 函式，以重設 **RIONotify** 函式呼叫之間的事件。</span><span class="sxs-lookup"><span data-stu-id="36df0-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="36df0-124">若為使用 i/o 完成埠的完成佇列， [**RIO \_ 通知 \_ 完成**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)結構的 **類型** 成員會設定為 **RIO \_ IOCP \_ 完成**。</span><span class="sxs-lookup"><span data-stu-id="36df0-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="36df0-125">**Iocp. IocpHandle** 成員應包含 [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)函式所建立之 i/o 完成埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36df0-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="36df0-126">若要接收 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) 完成，應用程式應該呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 或 [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) 函數。</span><span class="sxs-lookup"><span data-stu-id="36df0-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="36df0-127">應用程式應該提供完成佇列 [**的專用重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭物件，也可以使用 **Iocp CompletionKey** 成員來區別完成佇列上的 **RIONotify** 要求與其他 i/o 完成，包括其他完成佇列的 **RIONotify** 完成。</span><span class="sxs-lookup"><span data-stu-id="36df0-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="36df0-128">基於效率的目的， (**RIO \_ CQ** 結構) 和要求佇列 ([**RIO \_ RQ**](riorqueue.md) 結構) 不會受到同步處理原始物件的保護，因此可存取完成佇列。</span><span class="sxs-lookup"><span data-stu-id="36df0-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="36df0-129">如果您需要從多個執行緒存取完成或要求佇列，存取應由重要區段、精簡型讀取器寫入鎖定或類似的機制進行協調。</span><span class="sxs-lookup"><span data-stu-id="36df0-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="36df0-130">單一線程不需要此鎖定即可進行存取。</span><span class="sxs-lookup"><span data-stu-id="36df0-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="36df0-131">不同的執行緒可以存取個別的要求/完成佇列，而不需要鎖定。</span><span class="sxs-lookup"><span data-stu-id="36df0-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="36df0-132">只有當多個執行緒嘗試存取相同的佇列時，才會發生同步處理的需求。</span><span class="sxs-lookup"><span data-stu-id="36df0-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="36df0-133">如果多個執行緒發出相同通訊端上的傳送和接收，則也需要同步處理，因為傳送和接收作業會使用通訊端的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="36df0-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="36df0-134">如果有多個執行緒嘗試使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)來存取相同的 **RIO \_ CQ** ，則必須由重要區段、輕巧讀取器寫入器鎖定或類似的相互排除機制來協調存取。</span><span class="sxs-lookup"><span data-stu-id="36df0-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="36df0-135">如果未共用完成佇列，就不需要進行互斥。</span><span class="sxs-lookup"><span data-stu-id="36df0-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="36df0-136">當不再需要完成佇列時，應用程式可以使用 [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) 函式將其關閉。</span><span class="sxs-lookup"><span data-stu-id="36df0-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="36df0-137">**RIO \_ CQ** typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="36df0-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="36df0-138">不應直接使用 *Mswsockdef* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="36df0-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="36df0-139">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="36df0-139">Thread Safety</span></span>

<span data-ttu-id="36df0-140">如果有多個執行緒嘗試使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)來存取相同的 **RIO \_ CQ** ，則必須由重要區段、輕巧讀取器寫入器鎖定或類似的相互排除機制來協調存取。</span><span class="sxs-lookup"><span data-stu-id="36df0-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="36df0-141">如果未共用完成佇列，就不需要進行互斥。</span><span class="sxs-lookup"><span data-stu-id="36df0-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="36df0-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="36df0-142">Requirements</span></span>



| <span data-ttu-id="36df0-143">需求</span><span class="sxs-lookup"><span data-stu-id="36df0-143">Requirement</span></span> | <span data-ttu-id="36df0-144">值</span><span class="sxs-lookup"><span data-stu-id="36df0-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36df0-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36df0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="36df0-146">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36df0-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="36df0-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36df0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="36df0-148">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36df0-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="36df0-149">標頭</span><span class="sxs-lookup"><span data-stu-id="36df0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="36df0-150"><dt>Mswsockdef (包含 Mswsock) </dt></span><span class="sxs-lookup"><span data-stu-id="36df0-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36df0-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36df0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36df0-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="36df0-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="36df0-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="36df0-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="36df0-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="36df0-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="36df0-155">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="36df0-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="36df0-156">**重疊**</span><span class="sxs-lookup"><span data-stu-id="36df0-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="36df0-157">**RIO \_ 通知 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="36df0-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="36df0-158">**RIO \_ 通知 \_ 完成 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="36df0-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="36df0-159">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="36df0-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="36df0-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36df0-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="36df0-161">**RIOCreateCompletionQueue**</span><span class="sxs-lookup"><span data-stu-id="36df0-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="36df0-162">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="36df0-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="36df0-163">**RIODequeueCompletion**</span><span class="sxs-lookup"><span data-stu-id="36df0-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="36df0-164">**RIONotify**</span><span class="sxs-lookup"><span data-stu-id="36df0-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="36df0-165">**WSACreateEvent**</span><span class="sxs-lookup"><span data-stu-id="36df0-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="36df0-166">**WSAResetEvent**</span><span class="sxs-lookup"><span data-stu-id="36df0-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="36df0-167">**WSAWaitForMultipleEvents**</span><span class="sxs-lookup"><span data-stu-id="36df0-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
