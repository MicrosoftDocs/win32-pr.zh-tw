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
# <a name="rio_cq"></a>RIO \_ CQ

**RIO \_ CQ** Typedef 會以 Winsock 註冊的 i/o 擴充功能，指定用於傳送和接收要求之 i/o 完成通知的完成佇列描述項。


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**RIO \_ CQ**
</dt> <dd>

一種資料類型，可指定傳送和接收要求用於 i/o 完成通知的完成佇列描述項。

</dd> </dl>

## <a name="remarks"></a>備註

**RIO \_ CQ** 物件是用來進行傳送和接收網路要求的 i/o 完成通知（由 Winsock 註冊的 i/o 擴充功能）。

當 **RIO \_ CQ** 完成佇列不是空的時，應用程式可以使用 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)函數來要求通知。 應用程式也可以使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)函式，以非封鎖方式，在 **RIO \_ CQ** 完成佇列的任何時間輪詢狀態。

**RIO \_ CQ** 物件是使用 [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)函數所建立。 在建立時，應用程式必須指定佇列的大小，以決定可以保留多少完成專案。 當應用程式呼叫 [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) 函式來取得 [**RIO \_ RQ**](riorqueue.md) 控制碼時，應用程式必須指定傳送完成的 **RIO \_ CQ** 控制碼，以及接收完成的 **RIO \_ CQ** 控制碼。 當相同的佇列應該用於傳送和接收完成時，這些控制碼可能會完全相同。 **RIOCreateRequestQueue** 函式也需要最大未處理的傳送和接收作業數目，這些作業是針對相關聯的完成佇列或佇列的容量收費。 如果佇列沒有足夠的容量， **RIOCreateRequestQueue** 呼叫會失敗並出現 [WSAENOBUFS](windows-sockets-error-codes-2.md)。

建立 **RIO \_ CQ** 時，會設定完成佇列的通知行為。

如果是使用事件的完成佇列， [**RIO \_ 通知 \_ 完成**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)結構的 **類型** 成員會設定為 **RIO \_ 事件 \_ 完成**。 **EventHandle** 成員應該包含 [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)或 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)函數所建立事件的控制碼。 若要接收 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) 完成，應用程式應該使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 或類似的等候常式來等候指定的事件控制碼。 如果應用程式計畫要重設並重複使用事件，則應用程式可以將 **NotifyReset** 成員設定為非零值，以降低額外負荷。 這會導致 **RIONotify** 函式在通知發生時自動重設事件。 這樣可減少呼叫 [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) 函式，以重設 **RIONotify** 函式呼叫之間的事件。

若為使用 i/o 完成埠的完成佇列， [**RIO \_ 通知 \_ 完成**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)結構的 **類型** 成員會設定為 **RIO \_ IOCP \_ 完成**。 **Iocp. IocpHandle** 成員應包含 [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)函式所建立之 i/o 完成埠的控制碼。 若要接收 [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) 完成，應用程式應該呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 或 [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) 函數。 應用程式應該提供完成佇列 [**的專用重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭物件，也可以使用 **Iocp CompletionKey** 成員來區別完成佇列上的 **RIONotify** 要求與其他 i/o 完成，包括其他完成佇列的 **RIONotify** 完成。

> [!Note]  
> 基於效率的目的， (**RIO \_ CQ** 結構) 和要求佇列 ([**RIO \_ RQ**](riorqueue.md) 結構) 不會受到同步處理原始物件的保護，因此可存取完成佇列。 如果您需要從多個執行緒存取完成或要求佇列，存取應由重要區段、精簡型讀取器寫入鎖定或類似的機制進行協調。 單一線程不需要此鎖定即可進行存取。 不同的執行緒可以存取個別的要求/完成佇列，而不需要鎖定。 只有當多個執行緒嘗試存取相同的佇列時，才會發生同步處理的需求。 如果多個執行緒發出相同通訊端上的傳送和接收，則也需要同步處理，因為傳送和接收作業會使用通訊端的要求佇列。

 

如果有多個執行緒嘗試使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)來存取相同的 **RIO \_ CQ** ，則必須由重要區段、輕巧讀取器寫入器鎖定或類似的相互排除機制來協調存取。 如果未共用完成佇列，就不需要進行互斥。

當不再需要完成佇列時，應用程式可以使用 [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) 函式將其關閉。

**RIO \_ CQ** typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。 不應直接使用 *Mswsockdef* 標頭檔。

## <a name="thread-safety"></a>執行緒安全性

如果有多個執行緒嘗試使用 [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)來存取相同的 **RIO \_ CQ** ，則必須由重要區段、輕巧讀取器寫入器鎖定或類似的相互排除機制來協調存取。 如果未共用完成佇列，就不需要進行互斥。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Mswsockdef (包含 Mswsock) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**重疊**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**RIO \_ 通知 \_ 完成**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**RIO \_ 通知 \_ 完成 \_ 類型**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**RIO \_ RQ**](riorqueue.md)
</dt> <dt>

[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
