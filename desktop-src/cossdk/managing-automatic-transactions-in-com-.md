---
description: 在 COM + 程式設計模型中，您可以設計您的元件來執行最佳&\# 郵件; 啟用商務邏輯或建立資料庫連接&\# 郵件; 並依賴 Microsoft Windows 的交易處理架構來自動化交易。
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: 管理 COM + 中的自動交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510675"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="f59e8-103">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="f59e8-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="f59e8-104">在 COM + 程式設計模型中，您可以設計您的元件來執行最棒的動作：啟用商務邏輯或建立資料庫連接，並依賴 Microsoft Windows 的交易處理架構來自動化交易。</span><span class="sxs-lookup"><span data-stu-id="f59e8-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="f59e8-105">啟動交易</span><span class="sxs-lookup"><span data-stu-id="f59e8-105">Starting a Transaction</span></span>

<span data-ttu-id="f59e8-106">COM + 在遇到下列其中一種情況時，會自動開始交易：</span><span class="sxs-lookup"><span data-stu-id="f59e8-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="f59e8-107">當非交易式用戶端呼叫需要交易的元件時，或需要新的交易時。</span><span class="sxs-lookup"><span data-stu-id="f59e8-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="f59e8-108">當交易式用戶端呼叫需要新交易的元件時。</span><span class="sxs-lookup"><span data-stu-id="f59e8-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="f59e8-109">如果 COM + 判斷物件應該有新的交易，它會先開始交易，然後將物件放在其中。</span><span class="sxs-lookup"><span data-stu-id="f59e8-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="f59e8-110">此程序包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f59e8-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="f59e8-111">COM + 會建立內容物件、將 [JIT](com--just-in-time-activation.md) 啟動和 [同步](com--synchronization.md) 處理屬性設定為 [必要]，並將 [一致] [和 [完成] 旗標](consistent-and-done-flags.md) 分別設定為 True 和 False。</span><span class="sxs-lookup"><span data-stu-id="f59e8-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="f59e8-112">COM + 會與分散式交易協調器 (DTC) 通訊以開始交易。</span><span class="sxs-lookup"><span data-stu-id="f59e8-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="f59e8-113">DTC 會協調實體交易。</span><span class="sxs-lookup"><span data-stu-id="f59e8-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="f59e8-114">DTC 會產生交易識別碼，並將它傳回給 COM +。</span><span class="sxs-lookup"><span data-stu-id="f59e8-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="f59e8-115">交易識別碼會建立交易界限。</span><span class="sxs-lookup"><span data-stu-id="f59e8-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="f59e8-116">參與交易的所有物件都會共用相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f59e8-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="f59e8-117">當用戶端建立物件時，COM + 會在交易界限內啟用它。</span><span class="sxs-lookup"><span data-stu-id="f59e8-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="f59e8-118">結束交易</span><span class="sxs-lookup"><span data-stu-id="f59e8-118">Ending a Transaction</span></span>

<span data-ttu-id="f59e8-119">在發生下列其中一種情況時，COM + 會藉由認可或中止來結束自動交易：</span><span class="sxs-lookup"><span data-stu-id="f59e8-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="f59e8-120">交易的根物件會完成其工作，且 COM + 會釋放它。</span><span class="sxs-lookup"><span data-stu-id="f59e8-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="f59e8-121">在根物件停用之後，交易會嘗試認可。</span><span class="sxs-lookup"><span data-stu-id="f59e8-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="f59e8-122">用戶端會釋放根物件。</span><span class="sxs-lookup"><span data-stu-id="f59e8-122">The client releases the root object.</span></span> <span data-ttu-id="f59e8-123">如果沒有參考，根物件就會停用，而且交易會嘗試認可。</span><span class="sxs-lookup"><span data-stu-id="f59e8-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="f59e8-124">交易超過其超時閾值。</span><span class="sxs-lookup"><span data-stu-id="f59e8-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="f59e8-125">如果未在交易超時期間內認可交易，則會自動中止交易，並停用與交易相關聯的所有物件。</span><span class="sxs-lookup"><span data-stu-id="f59e8-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="f59e8-126">預設的交易超時期限為60秒。</span><span class="sxs-lookup"><span data-stu-id="f59e8-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f59e8-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f59e8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f59e8-128">一致且完成的旗標</span><span class="sxs-lookup"><span data-stu-id="f59e8-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="f59e8-129">藉由通知根物件來加速交易</span><span class="sxs-lookup"><span data-stu-id="f59e8-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="f59e8-130">藉由呼叫 SetComplete 來終止自動交易</span><span class="sxs-lookup"><span data-stu-id="f59e8-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



