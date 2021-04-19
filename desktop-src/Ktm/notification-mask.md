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
# <a name="notification_mask"></a><span data-ttu-id="1918b-103">通知 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="1918b-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="1918b-104">列出可由登記接收的不同通知類型。</span><span class="sxs-lookup"><span data-stu-id="1918b-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="1918b-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**交易 \_ 通知 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="1918b-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1918b-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="1918b-107">遮罩，表示交易通知的所有有效位。</span><span class="sxs-lookup"><span data-stu-id="1918b-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**交易 \_ 通知 \_ PREPREPARE**</span><span class="sxs-lookup"><span data-stu-id="1918b-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1918b-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="1918b-110">當用戶端呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) ，且沒有 resource MANAGER (RM) 支援單一階段認可或高階交易管理員 (TM) 呼叫 [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)，就會呼叫此通知。</span><span class="sxs-lookup"><span data-stu-id="1918b-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="1918b-111">RMs 會收到此通知，指出他們應該完成任何可能導致其他 RMs 在交易中登記的工作，例如清除其快取。</span><span class="sxs-lookup"><span data-stu-id="1918b-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="1918b-112">完成這些作業之後，RM 必須呼叫 [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)。</span><span class="sxs-lookup"><span data-stu-id="1918b-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="1918b-113">若要接收此通知，RM 也必須支援 **交易 \_ 通知 \_ 準備** 和 **交易 \_ 通知 \_ 認可**。</span><span class="sxs-lookup"><span data-stu-id="1918b-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**交易 \_ 通知 \_ 準備**</span><span class="sxs-lookup"><span data-stu-id="1918b-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1918b-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="1918b-116">此通知會在 **交易 \_ 通知 \_ PREPREPARE** 處理完成之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="1918b-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="1918b-117">它會通知 RM 完成與此登記相關聯的所有工作，以保證認可作業可能會成功，且中止作業也會成功。</span><span class="sxs-lookup"><span data-stu-id="1918b-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="1918b-118">一般來說，交易的大部分工作都是在準備階段期間完成。</span><span class="sxs-lookup"><span data-stu-id="1918b-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="1918b-119">對於永久性 RMs，它們必須在呼叫 [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) 函式之前先記錄其狀態。</span><span class="sxs-lookup"><span data-stu-id="1918b-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="1918b-120">這是 RM 要求回復交易的最後機會。</span><span class="sxs-lookup"><span data-stu-id="1918b-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**交易 \_ 通知 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="1918b-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1918b-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="1918b-123">此通知會通知 RM 完成與此登記相關聯的所有工作。</span><span class="sxs-lookup"><span data-stu-id="1918b-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="1918b-124">一般而言，RM 會釋放任何鎖定，釋出回復交易所需的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="1918b-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="1918b-125">RM 必須在完成這些作業時呼叫 [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) 函式來回應。</span><span class="sxs-lookup"><span data-stu-id="1918b-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**交易 \_ 通知 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="1918b-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1918b-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="1918b-128">此通知會通知 RM 要復原與交易相關聯的所有已完成工作。</span><span class="sxs-lookup"><span data-stu-id="1918b-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**交易 \_ 通知 \_ PREPREPARE \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="1918b-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1918b-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="1918b-131">此通知會向上層 TM 發出預先準備作業已順利完成的信號。</span><span class="sxs-lookup"><span data-stu-id="1918b-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**交易 \_ 通知 \_ 準備 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="1918b-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="1918b-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="1918b-134">此通知會向上層 TM 發出準備作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="1918b-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**交易 \_ 通知 \_ 認可 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="1918b-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="1918b-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="1918b-137">此通知會向上層 TM 發出認可作業已順利完成的信號。</span><span class="sxs-lookup"><span data-stu-id="1918b-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**交易 \_ 通知 \_ 回復 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="1918b-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1918b-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="1918b-140">此通知會向上層 TM 發出回復作業已順利完成的信號。</span><span class="sxs-lookup"><span data-stu-id="1918b-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**交易 \_ 通知 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="1918b-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="1918b-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="1918b-143">此通知會通知 RMs，因為必須重新傳遞交易結果，所以應復原其狀態。</span><span class="sxs-lookup"><span data-stu-id="1918b-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="1918b-144">例如，當 RM 復原時，以及有不確定的交易時。</span><span class="sxs-lookup"><span data-stu-id="1918b-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="1918b-145">此通知會在不確定狀態解決之後傳遞。</span><span class="sxs-lookup"><span data-stu-id="1918b-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**交易 \_ 通知 \_ 單一 \_ 階段 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="1918b-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="1918b-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="1918b-148">此通知會通知 RM 完成並認可交易，而不使用兩階段認可通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1918b-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="1918b-149">如果 RM 想要使用兩階段作業，它必須藉由呼叫 [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) 函式來回應。</span><span class="sxs-lookup"><span data-stu-id="1918b-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**交易 \_ 通知 \_ 委派 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="1918b-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="1918b-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="1918b-152">KTM 會向高階 TM 發出信號，以執行認可作業。</span><span class="sxs-lookup"><span data-stu-id="1918b-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**交易 \_ 通知 \_ 復原 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="1918b-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="1918b-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="1918b-155">KTM 會向優質 TM 發出信號，以查詢不確定交易的狀態。</span><span class="sxs-lookup"><span data-stu-id="1918b-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**交易 \_ 通知 \_ 登記 \_ PREPREPARE**</span><span class="sxs-lookup"><span data-stu-id="1918b-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="1918b-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-158">此通知會向上層 TM 發出通知，表示必須在指定的登錄上傳遞預先準備的通知。</span><span class="sxs-lookup"><span data-stu-id="1918b-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**交易 \_ 通知 \_ 上次 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="1918b-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="1918b-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-161">此通知表示此 RM 的復原操作已完成。</span><span class="sxs-lookup"><span data-stu-id="1918b-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**交易 \_ 通知 \_ INDOUBT**</span><span class="sxs-lookup"><span data-stu-id="1918b-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="1918b-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-164">指定的交易處於不確定的狀態。</span><span class="sxs-lookup"><span data-stu-id="1918b-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="1918b-165">當交易已備妥，但沒有高階的交易管理員 (TM) 可用時，RM 會在復原作業期間收到這項通知。</span><span class="sxs-lookup"><span data-stu-id="1918b-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="1918b-166">例如，當交易牽涉到遠端 TM 但該節點無法使用時，其節點無法使用，或本機 [分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) 服務無法使用，交易狀態為不確定。</span><span class="sxs-lookup"><span data-stu-id="1918b-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**交易 \_ 通知 \_ TM \_ 線上**</span><span class="sxs-lookup"><span data-stu-id="1918b-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="1918b-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-169">TM 已上線並接受要求。</span><span class="sxs-lookup"><span data-stu-id="1918b-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**交易 \_ 通知 \_ 要求 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="1918b-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="1918b-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-172">向 RMs 發出通知，指出有結果資訊可供使用，而且應該提出該資訊的要求。</span><span class="sxs-lookup"><span data-stu-id="1918b-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1918b-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**交易 \_ 通知 \_ 認可 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="1918b-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1918b-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="1918b-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="1918b-175">保留的。</span><span class="sxs-lookup"><span data-stu-id="1918b-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1918b-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="1918b-176">Requirements</span></span>



