---
description: COM + 可讓開發人員藉由允許可設定的交易隔離等級，更充分掌控應用程式。
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: 設定交易隔離等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468113"
---
# <a name="configuring-transaction-isolation-levels"></a><span data-ttu-id="54345-103">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="54345-103">Configuring Transaction Isolation Levels</span></span>

<span data-ttu-id="54345-104">COM + 可讓開發人員藉由允許可設定的交易隔離等級，更充分掌控應用程式。</span><span class="sxs-lookup"><span data-stu-id="54345-104">COM+ gives developers more control over their applications by allowing configurable transaction isolation levels.</span></span> <span data-ttu-id="54345-105">COM + 1.5 之前的 COM + 版本一律使用交易的最高層級隔離。</span><span class="sxs-lookup"><span data-stu-id="54345-105">Versions of COM+ prior to COM+ 1.5 always used the highest level of isolation for transactions.</span></span> <span data-ttu-id="54345-106">雖然這個層級保證一定會保留資料的完整性，但在大型資料庫上需要執行許多交易時，可能會導致效能問題（例如超時）。</span><span class="sxs-lookup"><span data-stu-id="54345-106">While this level guarantees that data integrity is always preserved, it can lead to performance issues, such as time-outs, when many transactions need to be performed on a large database.</span></span> <span data-ttu-id="54345-107">有了可設定的隔離等級，有經驗的開發人員可以增加並行，以改善效能和擴充性。</span><span class="sxs-lookup"><span data-stu-id="54345-107">With configurable isolation levels, experienced developers can increase concurrency to improve performance and scalability.</span></span>

<span data-ttu-id="54345-108">COM + 提供下列交易隔離等級。</span><span class="sxs-lookup"><span data-stu-id="54345-108">COM+ provides the following transaction isolation levels.</span></span>



| <span data-ttu-id="54345-109">層級</span><span class="sxs-lookup"><span data-stu-id="54345-109">Level</span></span>            | <span data-ttu-id="54345-110">描述</span><span class="sxs-lookup"><span data-stu-id="54345-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54345-111">序列化</span><span class="sxs-lookup"><span data-stu-id="54345-111">Serialized</span></span>       | <span data-ttu-id="54345-112">在目前的交易完成之前，其他交易無法變更目前交易讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="54345-112">Data read by a current transaction cannot be changed by another transaction until the current transaction finishes.</span></span> <span data-ttu-id="54345-113">無法插入任何可能會影響目前交易的新資料。</span><span class="sxs-lookup"><span data-stu-id="54345-113">No new data can be inserted that would affect the current transaction.</span></span> <span data-ttu-id="54345-114">這是最安全的隔離等級，而且是預設值。</span><span class="sxs-lookup"><span data-stu-id="54345-114">This is the safest isolation level and is the default.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="54345-115">可重複讀取</span><span class="sxs-lookup"><span data-stu-id="54345-115">Repeatable read</span></span>  | <span data-ttu-id="54345-116">在目前的交易完成之前，其他交易無法變更目前交易讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="54345-116">Data read by a current transaction cannot be changed by another transaction until the current transaction finishes.</span></span> <span data-ttu-id="54345-117">任何類型的新資料都可以在交易期間插入。</span><span class="sxs-lookup"><span data-stu-id="54345-117">Any type of new data can be inserted during a transaction.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="54345-118">讀取認可</span><span class="sxs-lookup"><span data-stu-id="54345-118">Read committed</span></span>   | <span data-ttu-id="54345-119">交易無法讀取其他尚未認可的交易正在修改的資料。</span><span class="sxs-lookup"><span data-stu-id="54345-119">A transaction cannot read data that is being modified by another transaction that has not committed.</span></span> <span data-ttu-id="54345-120">這是 Microsoft SQL Server 中的預設隔離等級。</span><span class="sxs-lookup"><span data-stu-id="54345-120">This is the default isolation level in Microsoft SQL Server.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="54345-121">讀取未認可</span><span class="sxs-lookup"><span data-stu-id="54345-121">Read uncommitted</span></span> | <span data-ttu-id="54345-122">交易可以讀取任何資料，即使是由另一筆交易修改也是一樣。</span><span class="sxs-lookup"><span data-stu-id="54345-122">A transaction can read any data, even if it is being modified by another transaction.</span></span> <span data-ttu-id="54345-123">這是最不安全的隔離等級，但允許最高的平行存取。</span><span class="sxs-lookup"><span data-stu-id="54345-123">This is the least safe isolation level but allows the highest concurrency.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="54345-124">任意</span><span class="sxs-lookup"><span data-stu-id="54345-124">Any</span></span>              | <span data-ttu-id="54345-125">支援任何隔離等級。</span><span class="sxs-lookup"><span data-stu-id="54345-125">Any isolation level is supported.</span></span> <span data-ttu-id="54345-126">下游元件最常使用此設定，以避免發生衝突。</span><span class="sxs-lookup"><span data-stu-id="54345-126">This setting is most commonly used by downstream components to avoid conflicts.</span></span> <span data-ttu-id="54345-127">這項設定很有用，因為任何下游元件的設定都必須使用等於或小於其直屬上游元件隔離等級的隔離等級。</span><span class="sxs-lookup"><span data-stu-id="54345-127">This setting is useful because any downstream component must be configured with an isolation level that is equal to or less than the isolation level of its immediate upstream component.</span></span> <span data-ttu-id="54345-128">因此，其隔離等級設定為 [任何] 的下游元件，一律會使用其直屬上游元件所使用的相同隔離等級。</span><span class="sxs-lookup"><span data-stu-id="54345-128">Therefore, a downstream component that has its isolation level configured as Any always uses the same isolation level that its immediate upstream component uses.</span></span> <span data-ttu-id="54345-129">如果交易中的根物件將其隔離等級設定為 [任何]，則會將其隔離等級序列化。</span><span class="sxs-lookup"><span data-stu-id="54345-129">If the root object in a transaction has its isolation level configured to Any, its isolation level becomes Serialized.</span></span> |



 

> [!Note]  
> <span data-ttu-id="54345-130">如果下游元件的設定比上游元件更高的隔離等級，並嘗試在交易中登記，則會產生錯誤結果，並中止交易。</span><span class="sxs-lookup"><span data-stu-id="54345-130">If a downstream component is configured with a higher isolation level than an upstream component and attempts to enlist in a transaction, an error results and the transaction aborts.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54345-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="54345-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54345-132">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="54345-132">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



