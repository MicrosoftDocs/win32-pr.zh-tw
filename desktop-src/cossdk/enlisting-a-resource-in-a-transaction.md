---
description: 在交易中登記資源
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: 在交易中登記資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386009"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="71e8f-103">在交易中登記資源</span><span class="sxs-lookup"><span data-stu-id="71e8f-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="71e8f-104">配置資源之後，但在將資源傳回給資源配置器之前，分配器管理員會檢查 COM + 以查看呼叫物件是否正在交易內執行。</span><span class="sxs-lookup"><span data-stu-id="71e8f-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="71e8f-105">如果呼叫的物件是在交易內執行，則分配器管理員會回呼至資源配置器，並要求它在交易中登記資源。</span><span class="sxs-lookup"><span data-stu-id="71e8f-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="71e8f-106">然後，資源會傳回給資源配置器，然後將它傳回給呼叫的實例。</span><span class="sxs-lookup"><span data-stu-id="71e8f-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="71e8f-107">資源配置器必須能夠在具有分散式交易協調器 (DTC) 的 OLE 交易中登記。</span><span class="sxs-lookup"><span data-stu-id="71e8f-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="71e8f-108">當資源配置不表達非交易資源（例如記憶體或執行緒）時，交易登記是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="71e8f-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="71e8f-109">當交易完成時，COM + 會通知分配者管理員其是否已認可或中止。</span><span class="sxs-lookup"><span data-stu-id="71e8f-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="71e8f-110">然後，分配者管理員會通知每個資源配置器的持有者，此交易中登記的任何資源現在都可以移至一般清查。</span><span class="sxs-lookup"><span data-stu-id="71e8f-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e8f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e8f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e8f-112">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="71e8f-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="71e8f-113">適用于 COM + 資源配置器的共用資源狀態</span><span class="sxs-lookup"><span data-stu-id="71e8f-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="71e8f-114">資源配置器資源配置進程</span><span class="sxs-lookup"><span data-stu-id="71e8f-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



