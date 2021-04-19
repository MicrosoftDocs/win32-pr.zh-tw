---
description: 交易是定義工作邏輯單位的物件。
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: " (核心交易管理員的交易) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978925"
---
# <a name="transactions"></a><span data-ttu-id="15bea-103">交易</span><span class="sxs-lookup"><span data-stu-id="15bea-103">Transactions</span></span>

<span data-ttu-id="15bea-104">交易是定義工作邏輯單位的物件。</span><span class="sxs-lookup"><span data-stu-id="15bea-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="15bea-105">只要有控制碼參考交易，交易就會處於作用中狀態，如果尚未認可或回復交易，則會將它視為使用中。</span><span class="sxs-lookup"><span data-stu-id="15bea-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="15bea-106">如果已建立交易，並且在認可或回復之前關閉了它的所有控制碼，就會回復交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="15bea-107">請考慮使用者模式交易式用戶端的案例，此用戶端會建立交易來界定其作業範圍，然後在一或多個資源管理員上執行更新。</span><span class="sxs-lookup"><span data-stu-id="15bea-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="15bea-108">發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="15bea-108">The following occurs:</span></span>

1.  <span data-ttu-id="15bea-109">用戶端會呼叫 [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) 函數來建立交易，並接收該交易的控制碼作為傳回值。</span><span class="sxs-lookup"><span data-stu-id="15bea-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="15bea-110">交易可以由任意數目的進程開啟或繼承;因此，每個進程都會參與交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="15bea-111">任何這些處理常式的失敗都會導致交易中止。</span><span class="sxs-lookup"><span data-stu-id="15bea-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="15bea-112">此交易可能還不是持續性。</span><span class="sxs-lookup"><span data-stu-id="15bea-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="15bea-113">如果交易使用的是假設性中止記錄，則只有在系統失敗時，才會復原已達到備妥狀態的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="15bea-114">用戶端必須明確地將交易傳遞給資源管理員。</span><span class="sxs-lookup"><span data-stu-id="15bea-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="15bea-115">用戶端會使用一或多個 RMs （例如交易式檔案系統）來執行其所有交易作業。</span><span class="sxs-lookup"><span data-stu-id="15bea-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="15bea-116">用戶端會呼叫 [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) 函數。</span><span class="sxs-lookup"><span data-stu-id="15bea-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="15bea-117">資源管理員會接收來自 KTM 的通知，以準備和認可其資料。</span><span class="sxs-lookup"><span data-stu-id="15bea-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="15bea-118">交易和執行緒</span><span class="sxs-lookup"><span data-stu-id="15bea-118">Transactions and Threads</span></span>

<span data-ttu-id="15bea-119">交易與執行緒不同。</span><span class="sxs-lookup"><span data-stu-id="15bea-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="15bea-120">多個執行緒或進程可以是單一交易的一部分。</span><span class="sxs-lookup"><span data-stu-id="15bea-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="15bea-121">相反地，執行緒可以是不同時間內數個不同交易的一部分。</span><span class="sxs-lookup"><span data-stu-id="15bea-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="15bea-122">交易函數</span><span class="sxs-lookup"><span data-stu-id="15bea-122">Transaction Functions</span></span>

<span data-ttu-id="15bea-123">下列函式會搭配交易使用。</span><span class="sxs-lookup"><span data-stu-id="15bea-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="15bea-124">函式</span><span class="sxs-lookup"><span data-stu-id="15bea-124">Function</span></span>                                                            | <span data-ttu-id="15bea-125">描述</span><span class="sxs-lookup"><span data-stu-id="15bea-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15bea-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="15bea-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="15bea-127">要求認可指定的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="15bea-128">**CommitTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="15bea-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="15bea-129">要求認可指定的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="15bea-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="15bea-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="15bea-131">建立新的交易對象。</span><span class="sxs-lookup"><span data-stu-id="15bea-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="15bea-132">**GetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="15bea-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="15bea-133">傳回指定之交易的要求資訊。</span><span class="sxs-lookup"><span data-stu-id="15bea-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="15bea-134">**OpenTransaction**</span><span class="sxs-lookup"><span data-stu-id="15bea-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="15bea-135">開啟現有的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="15bea-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="15bea-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="15bea-137">要求回復指定的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="15bea-138">**RollbackTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="15bea-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="15bea-139">要求回復指定的交易。</span><span class="sxs-lookup"><span data-stu-id="15bea-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="15bea-140">此函數會以非同步方式傳回。</span><span class="sxs-lookup"><span data-stu-id="15bea-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="15bea-141">**SetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="15bea-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="15bea-142">設定指定之交易的交易資訊。</span><span class="sxs-lookup"><span data-stu-id="15bea-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