| <span data-ttu-id="1918b-177">需求</span><span class="sxs-lookup"><span data-stu-id="1918b-177">Requirement</span></span> | <span data-ttu-id="1918b-178">值</span><span class="sxs-lookup"><span data-stu-id="1918b-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1918b-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1918b-179">Minimum supported client</span></span><br/> | <span data-ttu-id="1918b-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1918b-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="1918b-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1918b-181">Minimum supported server</span></span><br/> | <span data-ttu-id="1918b-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1918b-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="1918b-183">標頭</span><span class="sxs-lookup"><span data-stu-id="1918b-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="1918b-184"><dt>KtmTypes (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1918b-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1918b-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1918b-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="1918b-186">[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1918b-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1918b-187">核心交易管理員常數</span><span class="sxs-lookup"><span data-stu-id="1918b-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="1918b-188">**CreateEnlistment**</span><span class="sxs-lookup"><span data-stu-id="1918b-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="1918b-189">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="1918b-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="1918b-190">**GetNotificationResourceManager**</span><span class="sxs-lookup"><span data-stu-id="1918b-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="1918b-191">**GetNotificationResourceManagerAsync**</span><span class="sxs-lookup"><span data-stu-id="1918b-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="1918b-192">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="1918b-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="1918b-193">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="1918b-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="1918b-194">**交易 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="1918b-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

