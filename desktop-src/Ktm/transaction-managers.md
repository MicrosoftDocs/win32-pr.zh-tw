---
description: 交易管理員 (TM) 是記錄檔的實例。 在 KTM 中，TM 物件指定了 TM 的記錄檔和一些功能。 在特定節點上通常會有許多 TM 物件。  (RMs) 的資源管理員必須與特定 TM 相關聯。
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: 交易管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978926"
---
# <a name="transaction-managers"></a><span data-ttu-id="2bd70-106">交易管理員</span><span class="sxs-lookup"><span data-stu-id="2bd70-106">Transaction Managers</span></span>

<span data-ttu-id="2bd70-107">交易管理員 (TM) 是記錄檔的實例。</span><span class="sxs-lookup"><span data-stu-id="2bd70-107">A transaction manager (TM) is an instance of a log.</span></span> <span data-ttu-id="2bd70-108">在 KTM 中，TM 物件指定了 TM 的記錄檔和一些功能。</span><span class="sxs-lookup"><span data-stu-id="2bd70-108">In KTM, the TM objects specify the log and some of the functionality of the TM.</span></span> <span data-ttu-id="2bd70-109">在特定節點上通常會有許多 TM 物件。</span><span class="sxs-lookup"><span data-stu-id="2bd70-109">There are typically many TM objects on a particular node.</span></span> <span data-ttu-id="2bd70-110"> (RMs) 的資源管理員必須與特定 TM 相關聯。</span><span class="sxs-lookup"><span data-stu-id="2bd70-110">Resource managers (RMs) must be associated with a specific TM.</span></span> <span data-ttu-id="2bd70-111">有三種類型的 Tm：</span><span class="sxs-lookup"><span data-stu-id="2bd70-111">There are three types of TMs:</span></span>

-   <span data-ttu-id="2bd70-112">Volatile TM，沒有記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2bd70-112">A volatile TM, which has no log.</span></span>
-   <span data-ttu-id="2bd70-113">一般 TM （具有記錄檔），用於協調一或多個 RMs 的交易。</span><span class="sxs-lookup"><span data-stu-id="2bd70-113">A regular TM, which has a log and is used to coordinate the transactions of one or more RMs.</span></span>
-   <span data-ttu-id="2bd70-114">優質的交易管理員。</span><span class="sxs-lookup"><span data-stu-id="2bd70-114">A superior transaction manager.</span></span>

## <a name="volatile-transaction-managers"></a><span data-ttu-id="2bd70-115">Volatile 交易管理員</span><span class="sxs-lookup"><span data-stu-id="2bd70-115">Volatile Transaction Managers</span></span>

<span data-ttu-id="2bd70-116">Volatile TM 是唯讀或暫時性 RMs 的 TM。</span><span class="sxs-lookup"><span data-stu-id="2bd70-116">A volatile TM is a TM for read-only or volatile RMs.</span></span> <span data-ttu-id="2bd70-117">它沒有記錄檔，而且不會保存跨系統重新開機的交易狀態。</span><span class="sxs-lookup"><span data-stu-id="2bd70-117">It does not have a log and does not persist the state of transactions across system restarts.</span></span>

## <a name="transaction-managers"></a><span data-ttu-id="2bd70-118">交易管理員</span><span class="sxs-lookup"><span data-stu-id="2bd70-118">Transaction Managers</span></span>

<span data-ttu-id="2bd70-119">Tm 有記錄、一或多個永久性或 volatile RMs，或兩者都有。</span><span class="sxs-lookup"><span data-stu-id="2bd70-119">TMs have a log, one or more durable or volatile RMs, or both.</span></span> <span data-ttu-id="2bd70-120">TM 會跨系統重新開機來保存交易的狀態，直到交易完成為止。</span><span class="sxs-lookup"><span data-stu-id="2bd70-120">The TM will persist the state of a transaction across system restarts until the transactions are completed.</span></span> <span data-ttu-id="2bd70-121">使用「假設-中止」模型，因此會回復在 TM 物件關閉時作用中但未備妥的交易。</span><span class="sxs-lookup"><span data-stu-id="2bd70-121">A presumed-abort model is used, so transactions which were active but not prepared when the TM object is shut down are rolled back.</span></span> <span data-ttu-id="2bd70-122">當您第一次開啟 TM 時，必須藉由呼叫 [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) 函式來復原 tm。</span><span class="sxs-lookup"><span data-stu-id="2bd70-122">When you open a TM for the first time, you must recover the TM by calling the [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) function.</span></span>

## <a name="superior-transaction-managers"></a><span data-ttu-id="2bd70-123">優質的交易管理員</span><span class="sxs-lookup"><span data-stu-id="2bd70-123">Superior Transaction Managers</span></span>

