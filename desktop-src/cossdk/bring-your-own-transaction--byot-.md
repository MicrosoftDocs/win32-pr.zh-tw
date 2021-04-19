---
description: '整合您自己的交易 (BYOT) '
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: '整合您自己的交易 (BYOT) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973587"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="c21ac-103">整合您自己的交易 (BYOT) </span><span class="sxs-lookup"><span data-stu-id="c21ac-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="c21ac-104">BYOT 可讓您使用或繼承外部交易來建立元件。</span><span class="sxs-lookup"><span data-stu-id="c21ac-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="c21ac-105">也就是說，尚未有相關聯交易的元件可以取得交易。</span><span class="sxs-lookup"><span data-stu-id="c21ac-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="c21ac-106">目前，MTS 交易為自動;元件實例是否存在於交易中，會在建立時決定。</span><span class="sxs-lookup"><span data-stu-id="c21ac-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="c21ac-107">元件的交易屬性和其建立者會決定哪些交易與指定的實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="c21ac-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="c21ac-108">在所有情況下，MTS 都會控制交易存留期。</span><span class="sxs-lookup"><span data-stu-id="c21ac-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="c21ac-109">COM + 會將此延伸至，以允許將任意預先存在的 DTC 或 TIP 交易設定為新元件內容的交易屬性。</span><span class="sxs-lookup"><span data-stu-id="c21ac-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="c21ac-110">這可讓設定的元件與存留期由 TP 監視器、OTS 或 DBMS 控制的交易相關聯。</span><span class="sxs-lookup"><span data-stu-id="c21ac-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="c21ac-111">BYOT 交易必須謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="c21ac-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="c21ac-112">在某些情況下，它們可能會導致跨越多個同步處理網域的交易（也就是，它們允許具有交易的平行處理，進而造成鎖死狀況）。</span><span class="sxs-lookup"><span data-stu-id="c21ac-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="c21ac-113">自動交易（而不是 BYOT 交易）是商務元件撰寫者慣用的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="c21ac-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="c21ac-114">BYOT 交易的介面包含 [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) 介面和 [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) 介面。</span><span class="sxs-lookup"><span data-stu-id="c21ac-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="c21ac-115">**ICreateWithTransactionEx** 介面會建立在手動交易中登記的物件。</span><span class="sxs-lookup"><span data-stu-id="c21ac-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="c21ac-116">**ICreateWithTipTransactionEx** 介面會使用交易網際網路通訊協定 (提示) ，建立在手動交易內登錄的物件。</span><span class="sxs-lookup"><span data-stu-id="c21ac-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c21ac-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c21ac-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c21ac-118">繼承手動交易</span><span class="sxs-lookup"><span data-stu-id="c21ac-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



