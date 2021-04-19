---
description: 列出可由登記接收的不同通知類型。
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: 'NOTIFICATION_MASK (KtmTypes) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980546"
---
# <a name="notification_mask"></a>通知 \_ 遮罩

列出可由登記接收的不同通知類型。

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**交易 \_ 通知 \_ 遮罩**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



遮罩，表示交易通知的所有有效位。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**交易 \_ 通知 \_ PREPREPARE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



當用戶端呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) ，且沒有 resource MANAGER (RM) 支援單一階段認可或高階交易管理員 (TM) 呼叫 [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)，就會呼叫此通知。 RMs 會收到此通知，指出他們應該完成任何可能導致其他 RMs 在交易中登記的工作，例如清除其快取。 完成這些作業之後，RM 必須呼叫 [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)。 若要接收此通知，RM 也必須支援 **交易 \_ 通知 \_ 準備** 和 **交易 \_ 通知 \_ 認可**。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**交易 \_ 通知 \_ 準備**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



此通知會在 **交易 \_ 通知 \_ PREPREPARE** 處理完成之後呼叫。 它會通知 RM 完成與此登記相關聯的所有工作，以保證認可作業可能會成功，且中止作業也會成功。 一般來說，交易的大部分工作都是在準備階段期間完成。 對於永久性 RMs，它們必須在呼叫 [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) 函式之前先記錄其狀態。 這是 RM 要求回復交易的最後機會。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**交易 \_ 通知 \_ 認可**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



此通知會通知 RM 完成與此登記相關聯的所有工作。 一般而言，RM 會釋放任何鎖定，釋出回復交易所需的任何資訊。 RM 必須在完成這些作業時呼叫 [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) 函式來回應。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**交易 \_ 通知 \_ 回復**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



此通知會通知 RM 要復原與交易相關聯的所有已完成工作。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**交易 \_ 通知 \_ PREPREPARE \_ 完成**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



此通知會向上層 TM 發出預先準備作業已順利完成的信號。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**交易 \_ 通知 \_ 準備 \_ 完成**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



此通知會向上層 TM 發出準備作業已順利完成。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**交易 \_ 通知 \_ 認可 \_ 完成**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



此通知會向上層 TM 發出認可作業已順利完成的信號。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**交易 \_ 通知 \_ 回復 \_ 完成**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



此通知會向上層 TM 發出回復作業已順利完成的信號。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**交易 \_ 通知 \_ 復原**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



此通知會通知 RMs，因為必須重新傳遞交易結果，所以應復原其狀態。 例如，當 RM 復原時，以及有不確定的交易時。 此通知會在不確定狀態解決之後傳遞。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**交易 \_ 通知 \_ 單一 \_ 階段 \_ 認可**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



此通知會通知 RM 完成並認可交易，而不使用兩階段認可通訊協定。 如果 RM 想要使用兩階段作業，它必須藉由呼叫 [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) 函式來回應。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**交易 \_ 通知 \_ 委派 \_ 認可**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM 會向高階 TM 發出信號，以執行認可作業。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**交易 \_ 通知 \_ 復原 \_ 查詢**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM 會向優質 TM 發出信號，以查詢不確定交易的狀態。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**交易 \_ 通知 \_ 登記 \_ PREPREPARE**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



此通知會向上層 TM 發出通知，表示必須在指定的登錄上傳遞預先準備的通知。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**交易 \_ 通知 \_ 上次 \_ 復原**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



此通知表示此 RM 的復原操作已完成。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**交易 \_ 通知 \_ INDOUBT**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



指定的交易處於不確定的狀態。 當交易已備妥，但沒有高階的交易管理員 (TM) 可用時，RM 會在復原作業期間收到這項通知。 例如，當交易牽涉到遠端 TM 但該節點無法使用時，其節點無法使用，或本機 [分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) 服務無法使用，交易狀態為不確定。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**交易 \_ 通知 \_ TM \_ 線上**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



TM 已上線並接受要求。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**交易 \_ 通知 \_ 要求 \_ 結果**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



向 RMs 發出通知，指出有結果資訊可供使用，而且應該提出該資訊的要求。


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**交易 \_ 通知 \_ 認可 \_ 完成**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



保留的。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                            |
| 標頭<br/>                   | <dl> <dt>KtmTypes (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[核心交易管理員常數](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**交易 \_ 通知**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