<span data-ttu-id="2bd70-124">絕佳的 TM 是 TM，適用于其他的 tm。</span><span class="sxs-lookup"><span data-stu-id="2bd70-124">A superior TM is a TM for other TMs.</span></span> <span data-ttu-id="2bd70-125">它會協調交易。</span><span class="sxs-lookup"><span data-stu-id="2bd70-125">It coordinates transactions.</span></span> <span data-ttu-id="2bd70-126">它也會發出 **交易通知，讓 \_ \_** 核心交易管理員 (KTM) 的通知。</span><span class="sxs-lookup"><span data-stu-id="2bd70-126">It also issues **TRANSACTION\_NOTIFY\_PREPARE** notifications to the Kernel Transaction Manager (KTM).</span></span> <span data-ttu-id="2bd70-127">Microsoft Distributed Transaction Coordinator (DTC) ，就是絕佳 TM 的範例。</span><span class="sxs-lookup"><span data-stu-id="2bd70-127">An example of a superior TM is the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="2bd70-128">這種功能有額外的復原時間責任。</span><span class="sxs-lookup"><span data-stu-id="2bd70-128">This ability comes with an added recovery-time responsibility.</span></span> <span data-ttu-id="2bd70-129">在復原期間，RM 必須先呼叫 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) 函式來重新開啟登記。</span><span class="sxs-lookup"><span data-stu-id="2bd70-129">During recovery, the RM must first call the [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) function to re-open the enlistment.</span></span> <span data-ttu-id="2bd70-130">如果認可交易，它也必須提供 (或重新傳遞) 交易的結果;藉由呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) 函式或 [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) 函式，即可自由傳遞結果。</span><span class="sxs-lookup"><span data-stu-id="2bd70-130">It must also deliver (or re-deliver) the transaction's outcome if the transaction was committed; it is free to deliver an outcome by calling either the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function or the [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) function.</span></span> <span data-ttu-id="2bd70-131">此義務在收到相關聯的 **交易 \_ 通知 \_ 認可 \_ 完成** 或 **交易 \_ 通知 \_ 回復 \_ 完成** 通知事件之前，不會結束。如果上層 TM 無法在復原時執行這些作業，KTM 將會清除復原階段結束時尚未接收結果的任何交易。</span><span class="sxs-lookup"><span data-stu-id="2bd70-131">This obligation does not end until it has received an associated **TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE** or **TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE** notification event.If a superior TM fails to perform these operations at recovery time, the KTM will clean up any transactions that have not received outcomes by the end of the recovery phase.</span></span> <span data-ttu-id="2bd70-132">不過，這可能會導致交易結果不一致。</span><span class="sxs-lookup"><span data-stu-id="2bd70-132">However, this can result in inconsistent transaction outcomes.</span></span>

## <a name="transaction-manager-functions"></a><span data-ttu-id="2bd70-133">交易管理員函數</span><span class="sxs-lookup"><span data-stu-id="2bd70-133">Transaction Manager Functions</span></span>

<span data-ttu-id="2bd70-134">下列函數會與交易管理員一起使用。</span><span class="sxs-lookup"><span data-stu-id="2bd70-134">The following functions are used with transaction managers.</span></span>



| <span data-ttu-id="2bd70-135">函式</span><span class="sxs-lookup"><span data-stu-id="2bd70-135">Function</span></span>                                                                            | <span data-ttu-id="2bd70-136">描述</span><span class="sxs-lookup"><span data-stu-id="2bd70-136">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bd70-137">**CreateTransactionManager**</span><span class="sxs-lookup"><span data-stu-id="2bd70-137">**CreateTransactionManager**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | <span data-ttu-id="2bd70-138">建立新的交易管理員 (TM) 物件，並傳回具有指定存取權的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2bd70-138">Creates a new transaction manager (TM) object and returns a handle with the specified access.</span></span>  |
| [<span data-ttu-id="2bd70-139">**GetCurrentClockTransactionManager**</span><span class="sxs-lookup"><span data-stu-id="2bd70-139">**GetCurrentClockTransactionManager**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | <span data-ttu-id="2bd70-140">從交易管理員取得虛擬時鐘值。</span><span class="sxs-lookup"><span data-stu-id="2bd70-140">Obtains a virtual clock value from a transaction manager.</span></span>                                      |
| [<span data-ttu-id="2bd70-141">**GetTransactionManagerId**</span><span class="sxs-lookup"><span data-stu-id="2bd70-141">**GetTransactionManagerId**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | <span data-ttu-id="2bd70-142">取得指定之交易管理員的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bd70-142">Obtains an identifier for the specified transaction manager.</span></span>                                   |
| [<span data-ttu-id="2bd70-143">**OpenTransactionManager**</span><span class="sxs-lookup"><span data-stu-id="2bd70-143">**OpenTransactionManager**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | <span data-ttu-id="2bd70-144">開啟現有的交易管理員。</span><span class="sxs-lookup"><span data-stu-id="2bd70-144">Opens an existing transaction manager.</span></span>                                                         |
| [<span data-ttu-id="2bd70-145">**RecoverTransactionManager**</span><span class="sxs-lookup"><span data-stu-id="2bd70-145">**RecoverTransactionManager**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | <span data-ttu-id="2bd70-146">從記錄檔復原交易管理員的狀態。</span><span class="sxs-lookup"><span data-stu-id="2bd70-146">Recovers a transaction manager's state from its log file.</span></span>                                      |
| [<span data-ttu-id="2bd70-147">**RollforwardTransactionManager**</span><span class="sxs-lookup"><span data-stu-id="2bd70-147">**RollforwardTransactionManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | <span data-ttu-id="2bd70-148">將交易管理員的狀態從其記錄檔復原到指定的虛擬時鐘值。</span><span class="sxs-lookup"><span data-stu-id="2bd70-148">Recovers a transaction manager's state from its log file to the specified virtual clock value.</span></span> |



 

 

 



