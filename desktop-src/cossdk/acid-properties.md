---
description: 創造 by transaction 處理先鋒，縮寫 ACID 表示不可部分完成、一致、隔離且持久。
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: ACID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110568"
---
# <a name="acid-properties"></a><span data-ttu-id="363ba-103">ACID 屬性</span><span class="sxs-lookup"><span data-stu-id="363ba-103">ACID Properties</span></span>

<span data-ttu-id="363ba-104">創造 by transaction 處理先鋒，縮寫 ACID 表示不可部分完成、一致、隔離且持久。</span><span class="sxs-lookup"><span data-stu-id="363ba-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="363ba-105">為了確保可預測的行為，所有交易都必須擁有這些基本屬性，並將任務關鍵性交易的角色強化為全或無主張。</span><span class="sxs-lookup"><span data-stu-id="363ba-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="363ba-106">下列清單包含每個 ACID 屬性的定義和描述：</span><span class="sxs-lookup"><span data-stu-id="363ba-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="363ba-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>原子</span><span class="sxs-lookup"><span data-stu-id="363ba-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="363ba-108">交易必須剛好執行一次，而且必須是不可部分完成的，也就是所有工作都已完成或全都不是。</span><span class="sxs-lookup"><span data-stu-id="363ba-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="363ba-109">交易內的作業通常會共用通用意圖，且都是相互依存的。</span><span class="sxs-lookup"><span data-stu-id="363ba-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="363ba-110">藉由只執行這些作業的子集，系統可能會危及交易的整體意圖。</span><span class="sxs-lookup"><span data-stu-id="363ba-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="363ba-111">不可部分完成性可消除只處理一部分作業的機會。</span><span class="sxs-lookup"><span data-stu-id="363ba-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="363ba-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>一致</span><span class="sxs-lookup"><span data-stu-id="363ba-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="363ba-113">交易必須維持資料的一致性，將資料的一致狀態轉換成另一種一致的資料狀態。</span><span class="sxs-lookup"><span data-stu-id="363ba-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="363ba-114">維持一致性的大部分責任都與應用程式開發人員有關。</span><span class="sxs-lookup"><span data-stu-id="363ba-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="363ba-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>孤立</span><span class="sxs-lookup"><span data-stu-id="363ba-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="363ba-116">交易必須是隔離單位，這表示並行的交易應該會像是在系統中唯一執行的交易一樣運作。</span><span class="sxs-lookup"><span data-stu-id="363ba-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="363ba-117">由於高度隔離可能會限制並行交易數目，因此有些應用程式會減少 exchange 中的隔離等級，以獲得更好的輸送量。</span><span class="sxs-lookup"><span data-stu-id="363ba-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="363ba-118">如需詳細資訊，請參閱設定 [交易隔離等級](configuring-transaction-isolation-levels.md) 。</span><span class="sxs-lookup"><span data-stu-id="363ba-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="363ba-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>耐用</span><span class="sxs-lookup"><span data-stu-id="363ba-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="363ba-120">交易必須可復原，因此必須具有持久性。</span><span class="sxs-lookup"><span data-stu-id="363ba-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="363ba-121">如果交易認可，系統會保證即使電腦在認可之後立即損毀，也可以保存其更新。</span><span class="sxs-lookup"><span data-stu-id="363ba-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="363ba-122">特製化記錄可讓系統的重新開機程式完成交易所需的未完成作業，使交易持久。</span><span class="sxs-lookup"><span data-stu-id="363ba-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



