---
description: COM + 交易
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: COM + 交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385961"
---
# <a name="com-transactions"></a><span data-ttu-id="f03b0-103">COM + 交易</span><span class="sxs-lookup"><span data-stu-id="f03b0-103">COM+ Transactions</span></span>

<span data-ttu-id="f03b0-104">當您從線上書店購買書籍時，您會使用信用卡來交易書籍的費用。</span><span class="sxs-lookup"><span data-stu-id="f03b0-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="f03b0-105">提交訂單之後，一系列的相關作業 (驗證信用卡、清查可用性的驗證等) 確保您能取得書籍，而書店會取得您的金錢。</span><span class="sxs-lookup"><span data-stu-id="f03b0-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="f03b0-106">如果在交換期間，序列中的單一作業失敗，則整個交換會失敗。</span><span class="sxs-lookup"><span data-stu-id="f03b0-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="f03b0-107">您不會取得書籍，而書店也無法取得您的金錢。</span><span class="sxs-lookup"><span data-stu-id="f03b0-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="f03b0-108">負責讓此線上交換平衡且可預測的技術稱為 *交易處理*。</span><span class="sxs-lookup"><span data-stu-id="f03b0-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="f03b0-109">以程式設計的方式， *交易* 是一系列作業發生的工作單位。</span><span class="sxs-lookup"><span data-stu-id="f03b0-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="f03b0-110">除非交易內的所有作業都順利完成，否則 COM + 會使用程式設計交易來確保資源不會永久更新。</span><span class="sxs-lookup"><span data-stu-id="f03b0-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="f03b0-111">藉由將一組相關的作業一起系結到完全成功或完全失敗的 COM + 交易中，您可以大幅簡化錯誤復原。</span><span class="sxs-lookup"><span data-stu-id="f03b0-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="f03b0-112">下列主題介紹一般交易處理理論、更深入瞭解 COM + 中的交易，以及提供撰寫交易元件的實際秘訣。</span><span class="sxs-lookup"><span data-stu-id="f03b0-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="f03b0-113">主題</span><span class="sxs-lookup"><span data-stu-id="f03b0-113">Topic</span></span>                                                                   | <span data-ttu-id="f03b0-114">描述</span><span class="sxs-lookup"><span data-stu-id="f03b0-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="f03b0-115">COM + 交易概念</span><span class="sxs-lookup"><span data-stu-id="f03b0-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="f03b0-116">提供基本的詞彙和概念。</span><span class="sxs-lookup"><span data-stu-id="f03b0-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="f03b0-117">COM + 交易工作</span><span class="sxs-lookup"><span data-stu-id="f03b0-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="f03b0-118">提供撰寫交易元件的實用資訊。</span><span class="sxs-lookup"><span data-stu-id="f03b0-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




