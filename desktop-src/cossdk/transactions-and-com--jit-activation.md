---
description: 交易和 COM + JIT 啟用
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: 交易和 COM + JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847507"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="fba5c-103">交易和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="fba5c-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="fba5c-104">COM + JIT 啟用會緊密地系結至自動交易。</span><span class="sxs-lookup"><span data-stu-id="fba5c-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="fba5c-105">當您將元件設定為需要交易或需要新的交易時，JIT 啟用也會自動啟用。</span><span class="sxs-lookup"><span data-stu-id="fba5c-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="fba5c-106">這兩項功能自然地搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fba5c-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="fba5c-107">交易式 JIT 啟用的元件會共用下列特性：</span><span class="sxs-lookup"><span data-stu-id="fba5c-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="fba5c-108">無 國籍。</span><span class="sxs-lookup"><span data-stu-id="fba5c-108">Statelessness.</span></span> <span data-ttu-id="fba5c-109">您不會保存可能違反交易隔離的狀態，也不會保留物件停用時遺失的狀態。</span><span class="sxs-lookup"><span data-stu-id="fba5c-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="fba5c-110">快速使用。</span><span class="sxs-lookup"><span data-stu-id="fba5c-110">Rapid use.</span></span> <span data-ttu-id="fba5c-111">在自動交易中執行工作的物件標準使用模式是執行一些小型工作單位、投票和結束。</span><span class="sxs-lookup"><span data-stu-id="fba5c-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="fba5c-112">您在 COM + 交易中投票的方式以及 JIT 啟用的信號 doneness，也會緊密系結在一起。</span><span class="sxs-lookup"><span data-stu-id="fba5c-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="fba5c-113">如需詳細資訊，請參閱 [設定完成位](setting-the-done-bit.md)。</span><span class="sxs-lookup"><span data-stu-id="fba5c-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="fba5c-114">重複使用。</span><span class="sxs-lookup"><span data-stu-id="fba5c-114">Repeated use.</span></span> <span data-ttu-id="fba5c-115">當交易式工作適當地細分時，用戶端會使用相同的物件來執行不可部分完成的工作。</span><span class="sxs-lookup"><span data-stu-id="fba5c-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="fba5c-116">在認可或中止時停用。</span><span class="sxs-lookup"><span data-stu-id="fba5c-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="fba5c-117">在 COM + 中，交易認可或中止時，會停用交易界限內的所有物件。</span><span class="sxs-lookup"><span data-stu-id="fba5c-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="fba5c-118">搭配 COM + 交易元件，JIT 啟用可將通道保持開啟狀態，因為用戶端持有交易對象的長期參考。</span><span class="sxs-lookup"><span data-stu-id="fba5c-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="fba5c-119">做進一步的增強功能，您可以選擇將交易對象集區化，以重複使用其保留的資源、加快物件重新啟用時間，以及密切地管理為指定物件使用記憶體資源的方式。</span><span class="sxs-lookup"><span data-stu-id="fba5c-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fba5c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="fba5c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fba5c-121">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="fba5c-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="fba5c-122">啟用元件的 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="fba5c-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="fba5c-123">物件共用和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="fba5c-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



